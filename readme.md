# Demo for Jetbrains Rider issue (RIDER-14289 Support ProjectReferences in WebSites)[https://youtrack.jetbrains.com/issue/RIDER-14289]

Repro steps:

- Setup website to run within IIS, external to IDE
- Change the text in ClassLibrary.Class.Text
- Build the class library (do not build the website).
- Reload the homepage in your browser

In Visual Studio, the newly compiled class library is automatically copied into the website bin folder and no compile of the website is necessary.

In Rider, the newly compiled DLL is not copied.
