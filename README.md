# Nexus-Kurulum

- Makinamızda docker yüklü olması gerekiyor.
```
sudo apt update
sudo apt install docker.io
sudo apt install docker-compose
```
- Nexus klasörümüzün içerisine giriyoruz. (Docker-compose. yaml olduğu yer.)
```
docker-compose up -d
```

- Nexusa erişim için ``makina-ip:8081`` kullanıyoruz.
- Erişimde sıkıntı yaşarsak açılmama durumu olursa genellikle permission hatasından kaynaklı olabilir. Bunun için yetki vermemiz gerekiyor. 
```
sudo chown -R 200:200 /data/nexus-data
```
- Bu adımdan sonra docker'i tekrar down-up  yapmamız gerekiyor.
```
docker-compose down
docker-compose up -d
```
