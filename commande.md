**Arrêter tous les services (garde images et volumes)**
```sudo docker compose down```

**Arrêter un service spécifique**
```
sudo docker compose stop nom_service
```

**Démarrer tous les services**
sudo docker compose up -d

**Démarrer un service spécifique**
sudo docker compose start nom_service

**Redémarrer tous les services**
sudo docker compose restart

**Redémarrer un service spécifique**
sudo docker compose restart nom_service

**Voir les logs en temps réel**
sudo docker compose logs -f

**Logs d'un service spécifique**
sudo docker compose logs -f nom_service

**Nettoyer les images inutilisées**
sudo docker image prune -a

**Nettoyage complet (images, conteneurs arrêtés, réseaux, cache)**
sudo docker system prune -a --volumes

**Mettre à jour tous les services**
sudo docker compose pull
sudo docker compose up -d

**Mettre à jour un service spécifique**
sudo docker compose pull nom_service
sudo docker compose up -d nom_service
