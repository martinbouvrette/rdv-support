# rdv-support

Le site de l'app **RDV**, servi par GitHub Pages sur `rdv.wominute.com`.

Deux pages, et Apple exige les deux pour une app à abonnement :

| Adresse | Rôle | Où elle est déclarée |
|---|---|---|
| `/confidentialite` | Politique de confidentialité | App Store Connect · écran d'accueil de l'app · paywall |
| `/soutien` | Page de soutien (Support URL) | App Store Connect |

## Pourquoi ce dépôt existe

La politique de RDV vivait sur `wominute.com`, le site de **Wo-Minute** —
un autre produit. Elle s'affichait donc sous l'en-tête « wo-minute-support »,
et il aurait fallu y ajouter une deuxième page RDV pour la Support URL.

Ces deux adresses partent dans le **binaire de l'app** et dans App Store
Connect. Les changer après un dépôt coûte une nouvelle version. D'où la
décision de trancher avant le premier dépôt, le 21 septembre 2026.

Un sous-domaine plutôt qu'un domaine acheté : gratuit, le DNS de
`wominute.com` est déjà chez Cloudflare, et RDV obtient son propre espace.

## ⚠️ Les anciennes adresses doivent continuer de répondre

`wominute.com/rdv-confidentialite` a été publique et peut avoir été mise en
signet ou indexée. Elle redirige vers la nouvelle. Ne pas la supprimer.

## Mise en route (fait une seule fois)

1. Dépôt GitHub `rdv-support`, public.
2. Settings ▸ Pages ▸ Source : `main`, dossier `/`.
3. Cloudflare ▸ DNS de `wominute.com` ▸ CNAME `rdv` → `martinbouvrette.github.io`,
   **DNS only** (nuage gris) — le proxy de Cloudflare empêche GitHub d'émettre
   le certificat TLS.
4. Settings ▸ Pages ▸ Custom domain : `rdv.wominute.com`, puis cocher
   *Enforce HTTPS* une fois le certificat émis (quelques minutes).
