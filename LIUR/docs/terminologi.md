## Terminologi

Dalam rangka mengikuti tata kelola pengembangan aplikasi yang baik, liur menggunakan 3 environment (dev, staging, prod) dimana pada setiap environment dilakukan testing supaya meminimalisir error.

### Dev Environment

Adalah environment awal dalam pengembangan, biasanya ada di workstation atau laptop pengembang aplikasi

### Staging Environment

Adalah environment diatas dev, dimana setelah pengembang aplikasi melakukan perubahan apapun, bisa dicoba dalam environment ini. Disini hypervisor menggunakan Xenserver dibantu oleh vagrant sebagai aplikasi bantu dalam deployment dan provisioning.

### Produksi Environment

Adalah environment utama yang dimana end user menggunakannya. Disini service yang berjalan sudah harus HA (High Availability), sehingga hypervisor Xenserver akan diiringi dengan openstack untuk orkestrasi dari seluruh komponen kazoo.