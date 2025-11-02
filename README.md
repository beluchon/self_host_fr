🧱 Étapes principales

SSL / Certificat

Le certificat SSL avait été créé avec un mauvais email → suppression et recréation via la section SSL.

Il ne faut rien activer d’autre, juste générer un nouveau SSL et enregistrer.

Attention : limite de 7 à 10 certificats par semaine.

💎Docker

Commandes utilisées :

sudo docker compose down
sudo docker image prune -a
sudo docker compose up -d


🥩Activation du démarrage automatique :

sudo systemctl enable docker
sudo systemctl is-enabled docker


🚗Ajout de l’utilisateur au groupe Docker pour éviter le mot de passe sudo :

sudo usermod -aG docker $USER
newgrp docker


🍊Cloudflare / Sécurité

Le SSL est déjà géré par Cloudflare, donc inutile de le forcer côté serveur.

Turnstile (captcha Cloudflare) inutile ici, car cela bloquerait les addons.

Possibilité de protéger avec mot de passe via Nginx, sauf si l’instance doit être publique.

Vérification des paramètres de sécurité dans Cloudflare → domaine → sécurité → paramètres.

Configuration Nginx Proxy Manager

Suppression de l’ancien compte.

Ajout d’un nouvel utilisateur avec mot de passe.

Application du contrôle d’accès via Access List pour protéger dash.beluchon.top.

Docker Compose

Les variables d’environnement (env) peuvent être directement placées dans le fichier docker-compose.yml :

environment:
  - TUNNEL_TOKEN=


Les ports :

Gauche = ports locaux (ne doivent pas être en double)

Droite = ports internes (ne pas modifier)

Exemple : 3001 choisi car libre.

Vérifications finales

Sites (stremthru, dash) fonctionnent correctement.

Docker démarre automatiquement au boot.

SSL et proxy configurés proprement.
