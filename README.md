# REST-API-CALL-ANDROID
This is rest client to call webservice or API. You can easily get data from the server using REST CLIENT. File uploading, image uploading and video uploading is easy using this REST CLIENT. It contains with okhttp library.

You just need to call webservice using ParseController class.

            Map<String, String> map = new HashMap<>();
            map.put("url", ENTER YOUR URL); // you can user global single url, check parsecontroller class.
            map.put("email", strEmail); //parameters goes here.
            map.put("password", strPassword);
            
            // this is post call, check 2nd parameter, map will send parameters and url, true is boolean to show progress dialog, Loading is message white requesting. Finall Success or failed will call.
            
            new ParseController(LoginActivity.this, ParseController.HttpMethod.POST, map, true, "Loading...", new                                AsyncTaskCompleteListener() {

                @Override
                public void onSuccess(String response) {
                    try {
                    
                        // you will get response string here...
                        JSONObject objMain = new JSONObject(response);
                       
                        
                        
                    } catch (Exception e) {
                        e.printStackTrace();
                    }
                }

                @Override
                public void onFailed(int statusCode, String msg) {
                     //here you will get statuscode and message if http request failed...
                }
            });
