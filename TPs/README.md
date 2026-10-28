# TPs : blockchain, D-IAM et apprentissage fédéré (version nettoyée)

Ouvrir `index.html`. Les 8 sujets d'origine sont conservés sous les mêmes noms de fichier.

## Changements communs
- Mise en page unique (`style.css`, mode sombre et impression), HTML valide (listes hors des paragraphes, titres cohérents), structure : objectifs, documentation, travail, rendu.
- Titres corrigés (TP5 s'appelait « Apprentissage fédéré avec FashionMNIST »).
- Dates, dépôts et critères d'évaluation non précisés à l'origine : marqués `[à compléter]`.

## Corrections par document
- **TD FL** : imports manquants (`nn`, `F`) ajoutés ; ligne « Définition du modèle CNN » qui cassait le code (non commentée) corrigée ; client Flower, serveur et `pyproject.toml` ajoutés avec l'API récente (`ClientApp`/`ServerApp`, `flwr run`) à la place de `start_server` / `python server.py`, incohérente avec l'arborescence fournie. `train` et `test` laissés à écrire.
- **TP1** : le contrat s'appelait `SimpleStorage.sol` mais définissait `Storage` ; renommé `Storage.sol`. Ajout d'une commande `curl` JSON-RPC, d'une mise en garde sur la version du tutoriel Besu (23.4.0) et d'indications de vérification.
- **Tuto NFT / TP2** : `js-ipfs` (plus maintenu) remplacé par Kubo + `kubo-rpc-client` ; `create-react-app` + `npm run dev` (incohérents) remplacés par Vite ; Hardhat 2 + toolbox (ethers v6 : `deployContract`, `waitForDeployment`) ; OpenZeppelin 4.9.6 (constructeur `Ownable` différent en v5) ; le NFT n'avait pas d'URI (IPFS inutilisé) : `ERC721URIStorage` et `createNFT(recipient, uri)` ; `evmVersion: "paris"` pour un genesis Besu sans Shanghai ; clé privée via `.env`. Les tests, cités dans les objectifs mais absents des questions, ajoutés à la question 3.
- **TP3** : script de déploiement migré vers ethers v6 ; spécification en tableaux ; choix de conception laissés ouverts listés (délégation, règle ABAC, types de rôles) ; points de sécurité (`tx.origin`, remboursement des enchères, réentrance, événements) ; squelette de tests.
- **TP4** : numérotation (saut du 4 au 5) corrigée ; **Gauss** : l'énoncé parlait de bruit dans les *données* alors que c'est une attaque sur le *modèle* ; **Trim** : l'énoncé la décrivait comme « suppression ou modification extrême de données », alors que c'est l'attaque de Fang et al. (USENIX Security 2020) qui envoie des valeurs opposées à la direction honnête, hors de la plage honnête ; conditions des défenses ajoutées (Multi-Krum : n ≥ 2f+3) ; grille d'expériences ; le lien arXiv 1912.13445 pointait vers un article d'agrégation robuste (Pillutla et al.), non vers un survol : remplacé par Lyu et al. (arXiv 2012.06337) et d'autres références vérifiées.
- **TP5** : tableau « BFL : meilleure précision, sécurité élevée » reformulé en hypothèses à tester (rien ne prouve une meilleure précision) ; architecture on-chain/off-chain, déroulement d'un tour, mesures à rapporter.
- **Projet** : le CNN annoncé n'était pas défini : définition ajoutée dans le TD ; énoncé distingué du TP5 (synthèse TD + TP4 + TP5) : interprétation à confirmer.

## Non vérifié
Je n'ai pas pu exécuter le code (Flower, PyTorch, Hardhat, Besu indisponibles dans l'environnement de génération). Seule la syntaxe Python des extraits a été contrôlée. À tester avant distribution : versions de Flower, `flwr run`, ID du jeu de données `zalando-datasets/fashion_mnist`, compilation du contrat NFT et déploiement sur Besu.
