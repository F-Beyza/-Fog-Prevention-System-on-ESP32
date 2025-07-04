#Proje Amacı
Bu proje, soğuk hava depoları, izole kutular veya yüksek nemli ortamlarda çalışan sensör sistemlerinde karşılaşılan fog (yoğuşma) problemini önlemeye yönelik gömülü sistem çözümüdür.

ESP32 mikrodenetleyici kullanılarak;

sıcaklık ve nem ölçümü yapılmakta,

yoğuşma riski hesaplanmakta (çiy noktası üzerinden),

uygun şekilde ısıtıcı veya soğutucu tetiklenmektedir.

Veriler ayrıca MQTT protokolü üzerinden dış sistemlere aktarılır ve Node-RED gibi araçlarla izlenebilir hale gelir.
