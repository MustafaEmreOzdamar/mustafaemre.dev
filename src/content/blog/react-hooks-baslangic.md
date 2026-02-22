---
title: "React Hooks'a Giriş"
date: 2025-02-20
excerpt: "useState, useEffect ve diğer Hooks'ları kullanarak React'ta state ve side effect yönetimi."
tags: ["react", "javascript", "ders"]
---

React Hooks, fonksiyonel bileşenlerde state ve lifecycle özelliklerini kullanmamızı sağlayan fonksiyonlardır.

## useState

En temel Hook. Bileşenin durumunu yönetmek için kullanılır:

```jsx
const [count, setCount] = useState(0);
```

## useEffect

Side effect'leri (API çağrıları, abonelikler) yönetmek için:

```jsx
useEffect(() => {
  document.title = `Tıklama: ${count}`;
  return () => { /* cleanup */ };
}, [count]);
```

## Özet

Hooks ile kod daha okunabilir ve yeniden kullanılabilir hale gelir. useState ve useEffect en sık kullandığımız ikilisidir.
