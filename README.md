# Discord Lookup

Discord kullanıcıları hakkında bilgi almanızı sağlayan basit ve etkili bir araç.

## Kurulum

Modülü projenize eklemek için npm veya yarn paket yöneticisini kullanabilirsiniz.

```bash
npm install discord-lookup
```
veya
```bash
yarn add discord-lookup
```

## Kullanım
Aşağıda, `discord-lookup` modülünün nasıl kullanılacağını gösteren bazı örnekler bulunmaktadır.

### Modülü İçe Aktarma
Öncelikle modülü projenizde içe aktarın:
```javascript
const { Lookup } = require('discord-lookup');
```

### Kullanıcı Bilgisi Alma
Belirli bir kullanıcı hakkında bilgi almak için:
```javascript
const userInfo = Lookup.getUser(userID);
console.log(userInfo);
```

### Sunucu Listesini Alma
Kullanıcının üye olduğu sunucuları listelemek için:
```javascript
const serverNames = Lookup.getServerList(userID);
console.log(serverNames);
```

### İsim Listeleme
Kullanıcının daha önce kullandığı isimleri almak için:
```javascript
const nameList = Lookup.getNameList(userID);
console.log(nameList);
```

### İsim ve Yaş Listeleme
Kullanıcının kullandığı isimler ve yaşları hakkında bilgi almak için:
```javascript
const nameAndAgeList = Lookup.getNameAndAgeList(userID);
console.log(nameAndAgeList);
```

### Cinsiyet Listeleme
Kullanıcının cinsiyet bilgilerini almak için:
```javascript
const sexList = Lookup.getSex(userID);
console.log(sexList);
```

### Son Mesaj ve Ses Durumu
Kullanıcının en son çevrimiçi olduğu zaman ve ses durumu hakkında bilgi almak için:
```javascript
const lastSeen = Lookup.getLastSeen(userID);
console.log(lastSeen);
```

## Örnek Kullanım
Tüm işlevlerin bir arada nasıl kullanılacağını gösteren basit bir örnek:
```javascript
async function main(userID) {
    const userInfo = await Lookup.getUser(userID);
    console.log('Kullanıcı Bilgisi:', userInfo);

    const serverNames = await Lookup.getServerList(userID);
    console.log('Sunucular:', serverNames);

    const nameList = await Lookup.getNameList(userID);
    console.log('İsim Listesi:', nameList);

    const ageList = await Lookup.getAges(userID);
    console.log('Yaş Listesi:', ageList);

    const sexList = await Lookup.getSex(userID);
    console.log('Cinsiyet:', sexList);

    const lastSeen = await Lookup.getLastSeen(userID);
    console.log('Son Mesaj ve Ses Durumu:', lastSeen);
}

main('userID');

```

# Katkıda Bulunma
Geri bildirim ve katkılar her zaman hoş karşılanır! Lütfen bir pull request gönderin veya bir sorun bildirin.

# Lisans
Bu proje MIT Lisansı altında lisanslanmıştır.

# Not
Kullanıcı bilgilerinin gizliliğine önem verin ve bu tür bilgilere erişirken Discord'un kullanım şartlarına uyduğunuzdan emin olun.
