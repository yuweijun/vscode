## visual studio code personal config files

1. settings.json
2. keybindings.json
3. java.json

## java test case 输出的中文在output中显示乱码

解决方法如下：

    $ export LC_ALL=en_US.UTF-8
    $ code
 
再重新打开vscode运行测试用例，可以看到输出已经正常了。

## Use terminal as a login shell by default

This is happening because we don't run the integrated terminal as a login shell by default. You will need to add the following to launch bash as a login shell:

    // macOS:
    "terminal.integrated.shellArgs.osx": [ "-l" ]
    // Linux
    "terminal.integrated.shellArgs.linux": [ "-l" ]
    
You could also solve this by moving the relevant parts of your ~/.bash_profile to your ~/.bashrc file which is run for non-login shells.
