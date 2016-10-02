# AndroidCryptoHookPlugin

This plugin uses the JEB debugger API to monitor the use of cryptographic primitives in a running Android application, specifically the methods in the `Cipher` abstract class. This plugin is intended as proof-of-concept code show-casing what can be done with the `IDebuggerUnit` et al. set of interfaces.

Note that this plugin can be used with any client, such as the official UI RCP client, or a headless client.

How to use as a stand-alone Jar plugin:

- Navigate to the `build/` folder
- Build the plugin using Ant: `ant -file build-andhook.xml -Dversion=1.0.0 clean build package`
- Copy to your JEB `coreplugins/` folder and start JEB

How to use in a development environment, via the RCP desktop client:

- Set the plugin's *.class files folder and class name in the Development tab of the Options dialog
- Restart JEB
- Open an APK
- Start a debugging session, then run the plugin (via *File, Engines* menu.)
