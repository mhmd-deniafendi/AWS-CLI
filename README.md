# AWS-CLI
Cheat Sheet AWS CLI
Sedikit Catatan tentang AWS CLI. Pada repo ini menjunkan bagaimana kita login ke AWS CLI dan login ke EKS yang sudah mengaktifkan MFA menggunakan cmd di windows

### Pre-reqruisite
1. Sudah menginstall AWS CLI di windows
2. Memiliki akun di AWS dan sudah menyimpan untuk Accesskey Id dan Secretkey Id
3. Sudah menginstall aplikasi Authy di laptop atau handphone

### 1. Mennggunakan CMD di windows

```
$ aws configure
```

![image](https://user-images.githubusercontent.com/80587939/131803089-fd3325ca-62cc-4ea0-b9a0-2e546b55bd1e.png)
### 2. Masukan Access Key ID dan Secret Access Key

### 3. Masukan command berikut untuk login menggunakan MFA

```
$ aws sts get-session-token --serial-number arn:aws:iam::your_arn:mfa/yourusername --token-code yourtokencodefromauthy
```

dan command diatas akan memunculkan output seperti gambar dibawah ini
![image](https://user-images.githubusercontent.com/80587939/131801525-f2ef06c9-0867-4b5e-96cd-fb0816ec98ab.png)

## Masukan kembali Access Key ID dan Secret Key menggunakan pada langkah no 3

```
$ aws configure
```
