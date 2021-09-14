---
description: CNG fournit un modèle de stockage de clés privées qui permet de s’adapter aux demandes actuelles et futures de la création d’applications qui utilisent des fonctionnalités de chiffrement, telles que le chiffrement à clé publique ou privée, ainsi que les exigences de stockage du matériel de clé.
ms.assetid: 95e5750f-fdc5-41f3-a4ce-9593a7081e95
title: Stockage et récupération de clé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5abfd6319353440c580d53990075a71613a1eba9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013658"
---
# <a name="key-storage-and-retrieval"></a>Stockage et récupération de clé

-   [Architecture des Stockage clés](#key-storage-architecture)
-   [Types de clés](#key-types)
-   [Algorithmes pris en charge](#supported-algorithms)
-   [Répertoires et fichiers de clé](#key-directories-and-files)

## <a name="key-storage-architecture"></a>Architecture des Stockage clés

CNG fournit un modèle de stockage de clés privées qui permet de s’adapter aux demandes actuelles et futures de la création d’applications qui utilisent des fonctionnalités de chiffrement, telles que le chiffrement à clé publique ou privée, ainsi que les exigences de stockage du matériel de clé. Le routeur de stockage de clés est la routine centrale de ce modèle et est implémenté dans Ncrypt.dll. Une application accède aux fournisseurs de stockage de clés (KSP) sur le système via le routeur de stockage de clés, qui masque les détails, tels que l’isolation des clés, à la fois par l’application et le fournisseur de stockage. L’illustration suivante montre la conception et la fonction de l’architecture d’isolation de clé CNG.

![fournisseur de stockage de clés CNG](images/cng-key-storage-provider.png)

Pour respecter les exigences de critères communs (CC), les clés à long terme doivent être isolées afin qu’elles ne soient jamais présentes dans le processus d’application. CNG prend actuellement en charge le stockage des clés privées asymétriques à l’aide du logiciel Microsoft KSP fourni avec Windows Server 2008 et Windows Vista, et est installé par défaut.

l’isolation de clé est activée par défaut dans Windows Server 2008 et Windows Vista. La fonctionnalité d’isolation de clé n’est pas disponible sur les plateformes antérieures à celles-ci. En outre, les KSP tiers ne sont pas chargés dans le service d’isolation de clé (processus LSA). Seul le KSP Microsoft est chargé dans le service d’isolation de clé.

Le processus LSA est utilisé comme processus d’isolation de clé pour optimiser les performances. Tout accès aux clés privées passe par le routeur de stockage de clés, qui expose un ensemble complet de fonctions pour la gestion et l’utilisation des clés privées.

CNG stocke la partie publique de la clé stockée séparément de la partie privée. La partie publique d’une paire de clés est également gérée dans le service d’isolation de clé et est accessible à l’aide d’un appel de procédure distante (LRPC) local. Le routeur de stockage de clés utilise les appels LRPC lors de l’appel au processus d’isolation de clé. Tout accès aux clés privées passe par le routeur de clé privée et est audité par CNG.

Comme décrit ci-dessus, un large éventail de dispositifs de stockage matériel peut être pris en charge. Dans chaque cas, l’interface à tous ces périphériques de stockage est identique. Il comprend des fonctions permettant d’effectuer diverses opérations de clé privée, ainsi que des fonctions relatives au stockage et à la gestion des clés.

CNG fournit un ensemble d’API qui permettent de créer, de stocker et de récupérer des clés de chiffrement. pour obtenir la liste de ces api, consultez [Stockage des fonctions de clé CNG](cng-key-storage-functions.md).

## <a name="key-types"></a>Types de clés

CNG prend en charge les types de clés suivants :

-   Diffie-Hellman des clés publiques et privées.
-   Clés publiques et privées de l’algorithme de signature numérique (DSA, FIPS 186-2).
-   \#Clés publiques et privées RSA (PKCS 1).
-   Plusieurs clés publiques et privées héritées (CryptoAPI).
-   Clés publiques et privées de chiffrement à courbe elliptique.

## <a name="supported-algorithms"></a>Algorithmes pris en charge

CNG prend en charge les algorithmes de clé suivants.

| Algorithm | Longueur de clé/hachage (bits)             |
|-----------|------------------------------------|
| RSA       | 512 à 16384, en incréments de 64 bits |
| VA        | 512 à 16384, en incréments de 64 bits |
| DSA       | 512 à 1024, en incréments de 64 bits  |
| ECDSA     | P-256, P-384, P-521 (courbes NIST)  |
| ECDH      | P-256, P-384, P-521 (courbes NIST)  |
| MD2       | 128                                |
| MD4       | 128                                |
| MD5       | 128                                |
| SHA-1     | 160                                |
| SHA-256   | 256                                |
| SHA-384   | 384                                |
| SHA-512   | 512                                |



 

## <a name="key-directories-and-files"></a>Répertoires et fichiers de clé

Les fournisseurs de services de chiffrement de clés privées Microsoft hérités de Microsoft stockent les clés privées dans les répertoires

| Type de clé                | Répertoires                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Utilisateur privé            | % APPDATA% \\ Microsoft \\ crypto \\ RSA \\ *User sid*\\<br/>% APPDATA% \\ SID de l' \\ \\ \\ *utilisateur* Microsoft crypto DSS\\<br/>                                                   |
| Système local privé    | % ALLUSERSPROFILE% \\ Application Data \\ Microsoft \\ crypto \\ RSA \\ S-1-5-18\\<br/>% ALLUSERSPROFILE% \\ Application Data \\ Microsoft \\ crypto \\ DSS \\ S-1-5-18\\<br/>   |
| Service local privé   | % ALLUSERSPROFILE% \\ Application Data \\ Microsoft \\ crypto \\ RSA \\ S-1-5-19\\<br/>% ALLUSERSPROFILE% \\ Application Data \\ Microsoft \\ crypto \\ DSS \\ S-1-5-19\\<br/>   |
| Service réseau privé | % ALLUSERSPROFILE% \\ Application Data \\ Microsoft \\ crypto \\ RSA \\ S-1-5-20\\<br/>% ALLUSERSPROFILE% \\ Application Data \\ Microsoft \\ crypto \\ DSS \\ S-1-5-20\\<br/>   |
| Privé partagé          | % ALLUSERSPROFILE% \\ Application Data \\ Microsoft \\ crypto \\ RSA \\ MachineKeys<br/>% ALLUSERSPROFILE% \\ Application Data \\ Microsoft \\ crypto \\ DSS \\ MachineKeys<br/> |



 

CNG stocke les clés privées dans les répertoires suivants.

| Type de clé                | Répertoire                                                          |
|-------------------------|--------------------------------------------------------------------|
| Utilisateur privé            | % APPDATA% \\ des \\ clés de chiffrement Microsoft \\                                 |
| Système local privé    | % ALLUSERSPROFILE% de \\ données d’application \\ Microsoft \\ crypto \\ SystemKeys |
| Service local privé   | % WINDIR% \\ ServiceProfiles \\ LocalService                            |
| Service réseau privé | % WINDIR% \\ ServiceProfiles \\ NetworkService                          |
| Privé partagé          | % ALLUSERSPROFILE% des \\ clés de \\ \\ chiffrement Microsoft des données d’application \\       |



 

Voici quelques-unes des différences entre les conteneurs de clé CryptoAPI et CNG.

-   CNG utilise des noms de fichiers différents pour les fichiers de clé que les fichiers de clé créés par le Rsaenh.dll et Dssenh.dll les fournisseurs de services de chiffrement hérités. Les fichiers de clés hérités ont également l’extension. Key, mais les fichiers de clé CNG n’ont pas l’extension. Key.
-   CNG prend entièrement en charge les noms de conteneurs de clés Unicode. CNG utilise un hachage du nom de conteneur Unicode, tandis que CryptoAPI utilise un hachage du nom de conteneur ANSI.
-   CNG est plus flexible en ce qui concerne les paires de clés RSA. Par exemple, CNG prend en charge les exposants publics d’une longueur supérieure à 32 bits et prend en charge les clés dans lesquelles p et q sont des longueurs différentes.
-   Dans CryptoAPI, le fichier de conteneur de clé est stocké dans un répertoire dont le nom est l’équivalent textuel du SID de l’utilisateur. Ce n’est plus le cas dans CNG, ce qui élimine la difficulté de déplacer des utilisateurs d’un domaine à un autre sans perdre toutes leurs clés privées.
-   Le KSP et les noms de clé CNG sont limités aux caractères Unicode du **\_ chemin d’accès maximal** . Le fournisseur de services de chiffrement CryptoAPI et les noms de clé sont limités aux caractères ANSI du **\_ chemin d’accès maximal** .
-   CNG offre des propriétés de clé définies par l’utilisateur. Les utilisateurs peuvent créer et associer des propriétés personnalisées à des clés et les stocker avec des clés persistantes.

Lors de la persistance d’une clé, CNG peut créer deux fichiers. Le premier fichier contient la clé privée dans le nouveau format CNG et est toujours créé. Ce fichier n’est pas utilisable par les fournisseurs de services de chiffrement CryptoAPI hérités. Le deuxième fichier contient la même clé privée dans le conteneur de clé CryptoAPI hérité. Le deuxième fichier est conforme au format et à l’emplacement utilisés par Rsaenh.dll. La création du deuxième fichier se produit uniquement si l’indicateur **\_ \_ de clé d’écriture NCRYPT de l’indicateur \_ de \_ \_ magasin \_ hérité** est spécifié lors de l’appel de la fonction [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) pour finaliser une clé RSA. Cette fonctionnalité n’est pas prise en charge pour les clés DSA et DH.

Lorsqu’une application tente d’ouvrir une clé persistante existante, CNG tente d’abord d’ouvrir le fichier CNG natif. Si ce fichier n’existe pas, CNG tente de localiser une clé correspondante dans le conteneur de clé CryptoAPI hérité.

lorsque vous déplacez ou copiez des clés CryptoAPI d’un ordinateur source vers un ordinateur cible avec Outil de migration utilisateur Windows (USMT), CNG ne parvient pas à accéder aux clés sur l’ordinateur cible. Pour accéder à ces clés migrées, vous devez utiliser l’CryptoAPI.

 

 




