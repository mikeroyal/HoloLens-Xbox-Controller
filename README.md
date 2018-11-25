# HoloLens Xbox Controller Plugin

![hololens controller](https://user-images.githubusercontent.com/18353476/29101706-017fa182-7c69-11e7-9a7c-4aa6eaa3d432.jpg)

![hololens](https://user-images.githubusercontent.com/18353476/38452317-adefc5f0-39f6-11e8-84fd-9dbc2c9d16da.gif)

Requirements:

[HoloLens headset](https://www.microsoft.com/en-us/hololens)

[Xbox One wireless controller](https://www.newegg.com/Product/Product.aspx?Item=N82E16874103563)

[Windows 10](https://www.microsoft.com/en-us/software-download/windows10)(Build 1709 or later).

[Unity 2017.3 ](https://unity3d.com/)or later.

[Visual Studio 2017](https://www.visualstudio.com/) or later.

# Developing for VR, AR, and Mixed Reality 

[Microsoft Mixed Reality Toolkit](https://github.com/Microsoft/MixedRealityToolkit)

[Mixed Reality Academy](https://docs.microsoft.com/en-us/windows/mixed-reality/academy)

[Windows Dev Center for Mixed Reality](https://developer.microsoft.com/en-us/windows/mixed-reality/)

[Unity for VR and AR](https://unity3d.com/unity/features/multiplatform/vr-ar)

[Unity's Input Manager for Windows Mixed Reality motion controllers](https://docs.microsoft.com/en-us/windows/mixed-reality/gestures-and-motion-controllers-in-unity)

[Develop Mixed Reality Apps for Holographic Technology](https://www.microsoft.com/en-us/hololens/developers)

[Unity development overview for Windows Mixed Reality Apps](https://developer.microsoft.com/en-us/windows/mixed-reality/unity_development_overview)

[Windows Mixed Reality Developer Forum](https://forums.hololens.com/)

[Windows Mixed Reality Unity Forum](https://forum.unity.com/forums/windows-mixed-reality.102/)

Instructions:

1)	Pair your Xbox One S Wireless Controller to your HoloLens using the Bluetooth section of HoloLens Settings and following the instructions of your controller.

2)	Make sure your Unity WSA project has the following capabilities set:

		InternetClient
		
		HumanInterfaceDevice
		
3)	Set up the script you are going to use for input as follows.  (You can follow the example of the scene “ExampleScene” and the script “ControllerInputExample” to see how to use the code)

	a.	Add the using directive “using HoloLensXboxController;”
	
	b.	Add a private member “private ControllerInput controllerInput;”
	
	c.	Instantiate the controllerInput object in the Start() method:  ie “controllerInput = new ControllerInput(0, 0.19f);”.  The first parameter of the constructor is the number, starting at zero, of the controller you want to follow.  The second parameter is the default “dead” value; meaning all stick readings less than this value will be set to 0.0.
	
	d.	Make sure to call “controllerInput.Update();” in your MonoBehaviour Update() method.
	
4)	Build and deploy your application to HoloLens.

5)	Note:  these libraries will only handle Input on the HoloLens.  They will not handle input in the Unity Editor.  You will need to handle that separately.

# Unity Build Settings and VR Support for HoloLens
![virtualrealitysupported](https://user-images.githubusercontent.com/18353476/30458751-d69c5a12-9961-11e7-9c25-fb41c2864dce.png)
![unitybuildsettingscapabilities](https://user-images.githubusercontent.com/18353476/30458653-597be480-9961-11e7-9345-0bca4db2ba93.png)
