---
autogenerated: true
title: Using IntelliJ
layout: page
---

The following instructions for debugging Micro-Manager's Java code with
IntelliJ are intended to work on Windows or Mac. Updated for 2.0-gamma

(See also: [Writing plugins for
Micro-Manager](Writing_plugins_for_Micro-Manager "wikilink"))

1.  Download and install a recent Micro-Manager nightly build. We will
    refer to the installed Micro-Manager directory as `$INSTALLDIR`
    below.

<!-- -->

1.  Use git to clone the micro-manager source code
    [1](https://github.com/micro-manager/micro-manager). We'll refer to
    the root source directory as `$SRCDIR` below.&lt;!--

--&gt;

1.  Download, install and run [IntelliJ Community
    Edition](https://www.jetbrains.com/idea/download). You may also need
    to download a JDK from [AdoptOpenJDK](https://adoptopenjdk.net/).
    Micro-Manager is currently developed with JDK 8 (Java Development
    Kit 1.8).

<!-- -->

1.  Choose **Create New Project**

<!-- -->

1.  Name the Project (i.e. Micro-Manager2), and select the JDK (11 may
    work, but MM is developed with JDK8).

<!-- -->

1.  Select the project and right click and find "Open Module Settings
    (F4)".

<!-- -->

1.  Click on "Add Content Root". From `$SRCDIR` select
    **mmstudio/src/main/java** and **mmstudio/src/main/resources**

<!-- -->

1.  In the Project Settings dialog, select "Libraries". Use the "+"
    button in the second column to add libraries. If you have ant
    installed and ran *'ant -f buildscripts\\fetchdeps.xml* before, add
    `$SRCDIR/dependencies/artifacts/imagej`,
    `$SRCDIR/dependencies/artifacts/compile`. If you did not, you can
    try adding the plugins/micro-manager directory of your micro-manager
    installation. You will also need to supply MMAcqEngine.jar and
    MMCoreJ.jar, which you either build yourself, or that can be found
    in `$INSTALLDIR/polugins/micro-manager`. Click "OK"

<!-- -->

1.  in the IntelliJ menu, select Run &gt; Edit Configurations. Add new
    Configuration, type "Application".

\#\* **Main Class:** type in `ij.ImageJ`

\#\* **VM options:** type in `-Xmx3000M`. This sets the maximum memory
(megabytes) used by Java .Also add `-Dforce.annotation.index=true`.

\#\* **Working Directory:** type in your `$INSTALLDIR`

1.  You should now be able to Run and Debug the code.

<INCLUDE Note text="'''Explanation of the  <code>-Dforce.annotation.index</code> option''': Micro-Manager uses Scijava plugins for many of its internal components. In order for plugins to be detected at runtime it is important that the annotation processor is enabled.The <code>-Dforce.annotation.index</code> option will attempt to force to processor to be enabled. Optionally, you could also go to "settings->Build,Execution,Deployment-\>Annotation
Processors" and make sure that "Enable annotation processing" is
checked. If you find that the program crashes with a
\`NullPointerException\` on startup you may have forgotten to enable
annotation processing.😎"\>

{% include Note text="The components from the installed Micro-Manager can get out of sync with the source code. If you encounter unexpected errors, update to the latest nightly build and the latest source revision." %}
