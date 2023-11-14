# [ESGI] - Projet CI/CD

>- Léo STVENOT
>- Nathan PONCET

## Application : Random number
**Description de l'API Génératrice d'entier Aléatoire**

Cette API JavaScript est accessible depuis le port [3000](http://localhost:3000). 
Elle génère un entier aléatoire compris entre 1 et 100 et le renvoie au format JSON.

**Utilisation :**

- **Endpoint :** `http://localhost:3000`
- **Méthode :** `GET`

**Réponse :**
```json
{
  "min": 1,
  "max": 100,
  "random_number": 42
}
```

## Commandes
### Installation
```shell
npm install
```
### Lint
Lint le fchier [index.js](src/index.js) en mode ES6
```shell
npm run start
```
Lint le Dockerfile
```shell
hadolint Dockerfile
```
### Start
Démarrer l'application sur le port [3000](http://localhost:3000)
```shell
npm run start
```

## Docker
### Build
```
docker build --rm -t youpidok/random-number .
```
### Run
```shell
docker run --name random-number -p 3000:3000 -d youpidok/random-number 
```

## CI/CD