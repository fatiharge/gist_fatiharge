# gist.fatiharge.com

Konuları küçük parçalara bölerek hatırlatıcı notlar halinde yayınlamak amacıyla hazırlanmıştır.

## İçerik Hakkında

gist.fatiharge.com, bilgilendirici içerikleri hızlıca hatırlatıcı notlar şeklinde sunmak için geliştirilmiştir. 

## Teknolojiler Hakkında
Jekyll tabanlı **LightSpeed** teması, sade yapıya sahiptir. Tüm kaynak dosyaları bu repoda yer almaktadır. Sunucu yapılandırmasında, statik dosyalar bir NGINX Docker konteyneri üzerinde çalışmaktadır. Reverse proxy olarak ise Traefik kullanılmakta ve CI/CD süreçleri Jenkins üzerinden yönetilmektedir.

```mermaid
	graph LR
    A[CI/CD Süreçleri] --> A1[Github webhook]
    A1 --> A2[Jenkins]
    A2 --> A10[TEST]
    A10 --> A11[Fail Notifaction]
    A10 --> A3[Docker]
    A3 --> A4[Traefik]
	A4 --> A5[NGINX]
	
	A2 --> AA3[Static Files]

	BB2[Static Files] --> B3[NGINX]


    B[HTTP REQUEST] --> B0[gist.fatiharge.com]
    B0 --> B1[Traefik]
    B1 --> B2[docker]
    B2 --> B3[NGINX]
    B3 --> B4[jekyllrb]
    B4 --> B5[LightSpeed]
```

> **İletişim:** fatih@fatiharge.com