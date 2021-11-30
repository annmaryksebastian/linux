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


------------------------------------------------------------------------------------------------------------------------------------------------------------------


# CMPE 283 Assignment-3
## Completed by two members:
### Ashwin Kumar (015273258)
### Annmary K Sebastian (015215928)

### Member Contribution

We both took the already built kernel for Assignment-1 and made changes to it.

#### Ashwin's Contribution:
I analyzed the SDM Manual and figured out the exit reasons that are defined and also configured in KVM. Made Code changes into the cpuid.c file and vmx.c file for the EAX value 0x4FFFFFFD. Compiled the Kernel and loaded it using the following commands.
1. make -j 8 modules
2. make INSTALL_MOD_STRIP=1 modules_install
3. lsmod | grep kvm
4. rmmod kvm_intel
5. rmmod kvm
6. lsmod | grep kvm
7. modprobe kvm
8. modprobe kvm_intel
9. lsmod | grep kvm

Started the virtual machine (inner vm) and ran the test file to check the output.

#### Annmary's Contribution:

Made Code changes into the cpuid.c file and vmx.c file for the EAX value 0x4FFFFFFC. Compiled the Kernel and loaded it using the following commands.
1. make -j 8 modules
2. make INSTALL_MOD_STRIP=1 modules_install
3. rmmod kvm_intel
4. rmmod kvm
5. lsmod | grep kvm
6. modprobe kvm
7. modprobe kvm_intel
8. lsmod | grep kvm
9.Then started the inner vm virtual machine and ran the test file to check the output.

## Answers for 3 and 4
<pre>
3:
Exit counts greater than 0 were observed for exit codes: 0, 10, 28, 29, 30, 31, 40, 46, 47, 48, 54 and 55.
For exit codes 28, 29, 46, 47, 54 and 55 the count increased at a stable rate only during reboot operation.
For the remaining exit codes the counts increased to higher value during reboot operation, whereas it increased
with a lower value for normal operations such as file creation and deletion etc. From the output pattern mentioned below,
it was observed that, there were nearly 1.5 million exits during a reboot operation

4:
Most frequent exit types are: 0, 10, 30, 31, 40, 48 and 28.
Least frequent exit types are: 29, 46, 47, 54, and 55. 
</pre>

## Output Pattern Observed for different exit types:
<pre>
Exit Type       FIRST_Start,     Reboot,       Create File,     Delete File,     Reboot

1. 0:             16126,         32979,           32990,         32994,         49797
2. 10:            140278,       280327,          284362,        285115,        423010
3. 28:            31931,         64163,           64163,         64163,         95909
4. 29:               2,              4,               4,             4,            6
5. 30:            200658,       407978,          420884,        433471,        637408
6. 31:              934,          2947,           4840,         6073,          8016
7. 40:             1818,          3701,           11692,        12573,         14373
8. 46:               7,             14,             14,          14,             21
9. 47:               3,              6,              6,           6,              9
10. 48:             1033570,     200451,          2313123,     2346078,       3526212
11. 54:                3,             6,               6,          6,             9
12. 55:                3,             6,               6,          6,             9
</pre>

## Output Screenshots

![image](https://user-images.githubusercontent.com/78461249/143988917-13fdf416-83f5-4486-aa57-5a5c0308c971.png)

![image](https://user-images.githubusercontent.com/78461249/143988929-9b8273d6-43a2-4651-92e1-5f26fcadbf6e.png)

![image](https://user-images.githubusercontent.com/78461249/143988960-6b0e214a-9a19-4eaa-a453-99004f5aa0f8.png)

![image](https://user-images.githubusercontent.com/78461249/143988985-2fe9333f-6884-4de1-a307-e548df4970ab.png)

![image](https://user-images.githubusercontent.com/78461249/143989016-4b606d84-512c-4569-86a0-8d4cd793cac3.png)

![image](https://user-images.githubusercontent.com/78461249/143989029-fa979ec1-c3fb-427e-893d-5719593bb48a.png)

![image](https://user-images.githubusercontent.com/78461249/143989048-6ef42735-c5af-47b7-ad19-42ef9c8c6f96.png)

![image](https://user-images.githubusercontent.com/78461249/143989065-08215aca-f4b8-4656-9881-67eb43ebeb9f.png)

![image](https://user-images.githubusercontent.com/78461249/143989091-6cfebb4a-f68a-42ef-acc9-fec83bbc8f05.png)

![image](https://user-images.githubusercontent.com/78461249/143989116-92e91766-e8c4-44a1-91a5-e7cd8e04d372.png)

</pre>
