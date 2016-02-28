##  Tool - O2 Cmd SpringMVC v1.0.exe - as standalone exe 

I just had a request  for the O2's Spring MVC module (developed ages ago), and It was was a good opportunity to test the latest version of the '_O2 Standalone tool builde_r', since it now supports the embedding of the tools installed via an O2 Script (usually stored in the _ToolsOrApis folder).

You can download the [Tool - O2 Cmd SpringMVC v1.0.exe](https://dl.dropbox.com/u/81532342/O2Platform%20Tools/Spring%20MVC/Tool%20-%20O2%20Cmd%20SpringMVC%20v1.0.exe) (or build it using O2) which is the stand alone exe of the old **_O2_Cmd_SpringMvc.ms_**_i_ tool (See at the end of this post for details on how this exe was created)

  


[![](images/CropperCapture_5B68_5D.jpg)](http://4.bp.blogspot.com/-srum-XVFs0s/UIpaHVxtmUI/AAAAAAAAAsI/5yaNQzjeI30/s1600/CropperCapture%5B68%5D.jpg)

  
When you open this tool, you will get a GUI that looks like this:

[![](images/CropperCapture_5B69_5D.jpg)](http://3.bp.blogspot.com/-3SGL4TXm7Og/UIpcFRlpusI/AAAAAAAAAsQ/xTwj7a-MgX8/s1600/CropperCapture%5B69%5D.jpg)

  
Then if you drop a jar (or the zip of *.classes like the one you will find in the [jPetClinic -- O2 Demo Pack.zip](http://s3.amazonaws.com/Demo_Files/jPetClinic%20-%20O2%20Demo%20Pack.zip)  that you get from the [Packaged Spring MVC Security Test Apps: JPetStore and PetClinc](http://o2platform.wordpress.com/2011/07/18/packaged-spring-mvc-security-test-apps-jpetstore-and-petclinc/) ), a series of conversions will occur (Jython is used to parse the java byte code) :  


  


  


[![](images/CropperCapture_5B71_5D.jpg)](http://3.bp.blogspot.com/-wgaz45sXy_c/UIpcHPR9Z0I/AAAAAAAAAsg/znZJrFbsFfs/s1600/CropperCapture%5B71%5D.jpg)

  
Which when finished will look like this:

[![](images/CropperCapture_5B73_5D.jpg)](http://1.bp.blogspot.com/-BfXe7lXGfMQ/UIpcJdAxgCI/AAAAAAAAAss/8DWoSZgWRhA/s1600/CropperCapture%5B73%5D.jpg)

  
For a detailed explanation of how this module works (including the VERY important **_/*O2Helper:MVCAutoBindListObject_**: hack) take a look at this blog post:  
[Visualizing Spring MVC Annotations based Controls (and Autobinding PetClinic's vulnerabilities)](http://o2platform.wordpress.com/2011/07/19/visualizing-spring-mvc-annotations-based-controls-and-autobinding-petclinics-vulnerabilities/)

[![](images/CropperCapture_5B74_5D.jpg)](http://3.bp.blogspot.com/-CgYwwhoLv6Y/UIpe8OOgLhI/AAAAAAAAAtY/2trw41exaT4/s1600/CropperCapture%5B74%5D.jpg)

  


  


## How the [Tool - O2 Cmd SpringMVC v1.0.exe](https://dl.dropbox.com/u/81532342/O2Platform%20Tools/Spring%20MVC/Tool%20-%20O2%20Cmd%20SpringMVC%20v1.0.exe)  was created

It was quite easy to package the O2_Cmd_SpringMvc.msi tool (note-to-self: do this for the other really powerful old O2 tools that are gathering dust in the O2 archives)

  


**Step 1: Create an installer that downloads and extracts the msi:**

**  
**

[![](images/CropperCapture_5B76_5D.jpg)](http://3.bp.blogspot.com/-UYMKI1p7BLE/UIpgHtpXwOI/AAAAAAAAAto/PG6D3QQdImw/s1600/CropperCapture%5B76%5D.jpg)

  


**Step 2: In an O2 C# REPL script create the_ Tool - O2 Cmd SpringMVC.h2_ file**

  


Which will consume the installers (shown above) and will trigger the extraction (when executed for the first time as a standalone exe)

  


[![](images/CropperCapture_5B77_5D.jpg)](http://2.bp.blogspot.com/-NEHfpQ9CiIY/UIpgt75NlSI/AAAAAAAAAtw/pU1ehYQ8sJ8/s1600/CropperCapture%5B77%5D.jpg)

  


**Step 3: Open the context menu and chose the item to package the current script**

  


[![](images/CropperCapture_5B80_5D.jpg)](http://2.bp.blogspot.com/-DwkNFvGxoWk/UIpiBO13jyI/AAAAAAAAAt4/5rkm1g_suss/s1600/CropperCapture%5B80%5D.jpg)

  
And that's it!

The package tool (which is a script it self) should be open with the created exe:

[![](images/CropperCapture_5B81_5D.jpg)](http://4.bp.blogspot.com/-2p87z0Md3qc/UIpia9h0gJI/AAAAAAAAAuA/7URqioegS2w/s1600/CropperCapture%5B81%5D.jpg)

  
It's quite powerful the fact that it took me longer to write this blog post than to package that old O2 tool  :)
