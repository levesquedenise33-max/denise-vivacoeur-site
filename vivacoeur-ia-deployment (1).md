# 🚀 ViVaCoeur IA - Guide de Déploiement

## 📍 URLs de Déploiement

### **URL Principale**
```
https://vivacoeur.com/ia
```

### **URL Directe (Alternative)**
```
https://vivacoeur.com/apps/vivacoeur-ia-creator
```

### **Lien Court (QR Code)**
```
https://vivacoeur.link/ia
```

---

## 🔧 Instructions de Déploiement sur Netlify

### **Étape 1: Préparer le fichier**

1. Télécharge: `vivacoeur-ia-app.html`
2. Renomme en: `ia.html` (pour l'URL https://vivacoeur.com/ia)

### **Étape 2: Uploader sur Netlify**

```bash
# Option A: Via interface Netlify
1. Connecte-toi à Netlify (https://app.netlify.com)
2. Sélectionne ton site "vivacoeur.com"
3. Clique "Deploy" > "Drag and drop"
4. Dépose le fichier ia.html
5. Renomme: ia.html
6. Deploy! ✅

# Option B: Via Git/GitHub
1. Push dans ton repo: /src/pages/ia.html
2. Netlify redéploie automatiquement
3. Accès via: https://vivacoeur.com/ia
```

### **Étape 3: Vérifier l'accès**

```
✅ https://vivacoeur.com/ia
✅ Page charge en <2 secondes
✅ Tous les boutons réactifs
✅ Micro fonctionne (demande permission)
✅ Console JavaScript sans erreurs
```

---

## 🔐 Configuration API Anthropic

### **Pour activer la création réelle d'agents:**

1. **Ajouter ta clé API au formulaire:**
   - Champ "Clé API Anthropic"
   - Colle: `sk-ant-...`
   - ✅ Mode local sinon

2. **Ou configurer variable d'environnement Netlify:**
   ```
   Netlify Dashboard > Build & Deploy > Environment
   
   Ajouter:
   VITE_ANTHROPIC_API_KEY = sk-ant-...
   ```

3. **Ou intégrer API via backend (recommandé):**
   ```
   Créer endpoint: https://vivacoeur.com/api/create-agent
   
   POST /api/create-agent
   Body: {
     name: "ViVaCoeur IA Tuteur",
     description: "...",
     capabilities: [...],
     apiKey: process.env.ANTHROPIC_API_KEY
   }
   
   Réponse: { agentId, status, createdAt }
   ```

---

## 📊 Intégrations Multi-Plateformes

### **1. Google Classroom**
```
1. Crée une classe "ViVaCoeur IA"
2. Ajoute lien dans les matériaux:
   https://vivacoeur.com/ia
3. Élèves accèdent directement
```

### **2. Zoom Webinaire**
```
1. Zoom > Share Screen
2. Affiche: https://vivacoeur.com/ia
3. Démontre en direct
4. Enregistre la session
```

### **3. Shopify (Coeur&Vie)**
```
1. Ajoute produit "Formation ViVaCoeur IA"
2. Description include le lien:
   https://vivacoeur.com/ia
3. Après achat: accès formation
```

### **4. Email Zoho Mail**
```
Campagne formation:

Subject: 🚀 Accès ViVaCoeur IA - Crée tes propres Agents!

Body:
Bonjour [Nom],

Clique ici pour accéder au Meta-Agent ViVaCoeur IA:

👉 https://vivacoeur.com/ia

[Bouton CTA]
```

### **5. Moodle/LMS Custom**
```
Ajoute dans cours:

Ressource externe:
URL: https://vivacoeur.com/ia
Display: Embedded in frame (Iframe)
```

---

## 📱 QR Code pour Partage Mobile

### **Générer QR Code**
```
URL: https://vivacoeur.com/ia

Génère sur: https://qr-code-generator.com/
Télécharge comme image
Partage sur:
- Flyers
- Emails
- Posters
- Slides PowerPoint
```

---

## 📈 Analytics & Tracking

### **Ajouter Google Analytics**

Insère dans `<head>`:
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_ID');
</script>
```

### **Suivre:**
- Nombre de visiteurs
- Agents créés par jour
- Temps moyen par création
- Taux de complétion

---

## 🔗 Partage Complet

### **Email à tes élèves:**

```
Sujet: 🤖 Accès ViVaCoeur IA - Crée des Agents Autonomes!

Bonjour,

Tu as maintenant accès à ViVaCoeur IA, notre plateforme révolutionnaire 
de création d'agents IA pour l'entrepreneurship.

🔗 LIEN D'ACCÈS:
https://vivacoeur.com/ia

📖 GUIDE COMPLET:
ViVaCoeur_IA_Guide_Complet.docx (en pièce jointe)

✨ CE QUE TU PEUX FAIRE:
✓ Créer des tuteurs IA personnalisés
✓ Analyser documents (Word, Excel, PDF, PowerPoint)
✓ Transcrire voix en français
✓ Traduire dans 10+ langues
✓ Déployer agents sur vivacoeur.com
✓ Créer d'autres agents (récursion!)

🎯 DÉMARRAGE RAPIDE:
1. Ouvre: https://vivacoeur.com/ia
2. Décris ton agent (texte ou voix)
3. Configure capacités
4. Clique "Lancer ViVaCoeur IA Creator"
5. Vois les 4 phases en temps réel

❓ QUESTIONS?
📧 denise@vivacoeur.com
🌐 https://vivacoeur.com

Bon créatif!
Denise
```

---

## ✅ Checklist Déploiement Complet

- [ ] Fichier ia.html uploadé sur Netlify
- [ ] URL vivacoeur.com/ia accessible
- [ ] Micro fonctionne (test permissions)
- [ ] Lien API Anthropic configuré
- [ ] Déploiement Google Classroom complété
- [ ] Intégration Zoom testée
- [ ] Email campagne Zoho Mail envoyée
- [ ] QR Code généré & imprimé
- [ ] Analytics Google configurés
- [ ] Support email configuré (denise@vivacoeur.com)
- [ ] Document Word téléchargeable
- [ ] PowerPoint présentation prêt
- [ ] Excel suivi agents prêt

---

## 🚨 Dépannage

| Problème | Solution |
|----------|----------|
| Page blanche | Vérifier console F12 > Console |
| Micro pas de son | Vérifier permissions navigateur |
| API ne fonctionne pas | Vérifier clé sk-ant-... est valide |
| Lien pas accessible | Vérifier Netlify DNS settings |
| Déploiement lent | Minifier HTML (enlever commentaires) |

---

## 📞 Support

**Email:** denise@vivacoeur.com  
**Site:** https://vivacoeur.com  
**Formulaire:** https://vivacoeur.com/contact

