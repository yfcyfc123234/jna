Hacking on JNA with IntelliJ IDEA
======================================

The idea-jar target generates a jar that contains all the native bits needed by JNA.

Create a new module for JNA in Idea, mark the src folder as sources, testsrc as test sources.
Add a library to the module, include all jars from lib, lib/test and the idea-dispatch.jar generated by aforementioned ant target.

After this, you should be able to use JNA in your own code via this module, instead of including a JNA jar. This also speeds up development quite considerably, as you don't need to rebuild JNA jar between code changes.