hadoop3x-eclipse-plugin
=======================

eclipse plugin for hadoop 3.x.x
 

How to build
----------------------------------------

 [hdpusr@demo hadoop2x-eclipse-plugin]$ cd src/contrib/eclipse-plugin 

 # Assume hadoop installation directory is /usr/share/hadoop

 [hdpusr@apclt eclipse-plugin]$ ant jar -Dversion=3.1.0 -Dhadoop.version=3.1.0 -Declipse.home=/opt/eclipse -Dhadoop.home=/usr/share/hadoop

final jar will be generated at directory 

  ${hadoop2x-eclipse-plugin}/build/contrib/eclipse-plugin/hadoop-eclipse-plugin-2.4.1.jar

  
release version included
-------------------------------------
 
  release/hadoop-eclipse-kepler-plugin-2.4.1.jar  # not tested yet
 
  release/hadoop-eclipse-kepler-plugin-2.2.0.jar  
  

options required
--------------------------------------
  version: plugin version
  
  hadoop.version:  hadoop version you want to compiled with

  eclipse.home: path of eclipse home 

  hadoop.home: path of hadoop 3.x home

 

How to debug
--------------------------------------
  start eclipse with debug parameter:  

    /opt/eclipse/eclipse -clean -consolelog -debug
    

Note: compile issues resolve: 
--------------------------------------
1. For different hadoop, adjust ${hadoop2x-eclipse-plugin-master}/ivy/libraries.properties, to match hadoop dependency lib version.
2. modify ${hadoop3x-eclipse}/src/contrib/eclipse-plugin/build.xml, in the node: <attribute name="Bundle-ClassPath" ....  to add the jar needed. 
3. For eclipse, do **not** use eclipse-inst, install eclipse **FULL VERSION(SDK)** instead.
