# Doctors-Module
this will only will contain the app readme file for helping front-end developer



        @RequestMapping(value = "/DoctorProfile", method = RequestMethod.PUT)

        parameters : @RequestBody Doctor doc , @RequestParam String token            
        return : boolean 


         @RequestMapping(value = "/DoctorProfile", method = RequestMethod.GET)                              
         parameters :            @RequestParam String token                       
         return : Doctor


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
     
     
     
     
     @RequestMapping(value = "/Patient" ,  method = RequestMethod.DELETE )
     parameters :   @RequestBody PatientUser user 
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
  
    @RequestMapping(value = "/Exist/{userName}",method = RequestMethod.GET)
    parameters : @PathVariable(value = "userName") String userName)
    return : boolean 
  
  
    @RequestMapping(value = "/UploadImage" , method = RequestMethod.POST) // //new annotation since 4.3
     parameters : @RequestParam("file") MultipartFile file,@RequestParam String token
     return :             String
  
  
