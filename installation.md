How do we install Flutter in Windows, macOS and Linux OS like Ubuntu. In this section we will take a quick look at this topic.

Clicking the download button will automatically start downloading zipped Flutter in your Download folder. 

It would be around 700 MB in size. 

But everything else Smile with Code.

If you were born in September, it’s pretty safe to assume that your parents started their new year with a bang.
While extracting the file it would take around 1.30 GB of space on your hard drive. 

We have kept the extracted flutter folder there and created a new ‘environment’ path for the user. 

Because we want to work through the command prompt, in future, we have created this global environment path.

Creating a new environment variable path in any Windows operating system is also easy. 

In the Windows 10 operating system, we type ‘environment variable’ in the search prompt, it will automatically open up the related window for us.

We can copy and paste the whole path there as the following:

“C:\Users\Downloads\flutter\bin”.
Now, we can open the command prompt and type ‘flutter doctor’ to see whether we have any Flutter related IDE installed already. 

It will also check whether we have any connected devices or not.

We have not installed Android Studio or any other Flutter related IDE beforehand. 

The command ‘flutter doctor’ has detected that.

Are you a Beginner? Please read the following links.
Flutter Primer. We have planned it for absolute beginners who have not coded before.
Certainly, knowledge of Dart Programming is important. Please learn Dart. We have written articles on Dart for absolute beginners.
Moreover, You must know the Flutter latest versions. So go ahead. Make yourself comfortable with your Flutter Knowledge.
As a result, learning Dart and Flutter Important Concepts is important.
Most importantly, you must know how to deal with Images and Font Styling?
The basic layout Widgets without which you cannot start learning Flutter.
Which are Material Widgets and which are not? Learn them all.
Finally, an introduction to User Interface is necessary. So go ahead and read and practice to build beautiful designs.
To work with Flutter, we need a good IDE like Visual Studio Code. 

In fact, when we were downloading Flutter, it indicated that we should install Android Studio or any good IDE like VS code where we would have a connected device. 

The connected device is nothing but a virtual mobile device where we can see and test our mobile application.

Android Studio should be the best choice. 

It is widely used and Flutter’s home page also suggests downloading and installing that IDE.

In Flutter Doctor summary, we have found that Android Studio has not been installed and there is no device available.

We will do that in our macOS and Linux machines, because we will use any one of those operating systems to learn Flutter and Dart together.

Flutter for macOS and Linux
Downloading Flutter for macOS and Linux is the same. 

It will download the “flutter_linux_1.17.2-stable.tar.xz” file in your “Downloads” folder. 

Next we will issue the following command to extract Flutter, on our terminal:

tar xf flutter_linux_1.17.2-stable.tar.xz
Now we can copy this extracted ‘flutter’ directory to a suitable place, where we will build our first mobile application. 

In the ‘Documents’ directory, we have created another directory named ‘development’. 

We will keep the extracted ‘flutter’ directory there. 

Just like Windows 10, we will now set the global path for ‘flutter’, so that we can use the ‘flutter’ command, anywhere in our machine, in the future.

We will do that using ‘vim’ or ‘nano’ text editor, that works on the terminal. By the way, the commands are the same for any macOS or Linux operating system.

If you type the following command, the nano text editor will open up the ‘bashrc’ file.

nano ~/.bashrc
At the end of the ‘bashrc’ file we will add this line:


    export PATH=$PATH:/home/ss/Documents/development/flutter/bin:$PATH
We have to mention the full path as given above. We have kept our extracted ‘flutter/bin’ folder in the ‘/home/ss/Documents/development’ directory.

Our next step will be to download the Android Studio. 

Download the zipped folder and extract it anywhere in the machine. 

We have kept it in our ‘/home/’ directory. Next, issue this command:


    ss@ss-desktop:~$ cd android-studio/bin/
    ss@ss-desktop:~/android-studio/bin$ ./studio.sh 
It will open up the Android Studio for us. 

Once the Android Studio opens up, you can go to the ‘open folder’ option and choose the flutter project we have created already. 

How we have created it, we will come to that point in a minute. 

Before that, we need to see the Android Studio and our newly created virtual device.

Before opening the Android Studio, we opened up our terminal, and typed the following commands to reach the newly installed ‘flutter’ directory.

ss@ss-desktop:~$ cd Documents/development/flutter/
    ss@ss-desktop:~/Documents/development/flutter$ flutter doctor
    Doctor summary (to see all details, run flutter doctor -v):
    [✓] Flutter (Channel stable, v1.17.2, on Linux, locale en_IN)
    
    [✓] Android toolchain - develop for Android devices (Android SDK version 29.0.3)
    [✓] Android Studio (version 3.5)
    [✓] Android Studio (version 4.0)
    [✓] IntelliJ IDEA Community Edition (version 2019.3)
    [✓] VS Code (version 1.43.2)
    [!] Connected device
        ! No devices available

    ! Doctor found issues in 1 category.
    ss@ss-desktop:~/Documents/development/flutter$ 
As you have seen in the above output, ‘flutter doctor’ has found only one issue. 

It has not found any connected device. Otherwise, we have already installed Android Studio (version 4.0), which is the latest at the time of writing this book. 

We have also installed IntelliJ IDEA Community Edition, and we have also Visual Studio Code IDE. 

We can use the virtual device from Android Studio, but we can use the Visual Studio Code IDE or IntelliJ IDEA Community Edition IDE for writing our code. They will automatically synchronize with the connected device.

Once you have installed, please check the Flutter latest version and issue the following command:

flutter upgrade
However, before that we need to create our first flutter project with the help of flutter command as the following:


    flutter create my_first_flutter_app
Remember one thing. When we want to create a new flutter project, we should always create it like this. 

The naming convention is important here. 

We can only use the underscore between the words. No hyphen or space is allowed.

Now the time has come to go back to the Android Studio. 

We will pick up the ‘open folder’ option and choose to open the newly created flutter project.

We have named it as: ‘my_first_flutter_app’. 

To open up the connected device, we need to open the Android Virtual Device manager, or AVD manager in short. 

You will get that from the ‘tools’ menu.

Select any one of them and click the ‘green’ play button on the far right hand side of any virtual device. 

It will automatically open up the ‘connected device’.

Now everything is ready. We can start building our first mobile application from scratch using Flutter and Dart.

Before closing down this section, we should know a few good tips. 

Usually, the beginners encounter a few errors when they try to run the command:

flutter doctor
If it gives any error, try this command:

flutter doctor --android-licenses
It will ask you to accept the license. Accept it, and it will not give any error anymore. 

Another problem often gives trouble to the new developers.

As a beginning Flutter developer, people often are stuck with this issue. 

They cannot launch the virtual mobile device while working with Android Studio.

We want that every code we write should reflect on the virtual device. 

It can be done by going to the ‘AVD manager’ from tools. 

But sometimes an ugly error pops up its head and tells that ‘/dev/kvm permission denied’.

In Ubuntu 18 or Mac OS, you can give user the permission by issuing this command:

sudo chmod 777 -R /dev/kvm
But it has a drawback. If someone else uses your machine, then the other user also gets the permission.

The best remedy is – give permission to yourself only by the following commands:

 sudo apt install qemu-kvm
    sudo adduser your-username kvm
    sudo chown your-username /dev/kvm
It will solve the issue forever. 

Now you can launch any virtual device you want. You can launch the device with your Android Studio, and work with any other IDE like IntelliJ or Visual Studio.

