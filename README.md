# Wedlock API Documentation
This Repository Lists all API methods with input parameters(required/optional) also shows Response Format.

BASE-URL = "http://hostname/api/"

## Constants
-   Person Type
    - 1=groom
    - 2=bride
    - 3=key person
    - 4=guest

- RSVP Status
    - 0=pending
    - 1=coming
    - -1=not coming

## Get Wedding Invitations

-	GET Request
	-	User/invitation
- Parameters
	- contact
- Response
	```
	{  
	   "response":{  
	      "error":{  
	         "error_code":0,
	         "error_msg":"",
	         "msg":"Invitation found."
	      },
	      "wedding_invitation":[  
	         {  
	            "id":"7",
	            "folder_name":"1512378862",
	            "name":"Kristen & David",
	            "state":"1",
	            "city":"1",
	            "date":"2018-01-17",
	            "couple_photo_url":".\/uploads\/1512378862\/couple.png",
	            "pin":"13848333",
	            "welcome_note":"Event managed by Fusionbit events.",
	            "streaming_url":"",
	            "show_wedding":"1",
	            "qr_code_url":null,
	            "user_id":"1",
	            "api_key":"gs0wsw8s8gos88w8o808ggcw048ocwgsckwoc80s",
	            "is_deleted":"0",
	            "person_type":"2"
	         },
	         {  
	            "id":"1",
	            "folder_name":"1511263836",
	            "name":"Dadhichi Weds Unnati",
	            "state":"1",
	            "city":"1",
	            "date":"2017-11-21",
	            "couple_photo_url":".\/uploads\/1511263836\/couple.png",
	            "pin":"1234",
	            "welcome_note":"Event Manged By FusionBit",
	            "streaming_url":"https:\/\/www.youtube.com\/watch?v=-zJfwr-SZgY",
	            "show_wedding":"1",
	            "qr_code_url":null,
	            "user_id":"1",
	            "api_key":"ook804coccoww40ookg88kc48w4kskgsggwgk8cs",
	            "is_deleted":"0",
	            "person_type":"4"
	         }
	      ]
	   }
	}

	```
## Update User Profile

- Multipart POST Request
	- User/update_user_profile
- Parameters
	- user_image (optional)
	- name
	- guest_id
	- wedding_id
- Response
	```
	{  
	   "response":{  
	      "error":{  
	         "error_code":0,
	         "error_msg":"",
	         "msg":"Profile updated successfully"
	      }
	   }
	}
	```
## Update IOS Device Token
- GET Request
	- User/save_ios_device_token
- Parameters
	- contact
	- device_token
- Response
	```
	{  
	   "response":{  
	      "error":{  
	         "error_code":0,
	         "error_msg":"updated",
	         "msg":"Device token updated successfully."
	      }
	   }
	}
	```
## Get Full Wedding

- GET Request
	- Guest/wedding
- Parameters
	- API-KEY
	- name
	- contact
- Response
	```
	{  
	   "response":{  
	      "error":{  
	         "error_code":0,
	         "error_msg":"",
	         "msg":"Wedding found"
	      },
	      "wedding":{  
	         "id":"7",
	         "folder_name":"1512378862",
	         "name":"Kristen & David",
	         "state":"1",
	         "city":"1",
	         "date":"2018-01-17",
	         "couple_photo_url":".\/uploads\/1512378862\/couple.png",
	         "pin":"13848333",
	         "welcome_note":"Event managed by Fusionbit events.",
	         "streaming_url":"",
	         "show_wedding":"1",
	         "qr_code_url":null,
	         "user_id":"1",
	         "api_key":"gs0wsw8s8gos88w8o808ggcw048ocwgsckwoc80s",
	         "is_deleted":"0",
	         "guest":{  
	            "id":"31",
	            "wedding_id":"7",
	            "name":"Kristen Jackson",
	            "contact":"9409210488",
	            "email":"",
	            "designation":"",
	            "about":"Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
	            "face_image_url":".\/uploads\/1512378862\/bride.png",
	            "invited_in":null,
	            "person_type":"2",
	            "verification_image_url":null,
	            "groom_id":null,
	            "bride_id":"31",
	            "is_admin":"0",
	            "is_blocked":"0",
	            "android_device_token":"eNefwI45F4g:APA91bGeQNox72VeX11lMDn1ob_uxbpTKCIdS0oNgDV6d4QG8dxdSE3QZTE-tgWrMMmeaFmzQLESb32Nkk80Q-jfhTNl5czVC6uCO1OdrgsW7eGIHMCkR9KUsb9oSb6jj1v3Ba85xWBZ",
	            "ios_device_token":"",
	            "relation_name":null,
	            "person_type_name":"bride"
	         },
	         "groom":{  
	            "id":"32",
	            "wedding_id":"7",
	            "name":"David Hamm",
	            "contact":"0",
	            "email":"",
	            "designation":"",
	            "about":"It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem Ipsum is that it has a more-or-less normal distribution of letters, as opposed to using 'Content here, content here', making it look like readable English. Many desktop publishing packages and web page editors now use Lorem Ipsum as their default model text, and a search for 'lorem ipsum' will uncover many web sites still in their infancy. ",
	            "face_image_url":".\/uploads\/1512378862\/groom.png",
	            "relation":null,
	            "invited_in":null,
	            "person_type":"1",
	            "verification_image_url":null,
	            "groom_id":null,
	            "bride_id":null,
	            "is_admin":"0",
	            "is_blocked":"0",
	            "invitation":{  
	               "id":"4",
	               "wedding_id":"7",
	               "invitation_message":"Please celebrate with us \r\nthe freshness of new life \r\nand new love as we,\r\n\r\nLisa Anderson\r\nand\r\nJohn Taylor\r\n\r\nexchange wedding vows\r\n\r\nSunday, the seventh of October \r\ntwo thousand eighteen \r\nat six o'clock in the evening \r\n\r\nSt. Paul's Cathedral\r\n209 Flinders Ln, Melbourne\r\n\r\nReception to follow",
	               "share_message":"",
	               "tweet_tahuko":"",
	               "website_url":"",
	               "android_app_url":"",
	               "ios_app_url":"",
	               "groom_bride_id":"32"
	            },
	            "programs":[  
	               {  
	                  "id":"3",
	                  "wedding_id":"7",
	                  "program_name":"Engagement",
	                  "venue":"Courtyard Marriott",
	                  "bungalow_flat_no":"",
	                  "address":"",
	                  "city":"1",
	                  "state":"1",
	                  "pincode":"0",
	                  "location_lat":"23.0278763",
	                  "location_lng":"72.51216649999992",
	                  "instructions":"No gifts please......",
	                  "date_time":"2017-12-12 10:00:00",
	                  "program_image_url":".\/uploads\/1512378862\/programs\/1514894776.png",
	                  "common_program":"1",
	                  "groom_id":"32",
	                  "bride_id":"31",
	                  "is_deleted":"0"
	               },
	               {  
	                  "id":"4",
	                  "wedding_id":"7",
	                  "program_name":"Wedding",
	                  "venue":"Chanchal Party Plot",
	                  "bungalow_flat_no":"",
	                  "address":"",
	                  "city":"1",
	                  "state":"1",
	                  "pincode":"0",
	                  "location_lat":"23.0078496",
	                  "location_lng":"72.53787349999993",
	                  "instructions":"Come early it's my wedding.....",
	                  "date_time":"2017-12-15 11:00:00",
	                  "program_image_url":null,
	                  "common_program":"1",
	                  "groom_id":"32",
	                  "bride_id":"31",
	                  "is_deleted":"0"
	               },
	               {  
	                  "id":"7",
	                  "wedding_id":"7",
	                  "program_name":"Sangeet Sandhya",
	                  "venue":"Rajpath Club",
	                  "bungalow_flat_no":"",
	                  "address":"",
	                  "city":"1",
	                  "state":"1",
	                  "pincode":"0",
	                  "location_lat":"23.0342822",
	                  "location_lng":"72.50899319999996",
	                  "instructions":"Bring Props with you....",
	                  "date_time":"2018-01-20 20:00:00",
	                  "program_image_url":null,
	                  "common_program":"0",
	                  "groom_id":"32",
	                  "bride_id":"0",
	                  "is_deleted":"0"
	               }
	            ],
	            "key_persons":[  
	               {  
	                  "id":"86",
	                  "wedding_id":"7",
	                  "name":"Adam",
	                  "contact":"7570433857",
	                  "email":null,
	                  "designation":"Farmer",
	                  "about":null,
	                  "face_image_url":".\/uploads\/1512378862\/1516363819.png",
	                  "relation":"2",
	                  "invited_in":null,
	                  "person_type":"3",
	                  "verification_image_url":null,
	                  "groom_id":"32",
	                  "bride_id":null,
	                  "is_admin":"0",
	                  "is_blocked":"0",
	                  "relation_id":"2",
	                  "relation_name":"Father"
	               },
	               {  
	                  "id":"85",
	                  "wedding_id":"7",
	                  "name":"Olivia",
	                  "contact":"9832345234",
	                  "email":null,
	                  "designation":"Dancer",
	                  "about":null,
	                  "face_image_url":".\/uploads\/1512378862\/1516363632.png",
	                  "relation":"5",
	                  "invited_in":null,
	                  "person_type":"3",
	                  "verification_image_url":null,
	                  "groom_id":"32",
	                  "bride_id":null,
	                  "is_admin":"0",
	                  "is_blocked":"0",
	                  "relation_id":"5",
	                  "relation_name":"Sister"
	               }
	            ],
	            "albums":[  
	               {  
	                  "album_id":"9",
	                  "wedding_id":"7",
	                  "album_name":"Wedding",
	                  "album_type":"1",
	                  "guest_can_upload":"1",
	                  "guest_can_download":"1",
	                  "show_on_website":"0",
	                  "common_album":"1",
	                  "groom_id":"32",
	                  "bride_id":"31",
	                  "album_images":[  
	                     {  
	                        "image_id":"52",
	                        "album_id":"9",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Wedding\/pexels-photo-169198.jpeg",
	                        "image_title":"",
	                        "image_caption":""
	                     },
	                     {  
	                        "image_id":"50",
	                        "album_id":"9",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Wedding\/pexels-photo-169193.jpeg",
	                        "image_title":"",
	                        "image_caption":""
	                     },
	                     {  
	                        "image_id":"60",
	                        "album_id":"9",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Wedding\/pexels-photo%20%281%29.jpg",
	                        "image_title":"",
	                        "image_caption":""
	                     },
	                     {  
	                        "image_id":"61",
	                        "album_id":"9",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Wedding\/pexels-photo-193040.jpeg",
	                        "image_title":"",
	                        "image_caption":""
	                     },
	                     {  
	                        "image_id":"62",
	                        "album_id":"9",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Wedding\/pexels-photo-137576.jpeg",
	                        "image_title":"",
	                        "image_caption":""
	                     },
	                     {  
	                        "image_id":"63",
	                        "album_id":"9",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Wedding\/pexels-photo.jpg",
	                        "image_title":"",
	                        "image_caption":""
	                     },
	                     {  
	                        "image_id":"64",
	                        "album_id":"9",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Wedding\/pexels-photo-169198%20%281%29.jpeg",
	                        "image_title":"",
	                        "image_caption":""
	                     }
	                  ]
	               },
	               {  
	                  "album_id":"11",
	                  "wedding_id":"7",
	                  "album_name":"My Solo Shoot",
	                  "album_type":"1",
	                  "guest_can_upload":"0",
	                  "guest_can_download":"1",
	                  "show_on_website":"1",
	                  "common_album":"0",
	                  "groom_id":"32",
	                  "bride_id":"0",
	                  "album_images":[  
	                     {  
	                        "image_id":"71",
	                        "album_id":"11",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/My Solo Shoot\/pexels-photo-103123.jpeg",
	                        "image_title":"",
	                        "image_caption":""
	                     },
	                     {  
	                        "image_id":"72",
	                        "album_id":"11",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/My Solo Shoot\/pexels-photo-450212.jpeg",
	                        "image_title":"",
	                        "image_caption":""
	                     },
	                     {  
	                        "image_id":"73",
	                        "album_id":"11",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/My Solo Shoot\/pexels-photo-372176.jpeg",
	                        "image_title":"",
	                        "image_caption":""
	                     },
	                     {  
	                        "image_id":"74",
	                        "album_id":"11",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/My Solo Shoot\/pexels-photo-432059.jpeg",
	                        "image_title":"",
	                        "image_caption":""
	                     }
	                  ]
	               }
	            ]
	         },
	         "bride":{  
	            "id":"31",
	            "wedding_id":"7",
	            "name":"Kristen Jackson",
	            "contact":"9409210488",
	            "email":"",
	            "designation":"",
	            "about":"Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
	            "face_image_url":".\/uploads\/1512378862\/bride.png",
	            "relation":null,
	            "invited_in":null,
	            "person_type":"2",
	            "verification_image_url":null,
	            "groom_id":null,
	            "bride_id":"31",
	            "is_admin":"0",
	            "is_blocked":"0",
	            "invitation":{  
	               "id":"3",
	               "wedding_id":"7",
	               "invitation_message":"Because you have shared in our lives by your friendship and love, we Kristen & David together with our parents invite you to share the beginning of our new life together when we exchange marriage vows.",
	               "share_message":"Hi all I Kristen kindly invite you all in my wedding.",
	               "tweet_tahuko":"I have tweeted",
	               "website_url":"http:\/\/localhost\/wedlock\/index.php\/Wedding?key=gs0wsw8s8gos88w8o808ggcw048ocwgsckwoc80s",
	               "android_app_url":"https:\/\/play.google.com\/store\/apps\/details?id=com.rutvik.moodleattendanceapp",
	               "ios_app_url":"https:\/\/play.google.com\/store\/apps\/details?id=com.rutvik.moodleattendanceapp",
	               "groom_bride_id":"31"
	            },
	            "programs":[  
	               {  
	                  "id":"3",
	                  "wedding_id":"7",
	                  "program_name":"Engagement",
	                  "venue":"Courtyard Marriott",
	                  "bungalow_flat_no":"",
	                  "address":"",
	                  "city":"1",
	                  "state":"1",
	                  "pincode":"0",
	                  "location_lat":"23.0278763",
	                  "location_lng":"72.51216649999992",
	                  "instructions":"No gifts please......",
	                  "date_time":"2017-12-12 10:00:00",
	                  "program_image_url":".\/uploads\/1512378862\/programs\/1514894776.png",
	                  "common_program":"1",
	                  "groom_id":"32",
	                  "bride_id":"31",
	                  "is_deleted":"0"
	               },
	               {  
	                  "id":"4",
	                  "wedding_id":"7",
	                  "program_name":"Wedding",
	                  "venue":"Chanchal Party Plot",
	                  "bungalow_flat_no":"",
	                  "address":"",
	                  "city":"1",
	                  "state":"1",
	                  "pincode":"0",
	                  "location_lat":"23.0078496",
	                  "location_lng":"72.53787349999993",
	                  "instructions":"Come early it's my wedding.....",
	                  "date_time":"2017-12-15 11:00:00",
	                  "program_image_url":null,
	                  "common_program":"1",
	                  "groom_id":"32",
	                  "bride_id":"31",
	                  "is_deleted":"0"
	               },
	               {  
	                  "id":"8",
	                  "wedding_id":"7",
	                  "program_name":"Ras Garba",
	                  "venue":"Jodhpur Park Soc",
	                  "bungalow_flat_no":"52",
	                  "address":"ramdev nagar brts bus stop, satellite road",
	                  "city":"1",
	                  "state":"1",
	                  "pincode":"380015",
	                  "location_lat":"23.02626249999999",
	                  "location_lng":"72.51402899999994",
	                  "instructions":"Bring dandya ",
	                  "date_time":"2018-01-20 19:00:00",
	                  "program_image_url":".\/uploads\/1512378862\/programs\/1516347409.png",
	                  "common_program":"0",
	                  "groom_id":"0",
	                  "bride_id":"31",
	                  "is_deleted":"0"
	               }
	            ],
	            "key_persons":[  
	               {  
	                  "id":"34",
	                  "wedding_id":"7",
	                  "name":"Jonathan",
	                  "contact":"9824143119",
	                  "email":null,
	                  "designation":"Senior Software Developer At BluSoft",
	                  "about":null,
	                  "face_image_url":".\/uploads\/1512378862\/1512464008.png",
	                  "relation":"6",
	                  "invited_in":null,
	                  "person_type":"3",
	                  "verification_image_url":null,
	                  "groom_id":null,
	                  "bride_id":"31",
	                  "is_admin":"0",
	                  "is_blocked":"0",
	                  "relation_id":"6",
	                  "relation_name":"Brother"
	               },
	               {  
	                  "id":"35",
	                  "wedding_id":"7",
	                  "name":"Genifer",
	                  "contact":"0",
	                  "email":null,
	                  "designation":"",
	                  "about":null,
	                  "face_image_url":".\/uploads\/1512378862\/1512464083.png",
	                  "relation":"1",
	                  "invited_in":null,
	                  "person_type":"3",
	                  "verification_image_url":null,
	                  "groom_id":null,
	                  "bride_id":"31",
	                  "is_admin":"0",
	                  "is_blocked":"0",
	                  "relation_id":"1",
	                  "relation_name":"Mother"
	               },
	               {  
	                  "id":"36",
	                  "wedding_id":"7",
	                  "name":"Json",
	                  "contact":"0",
	                  "email":null,
	                  "designation":"",
	                  "about":null,
	                  "face_image_url":".\/uploads\/1512378862\/1512464258.png",
	                  "relation":"2",
	                  "invited_in":null,
	                  "person_type":"3",
	                  "verification_image_url":null,
	                  "groom_id":null,
	                  "bride_id":"31",
	                  "is_admin":"0",
	                  "is_blocked":"0",
	                  "relation_id":"2",
	                  "relation_name":"Father"
	               },
	               {  
	                  "id":"81",
	                  "wedding_id":"7",
	                  "name":"Stephen B",
	                  "contact":"0",
	                  "email":null,
	                  "designation":"",
	                  "about":null,
	                  "face_image_url":".\/uploads\/1512378862\/1514895123.png",
	                  "relation":"23",
	                  "invited_in":null,
	                  "person_type":"3",
	                  "verification_image_url":null,
	                  "groom_id":null,
	                  "bride_id":"31",
	                  "is_admin":"0",
	                  "is_blocked":"0",
	                  "relation_id":"23",
	                  "relation_name":"Friend"
	               },
	               {  
	                  "id":"82",
	                  "wedding_id":"7",
	                  "name":" Jessica",
	                  "contact":"0",
	                  "email":null,
	                  "designation":"",
	                  "about":null,
	                  "face_image_url":".\/uploads\/1512378862\/1514895224.png",
	                  "relation":"5",
	                  "invited_in":null,
	                  "person_type":"3",
	                  "verification_image_url":null,
	                  "groom_id":null,
	                  "bride_id":"31",
	                  "is_admin":"0",
	                  "is_blocked":"0",
	                  "relation_id":"5",
	                  "relation_name":"Sister"
	               }
	            ],
	            "albums":[  
	               {  
	                  "album_id":"8",
	                  "wedding_id":"7",
	                  "album_name":"Pre wedding shoot",
	                  "album_type":"1",
	                  "guest_can_upload":"0",
	                  "guest_can_download":"0",
	                  "show_on_website":"1",
	                  "common_album":"0",
	                  "groom_id":null,
	                  "bride_id":"31",
	                  "album_images":[  
	                     {  
	                        "image_id":"58",
	                        "album_id":"8",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Pre wedding shoot\/pexels-photo-219776%20%281%29.jpeg",
	                        "image_title":"Beautiful Couple",
	                        "image_caption":"Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged."
	                     },
	                     {  
	                        "image_id":"57",
	                        "album_id":"8",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Pre wedding shoot\/pexels-photo-247295.jpeg",
	                        "image_title":"Beautiful Bride",
	                        "image_caption":"Getting ready for wedding"
	                     },
	                     {  
	                        "image_id":"48",
	                        "album_id":"8",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Pre wedding shoot\/pexels-photo-371312.jpeg",
	                        "image_title":"",
	                        "image_caption":""
	                     },
	                     {  
	                        "image_id":"55",
	                        "album_id":"8",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Pre wedding shoot\/pexels-photo-247858.jpeg",
	                        "image_title":"",
	                        "image_caption":""
	                     },
	                     {  
	                        "image_id":"56",
	                        "album_id":"8",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Pre wedding shoot\/pexels-photo-326625.jpeg",
	                        "image_title":"",
	                        "image_caption":""
	                     },
	                     {  
	                        "image_id":"54",
	                        "album_id":"8",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Pre wedding shoot\/food-couple-sweet-married.jpg",
	                        "image_title":"",
	                        "image_caption":""
	                     },
	                     {  
	                        "image_id":"59",
	                        "album_id":"8",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Pre wedding shoot\/pexels-photo-313707%20%281%29.jpeg",
	                        "image_title":"",
	                        "image_caption":""
	                     }
	                  ],
	                  "image_count":7,
	                  "album_image":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Pre wedding shoot\/pexels-photo-247295.jpeg"
	               },
	               {  
	                  "album_id":"9",
	                  "wedding_id":"7",
	                  "album_name":"Wedding",
	                  "album_type":"1",
	                  "guest_can_upload":"1",
	                  "guest_can_download":"1",
	                  "show_on_website":"0",
	                  "common_album":"1",
	                  "groom_id":"32",
	                  "bride_id":"31",
	                  "album_images":[  
	                     {  
	                        "image_id":"52",
	                        "album_id":"9",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Wedding\/pexels-photo-169198.jpeg",
	                        "image_title":"",
	                        "image_caption":""
	                     },
	                     {  
	                        "image_id":"50",
	                        "album_id":"9",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Wedding\/pexels-photo-169193.jpeg",
	                        "image_title":"",
	                        "image_caption":""
	                     },
	                     {  
	                        "image_id":"60",
	                        "album_id":"9",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Wedding\/pexels-photo%20%281%29.jpg",
	                        "image_title":"",
	                        "image_caption":""
	                     },
	                     {  
	                        "image_id":"61",
	                        "album_id":"9",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Wedding\/pexels-photo-193040.jpeg",
	                        "image_title":"",
	                        "image_caption":""
	                     },
	                     {  
	                        "image_id":"62",
	                        "album_id":"9",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Wedding\/pexels-photo-137576.jpeg",
	                        "image_title":"",
	                        "image_caption":""
	                     },
	                     {  
	                        "image_id":"63",
	                        "album_id":"9",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Wedding\/pexels-photo.jpg",
	                        "image_title":"",
	                        "image_caption":""
	                     },
	                     {  
	                        "image_id":"64",
	                        "album_id":"9",
	                        "image_url":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Wedding\/pexels-photo-169198%20%281%29.jpeg",
	                        "image_title":"",
	                        "image_caption":""
	                     }
	                  ],
	                  "image_count":7,
	                  "album_image":"http:\/\/localhost\/wedlock\/uploads\/files\/1512378862\/Wedding\/pexels-photo-169193.jpeg"
	               }
	            ]
	         },
	         "vendor":{  
	            "id":"1",
	            "email":"rutvik1061992@gmail.com",
	            "photographer_name":"Jaydip Bhatt",
	            "company_name":"Dreamsnaps",
	            "logo_url":".\/uploads\/vendor\/logos\/1514210627.png",
	            "background_url":".\/uploads\/vendor\/background\/1514272946.png",
	            "watermark_url":null,
	            "services":"Dream snaps is owned by Nikhil bhatt,Jaydip Bhatt and Mayur bhatt.\r\nWe specialize in wedding photography and events,cinematography wedding filler,corporate filming and candid photography. We have been associated with several news agencies since 1985. We are in Photography business 35+ years with passion.\r\nWe also design and provide photo book albums and high definition videos of weddings and events on blue ray discs.",
	            "since_in_market":"1985",
	            "website_url":"http:\/\/www.dreamsnapsindia.in\/",
	            "facebook_page_url":"https:\/\/www.facebook.com\/DreamSnaps.india\/",
	            "youtube_url":"https:\/\/www.youtube.com\/channel\/UCdcQbmAG_MVnXZfzRRRXvFQ",
	            "instagram_url":"",
	            "vimeo_url":"",
	            "address":"52 Jodhpur Park Soc Near Ramdevnagar Opp Courtyard Marriott",
	            "area":"Satellite",
	            "city":"1",
	            "state":"1",
	            "categories":"Candid Photography, ",
	            "pricing":"₹39500 - ₹64000",
	            "contact":"9409210488",
	            "other_contact":"079-26927476"
	         }
	      }
	   }
	}
	```
## Register Guest On Bride Side
- GET Request
	- Guest/register_guest_on_bride_side
- Parameters
	- API-KEY
	- guest_id
	- wedding_id
	- bride_id
- Response
	```
	{  
	   "response":{  
	      "error":{  
	         "error_code":0,
	         "error_msg":"",
	         "msg":"Guest registered on bride side."
	      }
	   }
	}
	```
## Register Guest On Groom Side
- GET Request
	- Guest/register_guest_on_groom_side
- Parameters
	- API-KEY
	- guest_id
	- wedding_id
	- groom_id
- Response
	```
	{  
	   "response":{  
	      "error":{  
	         "error_code":0,
	         "error_msg":"",
	         "msg":"Guest registered on groom side."
	      }
	   }
	}
	```
## RSVP Into Programs
- GET Request
	- Guest/going_into_program
- Parameters
	- API-KEY
	- guest_id
	- wedding_id
	- program_id
	- going (-1 = not going, 1 = going)
	- reason (optional)
- Response
	```
	{  
	   "response":{  
	      "error":{  
	         "error_code":0,
	         "error_msg":"",
	         "msg":"invitation updated successfully"
	      }
	   }
	}
	```
## Get Program RSVP Status Count For Bride
- GET Request
	- Guest/get_rsvp_status_bride
- Parameters
	- API-KEY
	- wedding_id
	- program_id
	- bride_id
- Response
	```
	{  
	   "response":{  
	      "error":{  
	         "error_code":0,
	         "error_msg":"",
	         "msg":""
	      },
	      "rsvp_status":{  
	         "coming":"1",
	         "not_coming":"1",
	         "pending":"0"
	      }
	   }
	}
	```
## Get Program RSVP Status Count For Groom
- GET Request
	- Guest/get_rsvp_status_groom
- Parameters
	- API-KEY
	- wedding_id
	- program_id
	- groom_id
- Response
	```
	{  
	   "response":{  
	      "error":{  
	         "error_code":0,
	         "error_msg":"",
	         "msg":""
	      },
	      "rsvp_status":{  
	         "coming":"1",
	         "not_coming":"1",
	         "pending":"0"
	      }
	   }
	}
	```
## Get Program RSVP Members List For Bride
- GET Request
	- Guest/get_rsvp_members_bride
- Parameters
	- API-KEY
	- wedding_id
	- program_id
	- bride_id
- Response
	```
	{  
	   "response":{  
	      "error":{  
	         "error_code":0,
	         "error_msg":"",
	         "msg":"rsvp members found"
	      },
	      "rsvp":[  
	         {  
	            "name":"Amishi Mehta",
	            "contact":"9409210477",
	            "email":null,
	            "designation":null,
	            "about":null,
	            "face_image_url":null,
	            "verification_image_url":null,
	            "is_admin":"0",
	            "is_blocked":"0",
	            "guest_invitation_id":"16",
	            "program_id":"3",
	            "is_going":"1",
	            "reason":"",
	            "wedding_id":"7",
	            "review":null
	         },
	         {  
	            "name":"Wedlock",
	            "contact":"7990673558",
	            "email":null,
	            "designation":null,
	            "about":null,
	            "face_image_url":null,
	            "verification_image_url":null,
	            "is_admin":"0",
	            "is_blocked":"0",
	            "guest_invitation_id":"24",
	            "program_id":"3",
	            "is_going":"0",
	            "reason":"",
	            "wedding_id":"7",
	            "review":null
	         }
	      ]
	   }
	}
	```
## Get Program RSVP Members List For Groom
- GET Request
	- Guest/get_rsvp_members_groom
- Parameters
	- API-KEY
	- wedding_id
	- program_id
	- groom_id
- Response
	```
	{  
	   "response":{  
	      "error":{  
	         "error_code":0,
	         "error_msg":"",
	         "msg":"rsvp members found"
	      },
	      "rsvp":[  
	         {  
	            "name":"Amishi Mehta",
	            "contact":"9409210477",
	            "email":null,
	            "designation":null,
	            "about":null,
	            "face_image_url":null,
	            "verification_image_url":null,
	            "is_admin":"0",
	            "is_blocked":"0",
	            "guest_invitation_id":"16",
	            "program_id":"3",
	            "is_going":"1",
	            "reason":"",
	            "wedding_id":"7",
	            "review":null
	         },
	         {  
	            "name":"Wedlock",
	            "contact":"7990673558",
	            "email":null,
	            "designation":null,
	            "about":null,
	            "face_image_url":null,
	            "verification_image_url":null,
	            "is_admin":"0",
	            "is_blocked":"0",
	            "guest_invitation_id":"24",
	            "program_id":"3",
	            "is_going":"0",
	            "reason":"",
	            "wedding_id":"7",
	            "review":null
	         }
	      ]
	   }
	}
	```
	
	## Upload photos to Album
- Multipart POST Request
	- Album/upload_images
- Parameters
	- guest_id
	- wedding_folder_name
	- album_name
	- album_id
	- album_images[] (Max: 10 images)
- Response
	```
	{  
       "response":{  
          "error":{  
             "error_code":0,
             "error_msg":"",
             "msg":""
          },
          "uploaded_images":[  
             {  
                "id":"1",
                "url":"http://wedlockclub.com/./uploads/files/1518500793/Pre Wedding/./uploads/files/1518500793/Pre Wedding/IMG-20180220-WA0004.jpg"
             },
             {  
                "id":"1",
                "url":"http://wedlockclub.com/./uploads/files/1518500793/Pre Wedding/./uploads/files/1518500793/Pre Wedding/IMG-20180220-WA0004.jpg"
             },
             {  
                "id":"1",
                "url":"http://wedlockclub.com/./uploads/files/1518500793/Pre Wedding/./uploads/files/1518500793/Pre Wedding/IMG-20180220-WA0004.jpg"
             },
             {  
                "id":"1",
                "url":"http://wedlockclub.com/./uploads/files/1518500793/Pre Wedding/./uploads/files/1518500793/Pre Wedding/IMG-20180220-WA0004.jpg"
             }
          ],
          "failed_images":[  
             "failed to upload",
             "invalid file name"
          ]
       }
    }
	```
	
		## Delete photo from Album
- POST Request
	- Album/delete_photo
- Parameters
	- image_id
	- guest_id
- Response
	```
	{  
	   "response":{  
	      "error":{  
	         "error_code":0,
	         "error_msg":"",
	         "msg":"image deleted successfully"
	      }
	   }
	}
	```
	
