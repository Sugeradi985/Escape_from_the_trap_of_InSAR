# Error in SAR image corregistration: Error: [Nodeld: CreateStack] org.jblas.NativeBlas.dgemm(CCIIID[DII[DIID[DII)V)

I have installed SNAP 8 in Ubuntu 18.04 and when I try to perform the co registration of a SAOCOM pair I get the same error "Error: [Nodeld: CreateStack] org.jblas.NativeBlas.dgemm(CCIIID[DII[DIID[DII)V)" despite I have installed libgfortran3 as is mentioned.

# To resolve:

'''shell
sudo apt-get update

sudo apt install libgfortran5
'''
