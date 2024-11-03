# Setting up LLVM
### Download all the files from GIT repo
```bash
sudo chown -R $(id -u):$(id -g) /mydata
cd /mydata
export MYMOUNT=/mydata
sudo git clone https://github.com/pperiucr/CS201Project.git
cd /mydata/CS201Project/
sudo unzip ./CS201-F24-Template-1.zip
cd /mydata/CS201Project/CS201-F24-Template
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

###  Build LLVM and Clang:
```bash
sudo mkdir build
sudo mkdir install
cd build
sudo cmake -G "Unix Makefiles" -DLLVM_ENABLE_PROJECTS=clang -DCMAKE_INSTALL_PREFIX=../install -DCMAKE_BUILD_TYPE=Release ../llvm
sudo make -j 8 install
clang --version
opt -version
```
