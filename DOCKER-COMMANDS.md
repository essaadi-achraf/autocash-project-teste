# 🐳 Commandes Docker - Autocash

## 1️⃣ Build de l'image Docker

```bash
docker build -t autocash-app .
```

Ou avec Docker Compose :

```bash
docker-compose build
```

---

## 2️⃣ Lancement de l'application

**Avec Docker Compose (recommandé) :**

```bash
docker-compose up -d
```

**Avec Docker directement :**

```bash
docker run -d --name autocash-app -p 8080:8080 autocash-app
```

---

## 3️⃣ Vérification que l'application fonctionne

**Tester l'endpoint :**

```bash
curl http://localhost:8080/hello
```

Ou ouvrir dans le navigateur : http://localhost:8080/hello

**Voir les logs :**

```bash
docker-compose logs -f autocash-app
```

Ou avec Docker :

```bash
docker logs -f autocash-app
```

---

## 4️⃣ Arrêt des conteneurs

**Avec Docker Compose :**

```bash
docker-compose down
```

**Avec Docker directement :**

```bash
docker stop autocash-app
docker rm autocash-app
```

---

## 📋 Commandes utiles supplémentaires

**Rebuild complet (sans cache) :**

```bash
docker-compose build --no-cache
docker-compose up -d
```

**Voir les conteneurs en cours d'exécution :**

```bash
docker ps
```

**Accéder au shell du conteneur :**

```bash
docker exec -it autocash-app sh
```

**Nettoyer les images inutilisées :**

```bash
docker image prune -a
```
