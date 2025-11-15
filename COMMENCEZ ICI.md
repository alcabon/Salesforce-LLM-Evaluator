# 🚀 COMMENCEZ ICI - Salesforce LLM Evaluator

## 👋 Bienvenue !

Félicitations ! Vous avez maintenant accès à une **extension VSCode complète** pour évaluer la qualité du code généré par différents modèles de langage (LLM) via GitHub Copilot, spécialement optimisée pour le développement Salesforce.

---

## ⚡ Démarrage ultra-rapide (5 minutes)

### Option 1: Script automatique (RECOMMANDÉ)

**Sur Linux/macOS:**
```bash
chmod +x setup.sh
./setup.sh
```

**Sur Windows:**
```cmd
setup.bat
```

Le script va:
- ✅ Vérifier les prérequis
- ✅ Installer les dépendances
- ✅ Compiler le projet
- ✅ Configurer VSCode
- ✅ Lancer l'extension

### Option 2: Installation manuelle

```bash
npm install
npm run compile
code .
# Appuyer sur F5 dans VSCode
```

---

## 📁 Que contient ce projet ?

### 🎯 Fichiers principaux

| Fichier | Description | Priorité |
|---------|-------------|----------|
| **START_HERE.md** | 👈 Ce fichier - Votre point de départ | ⭐⭐⭐ |
| **GETTING_STARTED.md** | Guide complet de mise en route | ⭐⭐⭐ |
| **QUICKSTART.md** | Installation en 5 minutes | ⭐⭐⭐ |
| **README.md** | Documentation complète | ⭐⭐ |
| **extension.ts** | Code source principal (800+ lignes) | ⭐⭐ |
| **salesforce-coding-standards.json** | 75+ règles de codage | ⭐⭐ |

### 📚 Documentation complète

| Fichier | Contenu | Pour qui ? |
|---------|---------|-----------|
| **INDEX.md** | Index de tous les fichiers | Tous |
| **ARCHITECTURE.md** | Documentation technique | Développeurs |
| **CONFIGURATION.md** | Config avancée, CI/CD | DevOps |
| **CHANGELOG.md** | Versions et roadmap | Tous |

### 🛠️ Outils

| Fichier | Utilité |
|---------|---------|
| **setup.sh** / **setup.bat** | Installation automatique |
| **analyze_results.py** | Analyse des résultats |
| **example-results.json** | Exemples de données |

### ⚙️ Configuration

| Fichier | Rôle |
|---------|------|
| **package.json** | Configuration extension |
| **tsconfig.json** | Config TypeScript |
| **.vscodeignore** | Fichiers exclus |

---

## 🎯 À quoi ça sert ?

Cette extension vous permet de:

### 1️⃣ Tester différents LLM
- GPT-4o, GPT-4, GPT-3.5-Turbo
- Claude 3.5 Sonnet
- Tous les modèles GitHub Copilot disponibles

### 2️⃣ Évaluer 5 types de code Salesforce
- ✅ **Apex** - Classes, services, triggers
- ✅ **LWC** - Composants JavaScript et HTML
- ✅ **Batch Apex** - Classes batch
- ✅ **REST API** - Endpoints personnalisés
- ✅ **Tests** - Classes de test Apex et Jest

### 3️⃣ Vérifier 75+ règles de qualité
- Bulkification (pas de SOQL/DML dans les boucles)
- Sécurité (sharing, FLS, permissions)
- Gestion d'erreurs (try-catch, logging)
- Accessibilité (ARIA, labels)
- Performance (optimisations)

### 4️⃣ Obtenir des scores et rapports
- Score sur 100 par test
- Détail des violations
- Comparaison entre modèles
- Export JSON/CSV

---

## 🏃 Premiers pas

### Étape 1: Installer (2 min)
```bash
./setup.sh  # ou setup.bat sur Windows
```

### Étape 2: Lancer (1 min)
```bash
code .      # Ouvrir dans VSCode
# Appuyer sur F5
```

### Étape 3: Tester (2 min)
1. Dans la nouvelle fenêtre VSCode, ouvrir la palette de commandes (Ctrl+Shift+P)
2. Chercher: "Salesforce LLM: Open LLM Evaluator Panel"
3. Sélectionner un modèle (ex: GPT-4o)
4. Cliquer sur "▶️ Run Test" pour un prompt Apex
5. Voir les résultats !

---

## 📖 Quelle documentation lire ?

### Je veux juste tester rapidement
→ **QUICKSTART.md** (5 minutes de lecture)

### Je veux tout comprendre
→ **GETTING_STARTED.md** (15 minutes de lecture)

### Je veux la doc complète
→ **README.md** (référence complète)

### Je suis développeur
→ **ARCHITECTURE.md** (documentation technique)

### Je veux personnaliser
→ **CONFIGURATION.md** (exemples avancés)

### Je cherche un fichier spécifique
→ **INDEX.md** (index complet)

---

## 💡 Exemple concret

```
Utilisateur: "Je veux comparer GPT-4o et Claude 3.5 sur la génération de code Apex"

Actions:
1. Ouvrir le panel LLM Evaluator
2. Sélectionner GPT-4o
3. Run All Tests (Apex)
4. Noter le score moyen (ex: 88/100)
5. Sélectionner Claude 3.5
6. Run All Tests (Apex)
7. Noter le score moyen (ex: 92/100)
8. Exporter les résultats
9. Analyser avec analyze_results.py

Résultat:
📊 Claude 3.5 est meilleur pour Apex (92 vs 88)
⚠️  Violations courantes: Missing documentation
💡 Recommandation: Utiliser Claude 3.5 pour code Apex
```

---

## 🎨 Fonctionnalités clés

### Interface utilisateur
- ✅ Panel latéral avec icône IA 🤖
- ✅ Dropdown de sélection de modèle
- ✅ Prompts pré-définis par catégorie
- ✅ Tableau de résultats en temps réel
- ✅ Boutons d'export et actions groupées

### Prompts de test inclus
```
Apex:
  ✓ Simple - Classe de service basique
  ✓ Trigger - Trigger avec handler
  ✓ Complex - Service avec permissions et erreurs

LWC:
  ✓ Simple - Liste avec recherche
  ✓ DataTable - Table éditable
  ✓ Complex - Formulaire avec validation

Batch:
  ✓ Simple - Batch de mise à jour
  ✓ Complex - Batch stateful avec logs

REST:
  ✓ Simple - Endpoint GET
  ✓ Complex - CRUD complet

Tests:
  ✓ Apex - Classe de test complète
  ✓ LWC - Tests Jest avec mocks
```

### Évaluation automatique
- 🔍 Détection par patterns regex
- 🔍 Vérifications personnalisées
- 📊 Scoring pondéré par sévérité
- 📈 Statistiques et métriques
- 💾 Historique des tests

---

## 🔧 Prérequis

Avant de commencer, assurez-vous d'avoir:

- ✅ **Node.js** v18 ou supérieur
- ✅ **VS Code** v1.85 ou supérieur
- ✅ **GitHub Copilot** (abonnement actif)
- ✅ **npm** (inclus avec Node.js)

Vérifications rapides:
```bash
node --version    # Doit afficher v18.x ou plus
code --version    # Doit afficher 1.85.x ou plus
code --list-extensions | grep copilot  # Doit trouver Copilot
```

---

## 🎓 Ressources d'apprentissage

### Tutoriels intégrés
1. **QUICKSTART.md** - Tutoriel 5 minutes
2. **GETTING_STARTED.md** - Tutoriel complet
3. **example-results.json** - Exemples réels
4. **analyze_results.py** - Script d'analyse

### Documentation externe
- [VS Code Extension API](https://code.visualstudio.com/api)
- [GitHub Copilot Docs](https://docs.github.com/copilot)
- [Salesforce Apex Guide](https://developer.salesforce.com/docs/atlas.en-us.apexcode.meta/apexcode/)
- [LWC Documentation](https://developer.salesforce.com/docs/component-library/overview/components)

---

## ❓ FAQ

### Q: L'extension fonctionne-t-elle sans GitHub Copilot ?
**R:** Non, GitHub Copilot est requis car l'extension utilise son API pour accéder aux LLM.

### Q: Puis-je ajouter mes propres règles de codage ?
**R:** Oui ! Éditez `salesforce-coding-standards.json` ou créez votre propre fichier.

### Q: Combien de temps prend un test complet ?
**R:** Environ 5-10 minutes pour tous les prompts (15 tests) avec délais anti-rate-limit.

### Q: Les résultats sont-ils sauvegardés ?
**R:** Oui, vous pouvez exporter en JSON ou CSV à tout moment.

### Q: Puis-je utiliser d'autres LLM que Copilot ?
**R:** Actuellement non, mais l'architecture permet d'ajouter d'autres providers.

### Q: Le code généré est-il réutilisable ?
**R:** Oui ! Tous les codes générés sont affichés et peuvent être copiés.

---

## 🐛 Problèmes courants

### "No models available"
**Solution**: Vérifier que GitHub Copilot est installé et actif
```bash
code --list-extensions | grep copilot
```

### "Cannot compile"
**Solution**: Supprimer node_modules et réinstaller
```bash
rm -rf node_modules
npm install
npm run compile
```

### "Standards file not found"
**Solution**: Vérifier le chemin dans settings.json
```json
{
  "salesforce-llm-evaluator.standardsFile": "${workspaceFolder}/salesforce-coding-standards.json"
}
```

---

## 🚀 Prochaines étapes

### Niveau 1 - Débutant (30 min)
- [ ] Lire QUICKSTART.md
- [ ] Exécuter setup.sh/setup.bat
- [ ] Lancer votre premier test
- [ ] Explorer l'interface

### Niveau 2 - Intermédiaire (1-2h)
- [ ] Lire GETTING_STARTED.md
- [ ] Tester tous les types de code
- [ ] Comparer 2-3 modèles
- [ ] Exporter et analyser les résultats

### Niveau 3 - Avancé (2-4h)
- [ ] Lire ARCHITECTURE.md
- [ ] Personnaliser les standards
- [ ] Créer vos propres prompts
- [ ] Intégrer dans votre workflow

### Niveau 4 - Expert (4h+)
- [ ] Lire CONFIGURATION.md
- [ ] Configurer CI/CD
- [ ] Créer des rapports automatisés
- [ ] Contribuer au projet

---

## 🎉 Vous êtes prêt !

### Action immédiate recommandée:

1. **Exécutez** le script de setup:
   ```bash
   ./setup.sh
   ```

2. **Ouvrez** le projet dans VSCode:
   ```bash
   code .
   ```

3. **Lancez** l'extension (F5)

4. **Testez** votre premier LLM !

---

## 📞 Besoin d'aide ?

- 📧 **Email**: support@example.com
- 💬 **Discord**: [Lien serveur]
- 🐛 **Issues**: GitHub Issues
- 📖 **Wiki**: GitHub Wiki
- 📚 **Docs**: Tous les fichiers .md

---

## 🌟 Contribuer

Le projet est open source ! Contributions bienvenues:
- 🐛 Reporter des bugs
- 💡 Proposer des fonctionnalités
- 📝 Améliorer la documentation
- 🔧 Soumettre du code

---

**Version**: 1.0.0  
**Date**: 15 Janvier 2025  
**License**: MIT  

---

<div align="center">

### 🚀 Prêt à tester vos LLM ?

**[COMMENCER MAINTENANT →](QUICKSTART.md)**

</div>

---

*Développé pour l'évaluation de la génération de code par LLM sur Salesforce*

**Happy Testing! 🎉**
