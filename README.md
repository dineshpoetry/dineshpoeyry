# Dinesh Poetry
Cloudflare Pages + D1 starter, no build step and no R2.

## Deploy
1. Back up your existing D1 database. Do not delete it.
2. Replace the GitHub repository files with this folder's contents.
3. Cloudflare Pages build command: blank; output directory: repository root.
4. Pages Settings → Functions → D1 binding: variable `DB`, select your existing database.
5. Set Pages environment variable `ADMIN_TOKEN` to a long random secret. Keep it private.
6. Do not run schema.sql on an existing database without checking its columns first. `CREATE TABLE IF NOT EXISTS` does not migrate old tables.
7. Deploy and test `/api/health`, `/api/library`, `/api/poets`, `/api/classic-books`.

Pages included: Home, Library, Readers, Reader page, Admin publishing form.
The world catalog uses Gutendex's `copyright=false` signal; this is not a worldwide legal guarantee. Only share full text when legally allowed. PDF links are source links; this site does not host PDFs.
