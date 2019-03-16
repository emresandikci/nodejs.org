---
layout: security.hbs
title: Güvenlik
---

# Güvenlik

## Node.js'de bir Bug bildirmek

Node.js'deki güvenlik hatalarını [HackerOne](https://hackerone.com/nodejs) aracılığı ile bildirin veya
bu [security@nodejs.org](mailto:security@nodejs.org) email adresine bir e-posta gönderebilirsiniz.

Raporunuz 24 saat içinde onaylanır ve 48 saat içinde raporunuza daha ayrıntılı bir yanıt alırsınız.

Raporunuza verilen ilk cevaptan sonra, güvenlik ekibi sizi bir düzeltme ve tam bir duyuru için kaydedilen ilerleme konusunda bilgilendirmeye çalışacak ve bildirilen konuyu çevreleyen ek bilgi veya rehberlik isteyebilir. Bu güncellemeler en az beş günde bir gönderilecektir; pratikte, bunun her 24-48 saatte olması daha muhtemeldir.

### Node.js Bug Bounty Programı

Node.js projesi güvenlik araştırmacıları ve sorumlu kamuoyu açıklamaları için resmi bir hata ödül programı yürütmektedir.

Bu program HackerOne platformu üzerinden yürütülmektedir.Daha fazla detay için [https://hackerone.com/nodejs](https://hackerone.com/nodejs) adresini ziyaret edebilirsiniz.

## 3.party modüller için Bug bildirmek

3.party modüllerdeki güvenlik hataları kendi geliştiricilerine bildirilmeli ve ayrıca [Node Ekosistem Güvenlik Ekibi](https://hackerone.com/nodejs-ecosystem) aracılığıyla veya security-ecosystem@nodejs.org adresine e-posta gönderilerek de koordine edilmelidir.

Bu sürece ilişkin detaylar [Güvenlik Çalışma Grubu repo'sunda](https://github.com/nodejs/security-wg/blob/master/processes/third_party_vuln_process.md) bulunabilir.

Node.js ve ekosisteminin güvenliğini arttırdığınız için teşekkür ederiz. Çabalarınız ve sorumlu ifşalarınız çok takdir edilmektedir ve onaylanacaktır.

## Açıklama Politikası

Node.js için güvenlik açıklama politikası

- Güvenlik raporu alındı ​​ve bir birincil işleyici atandı. Bu kişi düzeltme ve yayımlama işlemini koordine edecektir. Sorun onaylanır ve etkilenen tüm sürümlerin listesi belirlenir. Benzer olası sorunları bulmak için kod denetlenir. Halen bakım altında olan tüm sürümler için düzeltmeler hazırlanmıştır. Bu düzeltmeler kamu havuzuna bağlı değil, duyuru beklemede yerel olarak yapılmakta.

- Bu güvenlik açığı için önerilen bir ambargo tarihi seçilir ve bu güvenlik açığı için bir CVE (Common Vulnerabilities and Exposures | Yaygınexp Güvenlik Açıkları ve Riskleri (CVE®)) istenir.

- Ambargo tarihinde, Node.js güvenlik posta listesine duyurunun bir kopyası gönderilir. Değişiklikler kamu havuzuna gönderilir ve yeni yapılar nodejs.org'a dağıtılır. E-posta listesinden 6 saat sonra bildirimin bir kopyası Node.js blogunda yayınlanacaktır.

- Tipik olarak, ambargo tarihi, CVE'nin yayınlandığı tarihten 72 saat sonra belirlenir. Ancak, bu hatanın ciddiyetine bağlı olarak değişebilir veya bir düzeltmenin uygulanmasındaki zorluk olabilir.

- Bu süreç, özellikle diğer projelerin sahipleri ile koordinasyon gerektiğinde biraz zaman alabilir. Bug mümkün olduğunca zamanında ele almak için her türlü çaba gösterilecektir; Ancak, açıklamanın tutarlı bir şekilde yapılmasını sağlamak için yukarıdaki yayın sürecini takip etmemiz önemlidir.


## Güvenlik Güncelleştirmeleri Alma

Güvenlik bildirimleri aşağıdaki birkaç metod aracılığı ile bildirilecektir.

- [https://groups.google.com/group/nodejs-sec](https://groups.google.com/group/nodejs-sec)
- [https://nodejs.org/en/blog](https://nodejs.org/en/blog)

## Bu Politikaya Yapılan Yorumlar

Eğer bu süreci iyileştirecek bir öneride bulunmak isterseniz, lütfen buradan bize [pull request](https://github.com/nodejs/nodejs.org) de bulunabilirsiniz veya buradan
 [sorun bildirebilirisiniz](https://github.com/nodejs/security-wg/issues/new).
