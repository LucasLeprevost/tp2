**Nom :** Lucas Leprevost  
**Groupe :** Groupe 6  
**Année :** BUT1  

**IUT Le Havre - Cours GIT**

---

### Compte-rendu TP2 – Travailler avec un dépôt Git distant (GitHub)

Dans ce TP, on continue à apprendre Git, mais cette fois **en lien avec GitHub**, une plateforme en ligne qui permet de stocker nos dépôts à distance.  
C’est très pratique pour :
- sauvegarder notre travail,
- y accéder depuis plusieurs ordinateurs,
- et plus tard, travailler en équipe.

---

### Objectifs :
- Créer un compte GitHub
- Générer une clé SSH pour sécuriser la connexion
- Lier un dépôt local à un dépôt distant
- Apprendre à utiliser `git push` et `git pull`
- Cloner un dépôt GitHub sur son ordinateur

---

### Étapes réalisées :

1. **Création d’un compte GitHub**
   - Je me suis inscrit sur GitHub pour pouvoir héberger mes dépôts en ligne

2. **Configuration de la clé SSH**
   - J’ai généré une paire de clés SSH (`ssh-keygen`)
   - Puis j’ai ajouté ma clé publique sur GitHub (via Settings → SSH and GPG Keys)
   - Cela permet d’établir une connexion sécurisée entre mon ordi et GitHub, sans entrer mon mot de passe à chaque fois

3. **Lien entre dépôt local et GitHub**
   - J’ai créé un dépôt vide sur GitHub (nommé `tp1`)
   - Puis j’ai lié mon dépôt local (`git remote add origin ...`)
   - J’ai enfin envoyé mon projet sur GitHub avec `git push -u origin master`

4. **Synchronisation entre dépôt local et distant**
   - Si je modifie des fichiers sur mon ordi, je dois faire :
     - `git add`, `git commit`, puis `git push` pour envoyer les changements
   - Si des changements ont été faits sur GitHub (par moi ou plus tard par d'autres), je peux faire `git pull` pour les récupérer

5. **Cloner un dépôt existant**
   - Pour aller plus vite, j’ai appris à cloner un dépôt déjà en ligne avec `git clone`
   - J’ai cloné un nouveau dépôt `tp2` depuis GitHub
   - Puis j’y ai copié les fichiers du TP1 (sauf le dossier `.git`)

---

### Ce que j’ai retenu :
Ce TP m’a montré comment **connecter mon travail local à un dépôt en ligne**.  
GitHub devient une sorte de "nuage pour développeurs" où je peux envoyer mes projets.

Les commandes `push` (envoyer) et `pull` (récupérer) sont indispensables pour garder mes dépôts synchronisés entre mon ordi et GitHub.

J’ai aussi compris l’intérêt de cloner un dépôt existant : c’est beaucoup plus rapide et propre que de tout refaire à la main.

---

### Quelques commandes utiles vues dans le TP :
```bash
ssh-keygen                      # Génère une clé SSH
git remote add origin <url>     # Lie un dépôt local à un dépôt distant
git push -u origin master       # Envoie le dépôt local vers GitHub
git pull                        # Récupère les mises à jour du dépôt distant
git clone <url>                 # Clone un dépôt GitHub sur l’ordinateur
