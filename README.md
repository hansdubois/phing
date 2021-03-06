P     H     I     N     G
=========================


What is it?
-----------

  Phing is a PHP based build tool. In theory it is kind of like "make"
  without makes drawbacks and with the full portability and performance
  of PHP. (PH)pmake (I)s (N)ot (G)numake

Why?
----

  Why another build tool when there is already make, gnumake, nmake, jam, ant,
  and others? Because all those tools have limitations that the binarycloud
  development team could not live with when developing software across
  different platforms. Make-like tools are inherently shell-based: they
  evaluate a set of dependencies, then execute commands not unlike what you
  would issue on a shell.

  This means that you can easily extend these tools by using or writing any
  program for the OS that you are working on; however, this also means that
  you limit yourself to the OS, or at least the OS type, such as Unix, that
  you are working on.

  Makefiles are inherently evil as well. Anybody who has worked on them for
  any time has run into the dreaded tab problem. "Is my command not executing
  because I have a space in front of my tab?!!". Tools like Jam took care of
  this to a great degree, but still have yet another format to use and
  remember. Of course there is the Java based build tool ant, that is very
  good approach to what now Phing is. But still based on Java you have to have
  at least a running JRE installation on your plattfrom.
  Great for Java projects but we thought this is very consistent way to build
  a PHP based project. Additionally ant does not support a autoconf tool that
  writes out proper buildfiles based on some simple rules prior defined in a
  XML Configuration file.

  Phing is different. Instead of a model where it is extended with shell-based
  commands, Phing is extended using PHP classes. Instead of writing shell
  commands, the configuration files are XML-based, calling a target tree where
  various tasks get executed. Each task is run by an object that implements
  a particular Task action.

  Of course, this removes some of the expressive power that is inherent in
  being able to construct a shell command such as

    % `find . -name foo -exec rm {}`

  but it gives you the ability to be cross-platform - to work anywhere and
  everywhere. And if you really need to execute a shell command, Phing has an `<exec>`
  task that allows different commands to be executed based on the operating
  system it is executing on.

The Latest Version
------------------

  Details of the latest version can be found on the Phing homepage
  <http://phing.info/>.

Documentation
-------------

  Documentation is available in XHTML format in the docs/ directory. In particular,
  open the docs/phing_guide/book/index.html in a frames-compatible browser to see the
  phing user guide.

  For online documentation, you can also visit the Phing website: http://phing.info/

Licensing
---------

  This software is licensed under the terms you may find in the file
  named "LICENSE" in this directory.

  Thanks for using PHING.
