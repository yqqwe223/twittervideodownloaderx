# 🐦 Outil d'Analyse de Vidéos X.com

> Un outil léger, rapide et polyvalent pour extraire du contenu vidéo depuis X (anciennement Twitter)

[🌐 Démo en ligne](https://twittervideodownloaderx.com/fr) • [📝 Guide d'utilisation](#-guide-dutilisation) • [❓ Questions fréquentes](#-questions-fréquentes)

---

## 📋 Présentation du projet

Ce projet est un outil d'analyse vidéo basé sur le web, conçu pour extraire en toute sécurité des ressources vidéo à partir de publications publiques sur X.com (anciennement Twitter), tout en proposant des options de conversion et de téléchargement dans plusieurs formats. Aucune installation de logiciel client ni création de compte requise : utilisez-le directement depuis votre navigateur.

> ⚠️ **Avertissement important** : Cet outil est destiné exclusivement à un usage personnel d'apprentissage, de recherche technique et dans le cadre d'une utilisation raisonnable. Veuillez respecter l'[Accord développeur de la plateforme X](https://developer.twitter.com/en/developer-terms/agreement) ainsi que les lois sur le droit d'auteur applicables dans votre pays. Il est strictement interdit d'utiliser cet outil à des fins portant atteinte aux droits d'autrui.

---

## ✨ Fonctionnalités principales

- 🔗 **Analyse de liens** : Compatible avec les URLs standards des publications X.com ; détection automatique des vidéos et GIFs animés
- 📥 **Export multi-formats** :
  - Vidéo MP4 en qualité d'origine
  - Extraction audio → Format MP3
  - Extrait vidéo → Conversion en GIF animé
- 🌍 **Interface multilingue** : Prise en charge du français, anglais, chinois, japonais, coréen, et 16 langues au total
- 📱 **Compatibilité multiplateforme** : Fonctionne parfaitement sur Chrome / Firefox / Safari / Edge ; expérience optimisée pour mobile et tablette
- 🔒 **Respect de la vie privée** : Aucune inscription requise, aucune collecte de données personnelles ; processus d'analyse entièrement anonyme
- ⚡ **Traitement rapide** : Analyse terminée en moyenne en moins de 5 secondes ; prise en charge des requêtes simultanées

---

## 🚀 Démarrage rapide

### Utilisation en ligne (recommandée)
1. Accédez à [https://twittervideodownloaderx.com/fr](https://twittervideodownloaderx.com/fr)
2. Copiez le lien de la publication cible (exemple : `https://x.com/user/status/123456789`)
3. Collez le lien dans le champ de saisie → Cliquez sur le bouton 「Analyser」
4. Sélectionnez le format souhaité → Enregistrez le fichier selon les instructions du navigateur

### Déploiement local (pour développeurs)
```bash
# Cloner le dépôt
git clone https://github.com/your-repo/x-video-parser.git

# Installer les dépendances
cd x-video-parser && npm install

# Configurer les variables d'environnement (optionnel)
cp .env.example .env

# Démarrer le serveur de développement
npm run dev
```

> 💡 Note : Ce projet utilise une architecture basée sur Node.js + Express. Consultez la documentation détaillée de déploiement dans `/docs/DEPLOY.md`

---

## 🛠 Stack technique

| Module | Technologies utilisées |
|--------|------------------------|
| Frontend | Vue 3 + TypeScript + Vite |
| Backend | Node.js + Express + Axios |
| Traitement vidéo | ffmpeg.wasm (conversion légère côté frontend) |
| Proxy de relais | Cloudflare Workers / Middleware personnalisé |
| Internationalisation | vue-i18n + Packs de langues JSON |

---

## 📚 Guide d'utilisation

### Flux d'opération de base
```
1. Obtenir le lien de la publication
   └─ Ouvrez la publication cible sur X.com → Copiez l'URL depuis la barre d'adresse du navigateur

2. Envoyer la demande d'analyse
   └─ Collez le lien dans le champ de saisie de l'outil → Cliquez sur 「Télécharger la vidéo」

3. Sélectionner le format de sortie
   ├─ 🎬 Télécharger en MP4 : Enregistrer avec la qualité d'origine
   ├─ 🎵 Convertir en MP3 : Extraire la piste audio
   └─ 🎞 Convertir en GIF : Générer une animation courte (recommandé : ≤15 secondes)

4. Enregistrer le fichier
   └─ La ressource s'ouvrira dans un nouvel onglet → Clic droit/menu → 「Enregistrer sous」
```

### Conseils pour l'utilisation sur mobile
- iOS Safari : Bouton Partager → 「Enregistrer dans Fichiers」
- Android Chrome : Appui long sur la vidéo → 「Télécharger la vidéo」
- Si la vidéo se lance automatiquement : Cliquez sur `⋮` en haut à droite du lecteur → Sélectionnez 「Télécharger」

---

## ❓ Questions fréquentes

**Q : Où sont enregistrés les fichiers téléchargés ?**  
R : Les fichiers sont enregistrés dans le dossier de téléchargement configuré dans votre navigateur. Vous pouvez vérifier ou modifier ce chemin dans les paramètres du navigateur.

**Q : Puis-je analyser des comptes privés ou du contenu restreint ?**  
R : Non. Cet outil ne fonctionne qu'avec des publications configurées comme publiques et respecte les paramètres d'accès du contenu d'origine.

**Q : La qualité image/audio est-elle réduite après conversion ?**  
R : Le format MP4 conserve la qualité d'origine. Le format MP3 utilise un encodage standard à 128 kbps. Le format GIF optimise le taux d'images en fonction de la durée pour équilibrer taille du fichier et fluidité.

**Q : L'historique de téléchargement ou le cache sont-ils stockés ?**  
R : Non. Toutes les ressources sont transmises directement à l'appareil de l'utilisateur via un proxy temporaire ; le serveur ne conserve aucune requête ni fichier multimédia.

**Q : Que faire si l'analyse échoue ?**  
R : Veuillez vérifier : ① Que le lien correspond à une publication publique valide ② Que votre connexion internet est stable ③ Essayez avec un autre navigateur. Si le problème persiste, n'hésitez pas à le signaler via un Issue.

---

## ⚖️ Conformité réglementaire et Clause de non-responsabilité

- Cet outil **ne contourne ni ne viole aucune mesure de protection technique** des plateformes ; il se contente d'obtenir des métadonnées via des interfaces publiques
- L'utilisateur est responsable de vérifier que son usage est conforme à la législation locale et aux conditions d'utilisation de la plateforme
- Cas d'usage recommandés : Archivage personnel, démonstrations éducatives, matériel de référence pour la création de contenu... toujours dans le cadre de l'usage loyal (Fair Use)
- Si vous identifiez un contenu susceptible de porter atteinte à des droits, veuillez contacter le canal officiel de [X via ce formulaire de signalement de droits d'auteur](https://help.twitter.com/forms/dmca)

---

## 🤝 Guide de contribution

Nous accueillons avec plaisir vos Pull Requests et signalements d'Issues ! Avant de contribuer, veuillez consulter :
- [Standards de code](/CONTRIBUTING.md)
- [Guide de traduction multilingue](/locales/README.md)
- [Exigences de sécurité et de conformité](/SECURITY.md)

---

## 📄 Licence

Ce projet est publié sous la [Licence MIT](/LICENSE). Il peut être utilisé gratuitement à des fins éducatives et de recherche. Pour un usage commercial, veuillez vérifier attentivement le respect des réglementations légales applicables.

---

> 🌟 Si cet outil vous a été utile, n'hésitez pas à ✨lui attribuer une Étoile (Star) ! Votre soutien est la plus grande motivation pour que nous continuions à maintenir et améliorer ce projet~

*Dernière mise à jour : Mai 2026 | Version : v2.1.0*