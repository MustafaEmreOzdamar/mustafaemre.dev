# Canlıya Alma (Deploy) Rehberi

## 1. GitHub'a Yükle

```bash
git init
git add .
git commit -m "İlk commit"
git branch -M main
git remote add origin https://github.com/KULLANICI_ADIN/mustafaemre.dev.git
git push -u origin main
```

`KULLANICI_ADIN` yerine kendi GitHub kullanıcı adını yaz.

## 2. Vercel ile Deploy

1. [vercel.com](https://vercel.com) adresine git
2. GitHub ile giriş yap
3. "Add New Project" → Repository'ni seç
4. Framework Preset: **Astro** (otomatik algılanır)
5. "Deploy" butonuna tıkla

Birkaç dakika sonra siten canlıda olacak (örn: `mustafaemre-dev.vercel.app`).

## 3. Özel Domain (mustafaemre.dev)

1. Vercel projenin **Settings** → **Domains**
2. "Add" → `mustafaemre.dev` yaz
3. Domain sağlayıcında (GoDaddy, Namecheap vb.):
   - A kaydı: `76.76.21.21` (Vercel IP)
   - veya CNAME: `cname.vercel-dns.com`

## Formspree (İletişim & Bülten)

1. [formspree.io](https://formspree.io) hesabı oluştur
2. Yeni form ekle → Form ID'yi kopyala
3. `src/pages/iletisim.astro` → `YOUR_FORM_ID` değiştir
4. `src/components/Footer.astro` → `YOUR_NEWSLETTER_FORM_ID` değiştir (bülten için ayrı form)

## Giscus (Yorumlar)

1. GitHub'da site reponu **public** yap
2. [giscus.app](https://giscus.app) → reponu bağla, ayarları al
3. `src/components/Giscus.astro` → `repoId` ve `categoryId` değerlerini doldur
