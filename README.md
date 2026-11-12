# CleanDrive

Bilingual Russian / Estonian detailing studio website for Ahtme, Ida-Virumaa.

Live site: https://cleandrive-ahtme.airybluff8.chatgpt.site/

## Files

- dist/index.html — Russian page
- dist/et.html — Estonian page (production canonical URL: /et)
- dist/style.css — responsive styles
- dist/assets/ — logos and source artwork
- dist/robots.txt and dist/sitemap.xml — search indexing configuration

## Local preview

Run `python -m http.server 4173 --directory dist`, then open http://localhost:4173/.
The basic Python server serves the Estonian page at /et.html. Production hosting uses clean URLs (/et).

## Hosting

Publish dist as a static website. No build or dependencies required. Configure /et to serve et.html and redirect /et.html to /et, preserving query strings. Return HTTP 404 for unknown paths.
If changing domain, update canonical URLs, hreflang, Open Graph, JSON-LD, robots.txt and sitemap.xml in both language versions.

GitHub is a source backup; uploading here does not automatically redeploy the existing Sites publication.
