# Setting up LLVM
### Download all the files from GIT repo
```bash
sudo chown -R $(id -u):$(id -g) /mydata
cd /mydata
export MYMOUNT=/mydata
sudo git clone https://github.com/pperiucr/CS201Project.git
cd /mydata/CS201Project/
```

### Download and install LLVM
```bash
cd LLVM
sudo wget https://github.com/llvm/llvm-project/releases/download/llvmorg-12.0.1/llvm-12.0.1.src.tar.xz
sudo tar -xf llvm-12.0.1.src.tar.xz
sudo mv llvm-12.0.1.src llvm/
sudo wget https://github.com/llvm/llvm-project/releases/download/llvmorg-12.0.1/clang-12.0.1.src.tar.xz
sudo tar -xf clang-12.0.1.src.tar.xz
sudo mv clang-12.0.1.src clang/
```
