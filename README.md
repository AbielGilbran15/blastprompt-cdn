# CDN Build Output

Folder ini berisi artefak build produksi Blastprompt Studio yang diserve via [jsDelivr](https://www.jsdelivr.com/?docs=gh).

| File | Fungsi |
| --- | --- |
| `bundle.js` | Aplikasi React (single bundle, React di-load terpisah dari CDN) |
| `body.html` | Markup HTML body untuk Canvas shell (`<div id="root">`) |
| `styles.css` | CSS hasil kompilasi Tailwind |

## Jangan edit manual

File `bundle.js`, `body.html`, dan `styles.css` **dihasilkan otomatis** oleh pipeline:

```bash
npm run build
```

GitHub Actions (`deploy-cdn.yml`) menjalankan build saat push ke `main`, menyalin hasil ke folder ini, lalu purge cache jsDelivr.

Ubah kode di `/src`, bukan di folder ini.
