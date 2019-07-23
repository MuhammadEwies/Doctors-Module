# Doctors-Module
this will only will contain the app readme file for helping front-end developer



        @RequestMapping(value = "/DoctorProfile", method = RequestMethod.PUT)

        parameters : @RequestBody Doctor doc , @RequestParam String token            
        return : boolean 


         @RequestMapping(value = "/DoctorProfile", method = RequestMethod.GET)                              
         parameters :            @RequestParam String token                       
         return : Doctor

         // tested update at 27/6/2019 Ewies
         @RequestMapping(value = "/DoctorProfilePic", method = RequestMethod.GET)
          parameters : @RequestParam String token  )
          return :PatientsImages
          
          @RequestMapping(value = "/DoctorProfilePic" , method = RequestMethod.PUT)
             parameters :@RequestParam("file") MultipartFile file
             return :@RequestParam String token
             
             
             // Doctor Object Example 
             //json 
                                     {
                          "profilepicture": null,
                          "location": {
                            "lat": "15ll",
                            "lon": "sdfg"
                          },
                          "socialMedia": {
                            "facebook": "jkjgfdsasdfghjknm, bvcfdstyhjbnvfgh",
                            "twitter": null,
                            "whatsapp": null,
                            "linkedin": null,
                            "youtube": null
                          },
                          "name": "mohamed",
                          "department": null,
                          "city": null,
                          "bio": null,
                          "image": null,
                          "address": null,
                          "id": 2,
                          "mail": null,
                          "second_phone": null,
                          "open_dates": null,
                          "first_phone": null
                        }
             /////////////////////////////////////////////////
             
             
             
             
             
             
             
             
             
             
             
             
         @RequestMapping(value = "/IsAuthenticated", method = RequestMethod.POST)                        
          parameters :    @RequestHeader String token                                                         
          return : boolean                                                


         @RequestMapping(value = "/login", method = RequestMethod.POST)                                 
            parameters :                                                                                                               
                 @RequestParam("password") String pass,                                                                      
                 @RequestParam("username") String username                                                                       
             return :        TokenReturn                                                                               
     
   
        @RequestMapping(value = "/logout", method = RequestMethod.GET)
          paramters :
              @RequestHeader String token
          return: 
              boolean
 
 
    
     @RequestMapping(value = "/ForgetPassword", method = RequestMethod.GET)
      paramters :
            @RequestParam(value = "Mail") String Mail
      return :
             boolean
     
     
     
      // updated 27/4/2019
     @RequestMapping(value = "/Patient" ,  method = RequestMethod.DELETE )
     parameters :   @RequestParam int id ,  @RequestParam String token
     return     :   String
    
    @RequestMapping(value = "/Patient",method = RequestMethod.PUT)
    parameters : @RequestBody MyPatient patient ,@RequestParam String token 
    return :  boolean

    
    @RequestMapping(value = "/Patient", method = RequestMethod.POST)
     paramerts :   @RequestBody PatientUser user, @RequestParam String token 
     return  :MyPatient



    
    @RequestMapping(value = "/Patients", method = RequestMethod.GET)
     paramters : @RequestParam String token 
     return : List<MyPatient>
  
   
  
     @RequestMapping(value = "/UploadImage" , method = RequestMethod.POST) // //new annotation since 4.3
     parameters : @RequestParam("file") MultipartFile file,@RequestParam String token , @RequestParam int Patient_id
     return :             String
  
     @RequestMapping(value = "/Appointments" , method = RequestMethod.GET)
      parameters : @RequestParam String token
      return:  List of json objects 
      
      
      @RequestMapping(value = "/Appointment" , method = RequestMethod.POST)
      parameters : @RequestParam String token , @RequestBody Appointment appointment)
      return:  boolean 
      
      
      @RequestMapping(value = "/Appointment" , method = RequestMethod.PUT)
      parameters : @RequestParam String token , @RequestBody Appointment appointment)
      return:  boolean 
       
      @RequestMapping(value = "/AppointmentsReport" , method = RequestMethod.GET)
      parameters : @RequestParam String token
      return: oject contains three interger values (Success , Fail , Pending ) 
      will be represented in a circle in UI as a report of rate 
      
      @RequestMapping(value = "/Appointment" , method = RequestMethod.DELETE)
       parameters :@RequestParam String token , @RequestBody Appointment appointment
       return:boolean
       @RequestMapping(value = "/PendingAppointments" , method = RequestMethod.GET)
         parameters : @RequestParam String token )
         return :  List<Appointment> 
         
        @RequestMapping(value = "/AppointmentToUser" , method = RequestMethod.POST)
        parameters:@RequestParam String token , @RequestBody Appointment appointment
        return:MyPatient
     
        @RequestMapping(value = "/SearchPatients", method = RequestMethod.GET)
         parameters : @RequestParam String token ,String phone 
          // this string phone is and string of numbers can be in the phone of the patients
         return :List<MyPatient>
         
         
         @RequestMapping(value = "/PatientsAgesReport", method = RequestMethod.GET)
           Parameter:  (@RequestParam String token
           Return : Map<String,Integer>
