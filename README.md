# TP 01 — Jeu de piste HTTP

Ce dépôt documente la résolution du jeu de piste sur les protocoles et requêtes HTTP réalisé avec le client d'API **Bruno**.

---

## Sommaire
- [Étape 0 — Introduction au protocole](#étape-0--introduction-au-protocole)
- [Étape 1 — Paramètre simple dans l'URL](#étape-1--paramètre-simple-dans-lurl)
- [Étape 2 — Multiples paramètres d'URL (Query Params)](#étape-2--multiples-paramètres-durl-query-params)
- [Étape 3 — Découverte de la méthode POST](#étape-3--découverte-de-la-méthode-post)
- [Étape 4 — En-tête Content-Type](#étape-4--en-tête-content-type)
- [Étape 5 — Méthode PUT et négociation de contenu (Accept)](#étape-5--méthode-put-et-négociation-de-contenu-accept)
- [Étape 6 — Méthode DELETE et paramètres](#étape-6--méthode-delete-et-paramètres)
- [Étape 7 — Méthode PATCH et transmission d'un Body JSON](#étape-7--méthode-patch-et-transmission-dun-body-json)
- [Étape 8 — Finalisation : En-têtes personnalisés et Authentification](#étape-8--finalisation--en-têtes-personnalisés-et-authentification)

---

### Étape 0 — Introduction au protocole

* **Méthode :** `GET`
* **URL :** `http://172.16.3.254:8001/bienvenue`
* **Objectif :** Initialisation du jeu de piste et récupération des consignes pour la première étape.

![Capture Étape 0](<Etape 0.png>)

---

### Étape 1 — Paramètre simple dans l'URL

* **Méthode :** `GET`
* **URL :** `http://172.16.3.254:8001/decouverte-des-parametres?nom=Awaiye`
* **Paramètres (Query Params) :**
  * `nom` : `Awaiye`

![Capture Étape 1](<Etape 1.png>)

---

### Étape 2 — Multiples paramètres d'URL (Query Params)

* **Méthode :** `GET`
* **URL :** `http://172.16.3.254:8001/plusieurs-parametres?nom=Awaiye&prenom=Jad&age=19`
* **Paramètres (Query Params) :**
  * `nom` : `Awaiye`
  * `prenom` : `Jad`
  * `age` : `19`

![Capture Étape 2](<Etape 2.png>)
---

### Étape 3 — Découverte de la méthode POST

* **Méthode :** `POST`
* **URL :** `http://172.16.3.254:8001/un-peu-de-post`
* **Objectif :** Utiliser la méthode `POST` pour initier l'envoi de données vers le serveur.

![Capture Étape 3](<Etape 3.png>)

---

### Étape 4 — En-tête Content-Type

* **Méthode :** `POST`
* **URL :** `http://172.16.3.254:8001/5-content-type`
* **En-têtes (Headers) :**
  * `Content-Type` : `application/json`

![Capture Étape 4](<Etape 4.png>)

---

### Étape 5 — Méthode PUT et négociation de contenu (Accept)

* **Méthode :** `PUT`
* **URL :** `http://172.16.3.254:8001/put-method-6`
* **En-têtes (Headers) :**
  * `Content-Type` : `text/html`
  * `Accept` : `application/json`

![Capture Étape 5](<Etape 5.png>)

---

### Étape 6 — Méthode DELETE et paramètres

* **Méthode :** `DELETE`
* **URL :** `http://172.16.3.254:8001/et-oui-delete?filename=filename`
* **Paramètres (Query Params) :**
  * `filename` : `filename`

![Capture Étape 6](<Etape 6.png>)

---

### Étape 7 — Méthode PATCH et transmission d'un Body JSON

* **Méthode :** `PATCH`
* **URL :** `http://172.16.3.254:8001/etape8/api/users/12345`
* **En-têtes (Headers) :**
  * `Content-Type` : `application/json`
* **Corps de la requête (JSON Body) :**
  ```json
  {
    "role": "Developer",
    "email": "jagh@gmail.com"
  }

![Capture Étape 7](<Etape 7.png>)

---

### Étape 8 — Finalisation : En-têtes personnalisés et Authentification

* **Méthode :** `POST`
* **URL :** `http://172.16.3.254:8001/etape9`
* **En-têtes (Headers) :**
  * `Content-Type` : `application/json`
  * `api-key` : `FenelonBTSSIO`
  * `User-Agent` : `FenelonBTSSIO-UserAgent-LaRochelle-v1.0`
* **Corps de la requête (JSON Body) :**
  ```json
  {
    "name": "Donald Duck"
  }

![Capture Étape 8](<Etape 8.png>)