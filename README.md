# EAHGC Morocco Breeders Show 2026 — Landing Page

## 📦 Fichiers
- `index.html` — Page complète (logo inclus en base64, aucune dépendance locale)

---

## ✉️ Configuration EmailJS (OBLIGATOIRE pour recevoir les notifications)

### Étape 1 — Créer un compte EmailJS
1. Allez sur [https://www.emailjs.com](https://www.emailjs.com)
2. Cliquez **Sign Up** (gratuit — 200 emails/mois)
3. Confirmez votre email

### Étape 2 — Ajouter un service email
1. Dashboard → **Email Services** → **Add New Service**
2. Choisissez **Gmail** (recommandé)
3. Connectez votre compte Gmail
4. Notez le **Service ID** (ex: `service_abc123`)

### Étape 3 — Créer un template d'email
1. Dashboard → **Email Templates** → **Create New Template**
2. **To email** : `bellmaine.elghali@gmail.com`
3. **Subject** : `[EAHGC 2026] Nouvelle réservation - {{client_nom}}`
4. **Content** (copiez-collez ce contenu) :

```
Nouvelle réservation EAHGC Morocco Breeders Show 2026

Client : {{client_nom}}
Email : {{client_email}}
Téléphone : {{client_tel}}
Élevage / Société : {{client_elevage}}
Adresse : {{client_adresse}}

--- RÉSERVATION ---
Type : {{offre_type}}
Quantité : {{offre_qty}}
Journée(s) : {{offre_jours}}
TOTAL : {{offre_total}}

Message : {{message}}
```

5. Cliquez **Save**
6. Notez le **Template ID** (ex: `template_xyz456`)

### Étape 4 — Récupérer votre Public Key
1. Dashboard → **Account** → **General**
2. Copiez votre **Public Key** (ex: `user_ABCDEF123456`)

### Étape 5 — Mettre à jour index.html
Ouvrez `index.html` et remplacez ces 3 lignes (lignes ~350) :

```javascript
const EMAILJS_PUBLIC_KEY  = "VOTRE_PUBLIC_KEY";     // → ex: "user_ABCDEF123456"
const EMAILJS_SERVICE_ID  = "VOTRE_SERVICE_ID";     // → ex: "service_abc123"
const EMAILJS_TEMPLATE_ID = "VOTRE_TEMPLATE_ID";   // → ex: "template_xyz456"
```

---

## 🌐 Hébergement

### Option A — GitHub Pages (gratuit)
1. Créez un compte [GitHub](https://github.com)
2. Nouveau dépôt → uploadez `index.html`
3. Settings → Pages → Source: main branch
4. Votre site sera en ligne sur `https://votre-user.github.io/nom-repo`

### Option B — Netlify (gratuit, drag & drop)
1. Allez sur [https://app.netlify.com](https://app.netlify.com)
2. Glissez-déposez le dossier directement dans Netlify
3. Votre site est en ligne instantanément

### Option C — Hébergement traditionnel (FTP)
- Uploadez `index.html` à la racine de votre hébergement via FTP

---

## 💰 Tarification configurée

| Offre | Samedi seul | Dimanche seul | Sam + Dim |
|-------|------------|---------------|-----------|
| 1 place | 1 250 DH | 1 250 DH | 2 500 DH |
| 7 places | 8 750 DH | 8 750 DH | 17 500 DH |
| 1 table VIP | 20 000 DH | 20 000 DH | 40 000 DH |

---

© 2026 SOREC — Emirates Arabian Horse Global Cup
