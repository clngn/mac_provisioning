# Mac環境構築

## 1. XCodeのインストール
手でほげほげやる。Command Line Toolsも入れる。

## 2. Homebrewのインストール
```bash
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## 3. Ansibleのインストール
```bash
$ brew install pyenv pyenv-virtualenv

$ PYTHON2_LATEST=`pyenv install -l | sed -e 's/^ *//' | grep -E '^2' | tail -n 1`
$ pyenv install $PYTHON2_LATEST
$ pyenv virtualenv $PYTHON2_LATEST py2

$ pyenv activate py2
$ pip install ansible
```

## 3. 残りを入れる
```bash
(py2)$ ansible-playbook -i hosts localhost.yml -vv
```
