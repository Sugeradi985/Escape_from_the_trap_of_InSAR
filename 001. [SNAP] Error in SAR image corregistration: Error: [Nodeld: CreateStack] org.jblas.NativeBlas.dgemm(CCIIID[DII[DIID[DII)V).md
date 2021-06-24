# Error in SAR image corregistration: Error: [Nodeld: CreateStack] org.jblas.NativeBlas.dgemm(CCIIID[DII[DIID[DII)V)
# SNAP软件只在Linux平台出现这样的报错，在进行TOPS配准操作（BackCoding）时出现。
I have installed SNAP 8 in Ubuntu 18.04 and when I try to perform the co registration of a SAOCOM pair I get the same error "Error: [Nodeld: CreateStack] org.jblas.NativeBlas.dgemm(CCIIID[DII[DIID[DII)V)" despite I have installed libgfortran3 as is mentioned.

# To resolve:

```shell
sudo apt-get update

sudo apt install libgfortran5
```
