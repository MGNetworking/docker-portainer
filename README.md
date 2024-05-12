# Portainer

* [Information projet](#information-projet)
* [Lancement](#lancement)
* [docker compose](#docker-compose)

## Information projet

Ce projet permet de déployer dans un environnement docker le service Portainer Version Community Edition.

## Lancement

Il suffit de lancer la commande suivant :

```shell
docker compose up -d
```

## docker compose

La section volumes définit portainer_data en utilisant `type: none`,`device: $PWD/portainer_data` et `o: bind`

`type:` none indique à Docker de ne pas créer automatiquement le volume, mais d'utiliser le chemin spécifié dans device.

`device:` $PWD/portainer_data utilise le chemin absolu local ($PWD/portainer_data représente le répertoire
portainer_data dans le répertoire actuel où se trouve votre docker-compose.yml).

`o:` bind monte le chemin spécifié ($PWD/portainer_data) dans le conteneur.