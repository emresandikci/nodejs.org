---
layout: about.hbs
title: Hakkında
trademark: Ticari Marka
---
# Node.js&reg; Hakkında

Eşzamansız bir olaya dayalı JavaScript çalışma zamanı olan Node, ölçeklenebilir ağ uygulamaları oluşturmak için tasarlanmıştır.Aşağıdaki "merhaba dünya" örneğinde, birçok bağlantı aynı anda ele alınabilir. Her bağlantıda callback başlatılır, ancak yapılacak iş yoksa, Node uyuyacaktır.

```javascript
const http = require('http');

const hostname = '127.0.0.1';
const port = 3000;

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Merhaba Dünya\n');
});

server.listen(port, hostname, () => {
  console.log(`Sunucu http://${hostname}:${port}/ portunda çalışıyor`);
});
```

This is in contrast to today's more common concurrency model where OS threads
are employed. Thread-based ağ iletişimi nispeten yetersiz ve kullanımı çok zor. Ayrıca Node kullanıcıları, işlemin bitmesi beklenmediği için dead-locking(kilitleme) endişesi duymazlar. Node'daki neredeyse hiçbir işlev doğrudan I/O gerçekleştirmez, bu nedenle işlem hiçbir zaman engellenmez. Hiçbir şey engellemediğinden, ölçeklenebilir sistemlerin Node'da geliştirilmeleri çok makuldür.

Eğer bu işleyişe hakim değilseniz bu konu üzerine bir makale mevcuttur.
[Blocking vs Non-Blocking][].

---

Node, tasarımda Ruby's [Event Machine][] veya Python's [Twisted][] gibi sistemlere benzer ve bunlardan etkilenir. Node olay modelini biraz daha ileri götürür. Bir [event loop][] kütüphane yerine çalışma zamanı yapısı olarak sunar. Diğer sistemlerde, olay döngüsünü başlatmak için her zaman engelleyici bir çağrı vardır. Tipik olarak davranış bir betiğin başında geri çağrılarla tanımlanır ve sonunda `EventMachine::run()` gibi bir engelleme çağrısı yoluyla bir sunucuyu başlatır.Node'da start-the-event-loop gibi bir çağırma işlevi yoktur.Node, girdi betiğini yürüttükten sonra olay döngüsüne girer. Gerçekleştirilecek başka geri callback olmadığında, Node olay döngüsünden çıkar. Bu davranış tarayıcı JavaScript'i gibidir - olay döngüsü kullanıcıdan gizlenir.

HTTP, Akış ve düşük gecikme süresi göz önünde bulundurularak tasarlanan Node'da birinci sınıf bir vatandaştır. Bu, Node'u bir web kütüphanesinin veya çerçevenin temeli için çok uygun kılar.

Node thread'ler olmadan tasarlandığı için, ortamınızdaki birden çok çekirdekten yararlanamayacağınız anlamına gelmez. Child işlemler [`child_process.fork()`][] API'simizi kullanarak oluşturulabilir ve iletişim kurması kolay olacak şekilde tasarlanmıştır. Aynı arabirim üzerine kurulu, çekirdeklerinizde yük dengelemesini sağlamak için işlemler arasında soketleri paylaşmanıza izin veren [`cluster`][] modülüdür.

[Blocking vs Non-Blocking]: https://nodejs.org/en/docs/guides/blocking-vs-non-blocking/
[`child_process.fork()`]: https://nodejs.org/api/child_process.html#child_process_child_process_fork_modulepath_args_options
[`cluster`]: https://nodejs.org/api/cluster.html
[event loop]: https://nodejs.org/en/docs/guides/event-loop-timers-and-nexttick/
[Event Machine]: https://github.com/eventmachine/eventmachine
[Twisted]: http://twistedmatrix.com/
