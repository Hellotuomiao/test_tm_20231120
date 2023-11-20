# Linux中git的使用

## 编译

	export ARMGCC_DIR=/home/peong/wplace/gcc-arm-none-eabi-9-2019-q4-major
这个指令是在Linux系统下设置一个环境变量，将ARM GCC（GNU Compiler Collection）的安装目录指定为/home/peong/wplace/gcc-arm-none-eabi-9-2019-q4-major。

具体来说，这个环境变量ARMGCC_DIR被设置为指定的目录路径。这个目录似乎包含了 ARM 架构的嵌入式系统开发所需的工具链（toolchain），其中包括编译器、汇编器、链接器等等。通过设置这个环境变量，你可以告诉系统在执行一些需要 ARM GCC 的操作时去寻找这个特定的目录。

在使用 Git 的上下文中，这样设置环境变量可能是因为你的项目中使用了 ARM 架构，并且需要使用特定版本的 ARM GCC 工具链进行编译和构建。

```c
export PATH=$PATH:/home/peong/wplace/gcc-arm-none-eabi-9-2019-q4-major
```
这个命令是将 ARM GCC 工具链的二进制文件目录添加到系统的 PATH 环境变量中。通过这个设置，系统就能够在命令行中找到 ARM GCC 工具链的可执行文件，而不需要提供完整的路径。

具体而言：

export PATH 表示要对环境变量 PATH 进行设置。
$PATH 是当前 PATH 变量的值，通过这种方式保留了原有的 PATH 设置。
:/home/peong/wplace/gcc-arm-none-eabi-9-2019-q4-major 是要追加到 PATH 中的新路径，这里是 ARM GCC 工具链的二进制文件目录。
因此，通过这个命令，系统将会在搜索可执行文件时包括/home/peong/wplace/gcc-arm-none-eabi-9-2019-q4-major这个路径，从而可以直接在命令行中运行 ARM GCC 工具链的命令，而不需要输入完整的路径。这对于在命令行中方便地使用 ARM GCC 工具链是很有用的。
	
	cd boards/evkmimx8mp/
	
	cd boards/evkmimx8mp/multicore_examples/XT_Panel/armgcc/
	
	./build_debug.sh 

## 修改

```c
git commit -m "fix : main log error."
```

```c
git push  origin rpmsg 
```





