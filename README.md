# DDK_How_To_Build_EDK2
To introduce how to build edk2 on Ubuntu.

# Environment
1.Ubuntu 20.04.4 LTS

# Let us get started 
Download some required packages before we start to build. </br>
```sh
sudo apt install -y build-essential uuid-dev acpica-tools nasm python3.8 python3-distutils python3-pip gawk bc git 
```

commit 970e26294905d2d27369cf4041c6778105754f5e (HEAD -> master, origin/master, origin/HEAD) </br>
```sh
git clone https://github.com/tianocore/edk2.git
```

```sh
source edksetup.sh
```
![Screen Shot 2022-09-11 at 2 09 46 AM](https://user-images.githubusercontent.com/67073582/189497221-1f456336-b03b-48e0-9356-7817d6b57da3.png)

The commands below are needed, or we may have some issues, such as "./brotli/c/common/constants.h: No such file or directory".
```sh
git submodule init && git submodule update
```
![Screen Shot 2022-09-11 at 2 23 07 AM](https://user-images.githubusercontent.com/67073582/189497254-687608ca-baea-41b0-8728-785dba3194fc.png)
![Screen Shot 2022-09-11 at 2 26 14 AM](https://user-images.githubusercontent.com/67073582/189497263-b829e837-bf06-443e-a217-659e32868fcc.png)

```sh
make -C BaseTools/
```
![Screen Shot 2022-09-11 at 2 27 11 AM](https://user-images.githubusercontent.com/67073582/189497272-91b44b89-c930-415b-a2ca-3618e54620ff.png)

# References
1. https://github.com/tianocore/edk2
2. https://github.com/tianocore/tianocore.github.io/wiki/Getting-Started-with-EDK-II
3. ...
