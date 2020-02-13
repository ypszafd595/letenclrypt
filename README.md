# LetEncrypt
## setup pyenv
run yum command
```bash
sudo yum -y install gcc zlib-devel bzip2 bzip2-devel readline readline-devel \
 git openssl openssl-devel python2-pip libffi-devel
```
download pyenv
```
grep PYENV_ROOT ~/.bashrc > /dev/null 2>&1
if [ $? -eq 1 ]; then
  git clone https://github.com/pyenv/pyenv.git ~/.pyenv
cat >> ~/.bashrc << PYENV

#-----------------
export PYENV_ROOT="\$HOME/.pyenv"
export PATH="\$PYENV_ROOT/bin:\$PATH"
eval "\$(pyenv init -)"
PYENV
fi

source ~/.bashrc
```
install python3 on pyenv
```
pyenv insatll 3.7.6
```
create ur working directory
```bash
mkdir -p /ANY/PATH
cd $_
```
set python version on ur working directory.
```bash
pyenv local 3.7.6
```
run pip command.
```
pip install --upgrade pip
pip install virtualenv
```
create virtualenv directory
```
virtualenv 3.7.6
cd 3.7.6
```
run pip command
```
source ./bin/activate
pip install --upgrade pip
pip install ansible
```
git clone
```
git clone https://github.com/ypszafd595/letencrypt.git
cd letencrypt
```