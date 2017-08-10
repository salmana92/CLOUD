## Instalasi

(Jika pakai windows, bisa diinstall lewat cygwin / Baboon / WSL)

1. Install Vagrant. Lalu install plugin vagrant-env

$ vagrant plugin install vagrant-env

2. Siapkan virtualenv untuk liur HARUS dengan python3

mkvirtualenv -p `which python3` liur
workon liur

3. Clone repo liur dan bikin .env

git clone git@github.com:jogjacamp/liur.git
cd liur
python setup.py develop
cp .env.example .env

4. Edit .env. Ganti XS_PASSWORD sesuai password xenserver

XS_PASSWORD="somethingstupidlikeiloveyou"

5. Install vagrant plugin vagrant-xenserver

vagrant plugin install scripts/vagrant-xenserver-0.0.14.gem

6. Setup project liur

$ liur setup.me
$ liur setup.infra

7. Provision semua server untuk Kazoo

$ liur nodes.up

8. Deploy kazoo

$ liur deploy