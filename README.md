# SBT 0.13.8 and gen-sublime

Workaround is to edit _project/build.properties_ and use 0.13.7.

## Output:

```
sublime-scalap (master #)$ sbt
[info] Loading global plugins from /Users/richard/.sbt/0.13/plugins
[info] Updating {file:/Users/richard/.sbt/0.13/plugins/}global-plugins...
[info] Resolving org.fusesource.jansi#jansi;1.4 ...
[info] Done updating.
[info] Loading project definition from /Users/richard/tmp/sublime-scalap/project
[info] Updating {file:/Users/richard/tmp/sublime-scalap/project/}sublime-scalap-build...
[info] Resolving org.fusesource.jansi#jansi;1.4 ...
[info] Done updating.
[info] Set current project to sublime-scalap (in build file:/Users/richard/tmp/sublime-scalap/)
> gen-sublime
[info] Generating Sublime project for root directory: /Users/richard/tmp/sublime-scalap
[info] Getting dependency libraries sources transitively: false
[info] Saving external sources to: /Users/richard/tmp/sublime-scalap/target/External Libraries
[info] Updating {file:/Users/richard/tmp/sublime-scalap/}sublime-scalap...
[info] Resolving jline#jline;2.12 ...
[info] Done updating.
[info] Resolving jline#jline;2.12 ...
[info] Adding the following to external libraries:
[info]   scala-library-2.11.5-sources.jar
[info] Extracting jars to external sources directory
[info] Marking all files in sources directory as read-only
[info] Writing project to file: /Users/richard/tmp/sublime-scalap/sublime-scalap.sublime-project
java.lang.NoClassDefFoundError: scala/tools/scalap/scalax/rules/scalasig/ScalaSigSymbol
	at org.json4s.reflect.Reflector$ClassDescriptorBuilder$$anonfun$constructorsAndCompanion$3$$anonfun$13.apply(Reflector.scala:123)
	at org.json4s.reflect.Reflector$ClassDescriptorBuilder$$anonfun$constructorsAndCompanion$3$$anonfun$13.apply(Reflector.scala:122)
	at scala.collection.TraversableLike$$anonfun$map$1.apply(TraversableLike.scala:244)
	at scala.collection.TraversableLike$$anonfun$map$1.apply(TraversableLike.scala:244)
	at scala.collection.mutable.ResizableArray$class.foreach(ResizableArray.scala:59)
	at scala.collection.mutable.ArrayBuffer.foreach(ArrayBuffer.scala:47)
	at scala.collection.TraversableLike$class.map(TraversableLike.scala:244)
	at scala.collection.AbstractTraversable.map(Traversable.scala:105)
	at org.json4s.reflect.Reflector$ClassDescriptorBuilder$$anonfun$constructorsAndCompanion$3.apply(Reflector.scala:122)
	at org.json4s.reflect.Reflector$ClassDescriptorBuilder$$anonfun$constructorsAndCompanion$3.apply(Reflector.scala:116)
	at scala.collection.TraversableLike$$anonfun$map$1.apply(TraversableLike.scala:244)
	at scala.collection.TraversableLike$$anonfun$map$1.apply(TraversableLike.scala:244)
	at scala.collection.IndexedSeqOptimized$class.foreach(IndexedSeqOptimized.scala:33)
	at scala.collection.mutable.WrappedArray.foreach(WrappedArray.scala:34)
	at scala.collection.TraversableLike$class.map(TraversableLike.scala:244)
	at scala.collection.AbstractTraversable.map(Traversable.scala:105)
	at org.json4s.reflect.Reflector$ClassDescriptorBuilder.constructorsAndCompanion(Reflector.scala:116)
	at org.json4s.reflect.Reflector$ClassDescriptorBuilder.result(Reflector.scala:156)
	at org.json4s.reflect.Reflector$.createDescriptor(Reflector.scala:50)
	at org.json4s.reflect.Reflector$$anonfun$describe$1.apply(Reflector.scala:44)
	at org.json4s.reflect.Reflector$$anonfun$describe$1.apply(Reflector.scala:44)
	at org.json4s.reflect.package$Memo.apply(package.scala:39)
	at org.json4s.reflect.Reflector$.describe(Reflector.scala:44)
	at org.json4s.Extraction$.decomposeObject$1(Extraction.scala:91)
	at org.json4s.Extraction$.internalDecomposeWithBuilder(Extraction.scala:180)
	at org.json4s.Extraction$.decomposeWithBuilder(Extraction.scala:67)
	at org.json4s.Extraction$.decompose(Extraction.scala:194)
	at com.orrsella.sbtsublime.SublimeProject.toFile(SublimeProject.scala:37)
	at com.orrsella.sbtsublime.SublimePlugin$.doCommand(SublimePlugin.scala:116)
	at com.orrsella.sbtsublime.SublimePlugin$$anonfun$sublimeCommand$1.apply(SublimePlugin.scala:52)
	at com.orrsella.sbtsublime.SublimePlugin$$anonfun$sublimeCommand$1.apply(SublimePlugin.scala:52)
	at sbt.Command$$anonfun$command$1$$anonfun$apply$1.apply(Command.scala:29)
	at sbt.Command$$anonfun$command$1$$anonfun$apply$1.apply(Command.scala:29)
	at sbt.Command$.process(Command.scala:92)
	at sbt.MainLoop$$anonfun$1$$anonfun$apply$1.apply(MainLoop.scala:98)
	at sbt.MainLoop$$anonfun$1$$anonfun$apply$1.apply(MainLoop.scala:98)
	at sbt.State$$anon$1.process(State.scala:184)
	at sbt.MainLoop$$anonfun$1.apply(MainLoop.scala:98)
	at sbt.MainLoop$$anonfun$1.apply(MainLoop.scala:98)
	at sbt.ErrorHandling$.wideConvert(ErrorHandling.scala:17)
	at sbt.MainLoop$.next(MainLoop.scala:98)
	at sbt.MainLoop$.run(MainLoop.scala:91)
	at sbt.MainLoop$$anonfun$runWithNewLog$1.apply(MainLoop.scala:70)
	at sbt.MainLoop$$anonfun$runWithNewLog$1.apply(MainLoop.scala:65)
	at sbt.Using.apply(Using.scala:24)
	at sbt.MainLoop$.runWithNewLog(MainLoop.scala:65)
	at sbt.MainLoop$.runAndClearLast(MainLoop.scala:48)
	at sbt.MainLoop$.runLoggedLoop(MainLoop.scala:32)
	at sbt.MainLoop$.runLogged(MainLoop.scala:24)
	at sbt.StandardMain$.runManaged(Main.scala:53)
	at sbt.xMain.run(Main.scala:28)
	at xsbt.boot.Launch$$anonfun$run$1.apply(Launch.scala:109)
	at xsbt.boot.Launch$.withContextLoader(Launch.scala:128)
	at xsbt.boot.Launch$.run(Launch.scala:109)
	at xsbt.boot.Launch$$anonfun$apply$1.apply(Launch.scala:35)
	at xsbt.boot.Launch$.launch(Launch.scala:117)
	at xsbt.boot.Launch$.apply(Launch.scala:18)
	at xsbt.boot.Boot$.runImpl(Boot.scala:41)
	at xsbt.boot.Boot$.main(Boot.scala:17)
	at xsbt.boot.Boot.main(Boot.scala)
Caused by: java.lang.ClassNotFoundException: scala.tools.scalap.scalax.rules.scalasig.ScalaSigSymbol
	at java.net.URLClassLoader$1.run(URLClassLoader.java:372)
	at java.net.URLClassLoader$1.run(URLClassLoader.java:361)
	at java.security.AccessController.doPrivileged(Native Method)
	at java.net.URLClassLoader.findClass(URLClassLoader.java:360)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:424)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:357)
	at org.json4s.reflect.Reflector$ClassDescriptorBuilder$$anonfun$constructorsAndCompanion$3$$anonfun$13.apply(Reflector.scala:123)
	at org.json4s.reflect.Reflector$ClassDescriptorBuilder$$anonfun$constructorsAndCompanion$3$$anonfun$13.apply(Reflector.scala:122)
	at scala.collection.TraversableLike$$anonfun$map$1.apply(TraversableLike.scala:244)
	at scala.collection.TraversableLike$$anonfun$map$1.apply(TraversableLike.scala:244)
	at scala.collection.mutable.ResizableArray$class.foreach(ResizableArray.scala:59)
	at scala.collection.mutable.ArrayBuffer.foreach(ArrayBuffer.scala:47)
	at scala.collection.TraversableLike$class.map(TraversableLike.scala:244)
	at scala.collection.AbstractTraversable.map(Traversable.scala:105)
	at org.json4s.reflect.Reflector$ClassDescriptorBuilder$$anonfun$constructorsAndCompanion$3.apply(Reflector.scala:122)
	at org.json4s.reflect.Reflector$ClassDescriptorBuilder$$anonfun$constructorsAndCompanion$3.apply(Reflector.scala:116)
	at scala.collection.TraversableLike$$anonfun$map$1.apply(TraversableLike.scala:244)
	at scala.collection.TraversableLike$$anonfun$map$1.apply(TraversableLike.scala:244)
	at scala.collection.IndexedSeqOptimized$class.foreach(IndexedSeqOptimized.scala:33)
	at scala.collection.mutable.WrappedArray.foreach(WrappedArray.scala:34)
	at scala.collection.TraversableLike$class.map(TraversableLike.scala:244)
	at scala.collection.AbstractTraversable.map(Traversable.scala:105)
	at org.json4s.reflect.Reflector$ClassDescriptorBuilder.constructorsAndCompanion(Reflector.scala:116)
	at org.json4s.reflect.Reflector$ClassDescriptorBuilder.result(Reflector.scala:156)
	at org.json4s.reflect.Reflector$.createDescriptor(Reflector.scala:50)
	at org.json4s.reflect.Reflector$$anonfun$describe$1.apply(Reflector.scala:44)
	at org.json4s.reflect.Reflector$$anonfun$describe$1.apply(Reflector.scala:44)
	at org.json4s.reflect.package$Memo.apply(package.scala:39)
	at org.json4s.reflect.Reflector$.describe(Reflector.scala:44)
	at org.json4s.Extraction$.decomposeObject$1(Extraction.scala:91)
	at org.json4s.Extraction$.internalDecomposeWithBuilder(Extraction.scala:180)
	at org.json4s.Extraction$.decomposeWithBuilder(Extraction.scala:67)
	at org.json4s.Extraction$.decompose(Extraction.scala:194)
	at com.orrsella.sbtsublime.SublimeProject.toFile(SublimeProject.scala:37)
	at com.orrsella.sbtsublime.SublimePlugin$.doCommand(SublimePlugin.scala:116)
	at com.orrsella.sbtsublime.SublimePlugin$$anonfun$sublimeCommand$1.apply(SublimePlugin.scala:52)
	at com.orrsella.sbtsublime.SublimePlugin$$anonfun$sublimeCommand$1.apply(SublimePlugin.scala:52)
	at sbt.Command$$anonfun$command$1$$anonfun$apply$1.apply(Command.scala:29)
	at sbt.Command$$anonfun$command$1$$anonfun$apply$1.apply(Command.scala:29)
	at sbt.Command$.process(Command.scala:92)
	at sbt.MainLoop$$anonfun$1$$anonfun$apply$1.apply(MainLoop.scala:98)
	at sbt.MainLoop$$anonfun$1$$anonfun$apply$1.apply(MainLoop.scala:98)
	at sbt.State$$anon$1.process(State.scala:184)
	at sbt.MainLoop$$anonfun$1.apply(MainLoop.scala:98)
	at sbt.MainLoop$$anonfun$1.apply(MainLoop.scala:98)
	at sbt.ErrorHandling$.wideConvert(ErrorHandling.scala:17)
	at sbt.MainLoop$.next(MainLoop.scala:98)
	at sbt.MainLoop$.run(MainLoop.scala:91)
	at sbt.MainLoop$$anonfun$runWithNewLog$1.apply(MainLoop.scala:70)
	at sbt.MainLoop$$anonfun$runWithNewLog$1.apply(MainLoop.scala:65)
	at sbt.Using.apply(Using.scala:24)
	at sbt.MainLoop$.runWithNewLog(MainLoop.scala:65)
	at sbt.MainLoop$.runAndClearLast(MainLoop.scala:48)
	at sbt.MainLoop$.runLoggedLoop(MainLoop.scala:32)
	at sbt.MainLoop$.runLogged(MainLoop.scala:24)
	at sbt.StandardMain$.runManaged(Main.scala:53)
	at sbt.xMain.run(Main.scala:28)
	at xsbt.boot.Launch$$anonfun$run$1.apply(Launch.scala:109)
	at xsbt.boot.Launch$.withContextLoader(Launch.scala:128)
	at xsbt.boot.Launch$.run(Launch.scala:109)
	at xsbt.boot.Launch$$anonfun$apply$1.apply(Launch.scala:35)
	at xsbt.boot.Launch$.launch(Launch.scala:117)
	at xsbt.boot.Launch$.apply(Launch.scala:18)
	at xsbt.boot.Boot$.runImpl(Boot.scala:41)
	at xsbt.boot.Boot$.main(Boot.scala:17)
	at xsbt.boot.Boot.main(Boot.scala)
[error] java.lang.NoClassDefFoundError: scala/tools/scalap/scalax/rules/scalasig/ScalaSigSymbol
[error] Use 'last' for the full log.
```

## Additional local info

```
$ cat ~/.sbt/0.13/global.sbt
resolvers += "Type" at "http://repo.typesafe.com/typesafe/maven-releases"

$ cat ~/.sbt/0.13/plugins/build.sbt
addSbtPlugin("com.orrsella" % "sbt-sublime" % "1.0.9")

//addSbtPlugin("net.virtual-void" % "sbt-dependency-graph" % "0.7.4")

addSbtPlugin("com.typesafe.sbt" % "sbt-pgp" % "0.8.1")

addSbtPlugin("com.typesafe.sbteclipse" % "sbteclipse-plugin" % "2.5.0")

addSbtPlugin("com.github.mpeltonen" % "sbt-idea" % "1.6.0")
```


