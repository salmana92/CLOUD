## Instalasi

(Jika pakai windows, bisa diinstall lewat [Cygwin](https://www.cygwin.com/) / [Baboon](http://babun.github.io/) / [WSL](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide))

Install [Vagrant](http://vagrantup.com/). Lalu install plugin `vagrant-env`

```shell
$ vagrant plugin install vagrant-env
```

Siapkan virtualenv untuk liur **HARUS** dengan `python3`

```shell
mkvirtualenv -p `which python3` liur
workon liur
```

Clone repo `liur` dan bikin `.env`

```shell
git clone git@github.com:jogjacamp/liur.git
cd liur
python setup.py develop
cp .env.example .env
```

Edit `.env`. Ganti `XS_PASSWORD` sesuai password xenserver

```bash
XS_PASSWORD="somethingstupidlikeiloveyou"
```

Install vagrant plugin `vagrant-xenserver`

```shell
vagrant plugin install scripts/vagrant-xenserver-0.0.14.gem
```

Setup project `liur`

```shell
$ liur setup.me
$ liur setup.infra
```

Provision semua server untuk Kazoo

```shell
$ liur nodes.up
```

Deploy kazoo

```shell
$ liur deploy
```