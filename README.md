# TextToSpeech-SpeechToText-IBMWatson-Python
Through this project, two tools used in AI applications will be introduced and used to convert a live speech to a text and a text to a speech. An applicaion of these services is to create a robot that is able to have a conversation with customers and respond to them with natural-sounding voice and save that conversation which help business owners in developing their services. Both services are invented by IBM and are available for public use.

# Speech To Text

Through this section, IBM Watson’s Speech to Text service will be introduced. The service is used in this project to make the robot able to write customers’ evaluations. In order to be able to use the service, an API Key and a URL must be generated from IBM Cloud to access it and interact with the services (see the Figure below). However, the only informations that will be used is the API Key and the Region as it will be illustrated in the following section.

![STT IBM Watson](https://user-images.githubusercontent.com/85955049/127394999-be0b49f7-c4b7-427e-b276-b8fd500962e6.png)

**Code and License**

The code used in this program is written by Necholas Renotte and it is licensed and available to download and use. 
see: https://github.com/nicknochnack/RealTimeSpeechToText). 

The only file needs to be modified according to the service credentials of our speech to text service is the speech.cfg file. The Figure below shows the modified version of the file where the API key and the region are specified to be used later on the program transcribe.py. The program converts a live speech to a text within a 5 seconds period (may be changed by the command –t  time(seconds)).
![speech cfg](https://user-images.githubusercontent.com/85955049/127396693-ba202651-4303-479b-bcb9-9b41526262e3.png)


**Results**

After running the transcribe.py program, the output is printed as shown in the Figure below.
![STT Output](https://user-images.githubusercontent.com/85955049/127395733-cfbfac1f-ada3-4158-a7ed-256a609e80fa.png)

# Text To Speech
Through this section, IBM Watson’s Text to Speech service will be introduced. The service is used in this project to make the robot able to speak to the customer by converting written text into an audio with several languages and voice options. For example, the service supports Arabic language and the voice provided by IBM is a male called “Mr-Omar”, however, other languages support voices for both genders. Our speaker is a female called “Allison” and she speaks English with American accent. In order to be able to use the service, an API Key and a URL must be generated from IBM Cloud to access it and interact with the services (see the Figure below). In the following section, the text to speech program will be explained. 
![TTS IBM Watson](https://user-images.githubusercontent.com/85955049/127396044-eb3e2846-9de8-44c5-9833-37b5f7187067.png)

**Code**

The Figure below shows the program that converts a text to a speech. 
![TTS Program](https://user-images.githubusercontent.com/85955049/127396163-1ea207a7-d974-41e7-9b0c-2e00834a6cbf.png)

The first and the most important step is indicated to install the dependency “ibm_watson” to be able to access the service. The second step is to create two variables, one for the API key and the other for the URL and paste their values from the service credentials. The third step is to import the text to speech service from the dependency and to import the IAM authenticator which is used in the following step to request the service using the API key. The next two steps are to create a new TTS using the imported TextToSpeech service and then to set the service’s URL. Finally, the last three rows are indicated to convert the text to an audio as an .mp3 file. To clarify, the first row creates an .mp3 file with the name “TTS Output-Greeting” as an audio_file. Then the .synthesize function is used to synthesizes the text to an audio that is spoken in the specified voice and format “en-US_AllisonV3Voice” as well as the .get_result() to get the HTTP response of the service request and then the result is stored in the variable res. Finally, the .content function is used to fetch the content from the stored data in the variable res and .write the audio file.

**Result**

As it is mentioned before, the result is generated as an mp3 file and it is attached under the name “TTS output-Greeting”. 

