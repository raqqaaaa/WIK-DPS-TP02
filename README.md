# Projet API - TP 2

### **GET /ping**
- **Réponse :** JSON contenant les headers HTTP de la requête, code **200**

Exemple de réponse :
```json
{
  "host": "localhost:3000",
  "user-agent": "curl/7.88.1",
  "accept": "*/*"
}
```
Tout autre verbe HTTP et/ou route donne un code 404 avec une réponse vide.

### ⚡ Mise à jour dans le TP 2

Ce deuxième TP contient deux Dockerfiles permettant de lancer notre application :

Dockerfile : contient un seul stage

Dockerfile.multi : contient deux stages afin de séparer les étapes de build et d'exécution

### 🛠️ Comment lancer le projet ?
## 🔐 Version Single Stage

```sh
docker build --no-cache -f Dockerfile -t api-single .
docker run -d -p 3000:3000 --name single api-single
docker rm -f single
```

## 🔐 Version Multi Stage
```sh
docker build --no-cache -f Dockerfile.multi -t api-multi .
docker run -d -p 3000:3000 --name multi api-multi
docker rm -f multi
```
