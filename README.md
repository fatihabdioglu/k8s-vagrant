# Kubernetes Vagrant Lab - Ubuntu

Bu proje, Vagrant kullanarak 3 Node'lu bir Kubernetes lab ortamı oluşturmanıza yardımcı olur. 

## Kurulum

1. **Vagrant ve VirtualBox Kurulumu:**
   - [Vagrant'ı indirin ve yükleyin](https://www.vagrantup.com/downloads).
   - [VirtualBox'ı indirin ve yükleyin](https://www.virtualbox.org/wiki/Downloads).

2. **Vagrant Konfigürasyonu:**
   - Bu proje dizinine gidin. 
```
   git clone https://github.com/fatihabdioglu/k8s-vagrant.git
   cd k8s-vagrant
```
   - `Vagrantfile` dosyasını inceleyin ve gerektiğinde değişiklikler yapın.

3. **Vagrant Ortamını Başlatma:**
   - Terminal veya Komut İstemi'nde aşağıdaki komutu çalıştırın.
```
    vagrant up
```
   - `vagrant status` komutuyla oluşan nodeları listeleyebilirsiniz
   - `vagrant ssh <node-name>` komutuyla oluşan nodelara ssh ile bağlanabilirsiniz.

4. **Vagrant Ortamını Kapatma:**
   - Terminalden `vagrant destroy -f` komutuyla oluşan sanal makine ve clusterları yokedebilirsiniz.

## Notlar

- `kubeadm/bootstrap.sh`, `kubeadm/init-master.sh`, ve `kubeadm/init-worker.sh` dosyalarını inceleyerek kurulum adımları hakkında daha fazla bilgi edinebilirsiniz.
- Calico veya Flannel cni seçmek için `Vagrantfile` dosyasında `pod_network_type` değişkenini güncelleyebilirsiniz.
