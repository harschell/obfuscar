# obfuscar
Automatically exported from code.google.com/p/obfuscar

Obfuscar is a basic obfuscator for .NET assemblies. It uses massive overloading to rename metadata in .NET assemblies (including the names of methods, properties, events, fields, types and namespaces) to a minimal set, distinguishable in most cases only by signature.

For example, if a class contains only methods that accept different parameters, they can all be renamed 'A'. If another method is added to the class that accepts the same parameters as an existing method, it could be named 'a'.

It makes decompiled code very difficult to follow. The wiki has more details about WhatItDoes.

The current stable release is Obfuscar 1.5.4.

There is also the Obfuscar 2.0.0 Beta release. This is a port of Obfuscar 1.5.4 to the new Mono.Cecil 0.9 library. By use of this new library Obfuscar now supports .NET 4.0 assemblies. Because there are a lot of subtle changes in Cecil's new API this release of Obfuscar must be considered beta.

Note: Since version 1.5 the attrib attribute is evaluated correctly. Be sure to check if there are any unintended attrib values from the example in your configuration file.

Obfuscar works its magic with the help of Jb Evain's fantastic Cecil library, and uses the C5 Generic Collection Library to hold its data.
