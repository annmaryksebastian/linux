# CMPE 283 Assignment-2
## Completed by two members:
### Ashwin Kumar (015273258)
### Annmary K Sebastian (015215928)

### Member Contribution

#### Annmary's Contribution:
I made the code changes relevant for this assignment in the files cpuid.c and vmx.c. Then compiled the kernel using the following command
1. make -j 8 modules
2. make INSTALL_MOD_STRIP=1 modules_install
3. rmmod kvm_intel
4. rmmod kvm
5. modprobe kvm
6. modprobe kvm_intel

After this, I started the virutal machine(inner vm) and ran the test file to check the output.

#### Ashwin's Contribution:
I cloned the git repository and started the terminal inside linux directory and ran the following commands to make the linux kernel ready:
1. cp /boot/config-$(uname -r) .config
2. make oldconfig
3. make -j 8 modules_install'
4. make
5. make install

After this I installed the virtual machine manager and started ubuntu20.04 OS in the inner vm.

## Output Screenshots

![image](https://user-images.githubusercontent.com/78461249/142982642-66e849be-e7d5-46a9-8491-a56449113f78.png)

![image](https://user-images.githubusercontent.com/78461249/142982791-3bd8a30c-0b99-4392-ace0-b2704e7b2e41.png)


