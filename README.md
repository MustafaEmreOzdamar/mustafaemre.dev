# mustafaemre.dev

Kişisel web sitesi — blog, projeler, yazılım haberleri ve dersler.

## Özellikler

- Dark / Light mode
- Blog (Markdown, arama)
- Projeler sayfası
- İletişim formu (Formspree)
- Newsletter (Footer)
- Giscus yorum sistemi
- Mobil responsive, hamburger menü

## Kurulum

```bash
npm install
npm run dev
```

http://localhost:4321

## Proje Yapısı

```
src/
├── components/     # Header, Footer, ThemeToggle, MobileNav, BlogSearch, Giscus
├── content/blog/   # Markdown blog yazıları
├── data/
│   └── site.ts     # Site ayarları, projeler, "şu an" metni
├── layouts/
└── pages/          # /, /blog, /blog/[slug], /projeler, /hakkimda, /iletisim
```

## Özelleştirme

| Ne | Dosya |
|----|-------|
| "Şu an" metni, e-posta | `src/data/site.ts` |
| Projeler listesi | `src/data/site.ts` |
| Sosyal linkler | `src/components/Footer.astro` |
| İletişim formu | `src/pages/iletisim.astro` (Formspree ID) |
| Newsletter formu | `src/components/Footer.astro` (Formspree ID) |
| Yorumlar (Giscus) | `src/components/Giscus.astro` |

## Blog Yazısı

`src/content/blog/` klasörüne `.md` ekleyin:

```md
---
title: "Başlık"
date: 2025-02-22
excerpt: "Kısa açıklama"
tags: ["etiket1", "etiket2"]
---

İçerik...
```

## Deploy

Detaylı adımlar için **DEPLOY.md** dosyasına bakın.

1. GitHub'a push
2. Vercel'e bağla
3. Domain ekle (opsiyonel)
