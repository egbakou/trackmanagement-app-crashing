<h3 align="center">
    <img src="src/assets/banner.png"/>
</h3>
#### Steps to reproduce the issue

1. Clone the LibVLCSharp repo on Github by using the command `https://github.com/egbakou/trackmanagement-app-crashing`
2. Open the solution in Visual Studio
3. When restore completed, make sure that your stratup project is `LibVLCSharp.Forms.Sample.MediaElement.Android`
4. Connect physical Android device to Visual Studio (Android 8.1 or 5.1)
5. Run the stratup project in debug mode

#### What's the expected result?
When the video has finished playing, you will have one of the two following situations:
1. The app closes automatically (Crash).
2. The app does not close automatically but when you click on the play button, It closes (Crash).

#### What's the actual result in Output?
`JNI DETECTED ERROR IN APPLICATION: a thread (tid 27209 is making JNI calls without being attached \[com.companynam\] runtime.cc:638\] in call to GetJavaVM \[com.companynam\] runtime.cc:638\] \[libc\] Fatal signal 6 (SIGABRT), code -1 (SI_QUEUE) in tid 27209 (Thread-194), pid 27161 (com.companyname)`
###### OR
`[art] Native thread exiting without having called DetachCurrentThread (maybe it's going to use a pthread_key_create destructor?): Thread[17,tid=22838,Native,Thread*=0xb9200ee8,peer=0x12e0b0a0,"mediacodec_jni"]
[libc] Fatal signal 11 (SIGSEGV), code 1, fault addr 0x0 in tid 22838 (mediacodec_jni)
[Choreographer] Skipped 62 frames!  The application may be doing too much work on its main thread.`
