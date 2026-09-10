# TrueNAS SCALE on Proxmox (Quarto book + site)

Quarto book source. Open the folder as an RStudio project and render, or:

```bash
cd proxmox-truenas-book
quarto preview    # live website
quarto render     # writes _book/
quarto publish gh-pages
```

`project.type` is `book`, which Quarto builds as a multi-page HTML site with numbered chapters, search, and sidebar. PDF and EPUB formats are also declared in `_quarto.yml`.

- Website: https://esimms999.github.io/proxmox-truenas-book/
- PDF: https://esimms999.github.io/proxmox-truenas-book/TrueNAS-SCALE-on-Proxmox.pdf
