# ZUNE PREMIUM ADMIN 3.0 — ROOT HTML BUILD

## Muundo wa URL
HTML zote za modules ziko moja kwa moja kwenye root ya repository: `users.html`, `sellers.html`, `orders.html`, n.k. Hakuna `pages/`, iframe wala `#users` routing.

## Deploy GitHub Pages
1. Pakua na unzip project.
2. Weka yaliyomo ndani ya repository/folder `admin/` ya GitHub Pages.
3. Hakikisha `index.html` iko kwenye root hiyo.
4. Enable GitHub Pages kwa branch/folder unayotumia.
5. Fungua `https://<username>.github.io/admin/users.html`.

## Supabase
- Weka Project URL na anon/public key ndani ya `js/config.js`.
- Usitumie `service_role` key kwenye browser wala kucommit secrets.
- `users.html` ina contract ya `window.ZUNE_USERS_API`; implement API hii kwa Edge Functions/RPC zilizothibitishwa kabla ya kutumia create/edit/ban/delete.
- Moduli nyingine zina read-only discovery scaffold; hazifanyi write operations za kubuni. Hakikisha kila table, column na RLS policy ipo kabla ya kutegemea read query.
- Usikimbize migrations bila ku-review schema ya production.

## Muhimu
Hii ZIP inatekeleza mabadiliko ya file layout na deep-link URL ulioomba. Si uthibitisho kwamba modules zote zimeunganishwa kikamilifu na Supabase au kwamba vitendo vyote vya marketplace viko live. SQL migration files hazikuongezwa upya ili kuepuka kurudia au kuharibu migrations zilizopo.
