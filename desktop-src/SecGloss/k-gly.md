---
description: Contient les définitions des termes de sécurité qui commencent par la lettre K.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f17042c3-ba1a-408f-af55-5f171b0dee33
title: K (Glossaire de la sécurité)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e7d1b474b774b5cdb7a0b8d05a512a8d291573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952376"
---
# <a name="k-security-glossary"></a>K (Glossaire de la sécurité)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J K [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_kca_gly"></span><span id="_SECURITY_KCA_GLY"></span>**KCA**
</dt> <dd>

Consultez *autorité de certification de clé*.

</dd> <dt>

<span id="_security_kdc_gly"></span><span id="_SECURITY_KDC_GLY"></span>**Centre**
</dt> <dd>

Consultez *Centre de distribution de clés*.

</dd> <dt>

<span id="_security_kea_gly"></span><span id="_SECURITY_KEA_GLY"></span>**KEA**
</dt> <dd>

Consultez *algorithme d’échange de clés*.

</dd> <dt>

<span id="_security_kerberos_protocol_gly"></span><span id="_SECURITY_KERBEROS_PROTOCOL_GLY"></span>**Protocole Kerberos**
</dt> <dd>

Protocole qui définit comment les clients interagissent avec un service d'authentification de réseau. Les clients obtiennent des tickets du centre de distribution de clés Kerberos (KDC), et ils présentent ces tickets aux serveurs lorsque les connexions sont établies. Les tickets Kerberos représentent les informations d'identification réseau du client.

</dd> <dt>

<span id="_security_key_blob_gly"></span><span id="_SECURITY_KEY_BLOB_GLY"></span>**objet BLOB de clé**
</dt> <dd>

Objet BLOB contenant une clé privée chiffrée. Les objets BLOB de clé offrent un moyen de stocker les clés en dehors du CSP. Les objets BLOB de clé sont créés en exportant une clé existante à partir du CSP en appelant la fonction **CryptExportKey** . Plus tard, l’objet BLOB de clé peut être importé dans un fournisseur (souvent un CSP différent sur un autre ordinateur) en appelant la fonction **CryptImportKey** . Cela crée dans le CSP une clé qui est un doublon de celle qui a été exportée.

Voir aussi [*objet blob de clé simple*](s-gly.md), objet blob de clé [*publique*](p-gly.md)et [*objet blob de clé privée*](p-gly.md).

</dd> <dt>

<span id="_security_key_blob_format_gly"></span><span id="_SECURITY_KEY_BLOB_FORMAT_GLY"></span>**format BLOB de clé**
</dt> <dd>

Format de l’objet BLOB de clé lorsqu’une clé publique ou de session est exportée à partir d’un fournisseur de services de chiffrement. Le format est spécifié par le type de fournisseur du CSP exportateur. Un objet BLOB de clé est créé en appelant **CryptExportKey**.

Voir aussi [*blob de clé publique*](p-gly.md) et [*objet blob de clé simple*](s-gly.md).

</dd> <dt>

<span id="_security_key_certification_authority_gly"></span><span id="_SECURITY_KEY_CERTIFICATION_AUTHORITY_GLY"></span>**autorité de certification de clé**
</dt> <dd>

(KCA) Entité approuvée qui conserve généralement une base de données sécurisée de messages composés signés avec la clé privée de KCA. Dans les implémentations pratiques, les messages composés sont constitués du nom de l’utilisateur, de la clé publique de l’utilisateur et de toute autre information importante sur l’utilisateur. Lorsque l’application réceptrice reçoit un message signé d’un utilisateur, l’application peut ensuite vérifier la clé publique reçue avec le message en la comparant à la clé publique stockée dans la base de données KCA.

</dd> <dt>

<span id="_security_key_container_gly"></span><span id="_SECURITY_KEY_CONTAINER_GLY"></span>**conteneur de clé**
</dt> <dd>

Partie de la base de données de clé qui contient toutes les paires de clés (les paires de clés de signature et d’échange) appartenant à un utilisateur spécifique. Chaque conteneur a un nom unique qui est utilisé lors de l’appel de la fonction **CryptAcquireContext** pour obtenir un handle vers le conteneur.

</dd> <dt>

<span id="_security_key_database_gly"></span><span id="_SECURITY_KEY_DATABASE_GLY"></span>**base de données clé**
</dt> <dd>

Base de données qui contient les clés de chiffrement persistantes pour un CSP spécifique. La base de données contient un ou plusieurs conteneurs de clé, qui stockent individuellement toutes les paires de clés de chiffrement pour un utilisateur spécifique.

Voir aussi *conteneur de clé*.

</dd> <dt>

<span id="_security_key_distribution_center_gly"></span><span id="_SECURITY_KEY_DISTRIBUTION_CENTER_GLY"></span>**centre de distribution de clés**
</dt> <dd>

Centre Service réseau qui fournit des tickets de session et des clés de session temporaires utilisés dans le protocole d’authentification Kerberos V5. Le KDC s’exécute en tant que processus privilégié sur tous les contrôleurs de domaine.

Voir aussi *protocole Kerberos*.

</dd> <dt>

<span id="_security_key_exchange_algorithm_gly"></span><span id="_SECURITY_KEY_EXCHANGE_ALGORITHM_GLY"></span>**algorithme d’échange de clés**
</dt> <dd>

Algorithme utilisé pour chiffrer et déchiffrer les clés d’échange (clés de session symétrique). Parmi les algorithmes d’échange de clés courants, citons Diffie-Hellman et KEA, l’algorithme d’échange de clés spécifié par un \_ type de fournisseur Fortezza. L’algorithme KEA est une version améliorée de l’algorithme Diffie-Hellman. Chaque type de fournisseur ne peut spécifier qu’un seul algorithme d’échange de clés.

</dd> <dt>

<span id="_security_key_exchange_algorithm_name_gly"></span><span id="_SECURITY_KEY_EXCHANGE_ALGORITHM_NAME_GLY"></span>**Algorithme d’échange de clés**
</dt> <dd>

(KEA) Algorithme d’échange de clés spécifié par un \_ type de fournisseur Fortezza. Cet algorithme est une version améliorée de l’algorithme Diffie-Hellman.

</dd> <dt>

<span id="_security_key_exchange_certificate_gly"></span><span id="_SECURITY_KEY_EXCHANGE_CERTIFICATE_GLY"></span>**certificat d’échange de clés**
</dt> <dd>

Certificat utilisé pour chiffrer les informations envoyées à un autre tiers. Le certificat d’échange de clés de l’autorité de certification (CA) peut être utilisé par un client pour chiffrer les informations envoyées à l’autorité de certification.

</dd> <dt>

<span id="_security_key_exchange_functions_gly"></span><span id="_SECURITY_KEY_EXCHANGE_FUNCTIONS_GLY"></span>**fonctions d’échange de clés**
</dt> <dd>

Ensemble de fonctions utilisées pour échanger ou transmettre des clés. Les fonctions d’échange de clés peuvent également être utilisées pour implémenter des échanges de clé en trois phases entièrement authentifiés.

</dd> <dt>

<span id="_security_key_exchange_key_pair_gly"></span><span id="_SECURITY_KEY_EXCHANGE_KEY_PAIR_GLY"></span>**paire de clés d’échange de clés**
</dt> <dd>

Consultez [*paire de clés Exchange*](e-gly.md).

</dd> <dt>

<span id="_security_key_exchange_private_key_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PRIVATE_KEY_GLY"></span>**clé privée d’échange de clés**
</dt> <dd>

Clé privée d’une paire de clés d’échange.

Voir aussi [*paire de clés Exchange*](e-gly.md).

</dd> <dt>

<span id="_security_key_exchange_protocol_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PROTOCOL_GLY"></span>**protocole d’échange de clés**
</dt> <dd>

Protocole par lequel deux parties échangent des informations pour établir un secret partagé. Le secret partagé est généralement utilisé en tant que clé de chiffrement symétrique.

</dd> <dt>

<span id="_security_key_exchange_public_key_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PUBLIC_KEY_GLY"></span>**clé publique d’échange de clés**
</dt> <dd>

Clé publique d’une paire de clés d’échange.

Voir aussi [*paire de clés Exchange*](e-gly.md).

</dd> <dt>

<span id="_security_key_generation_functions_gly"></span><span id="_SECURITY_KEY_GENERATION_FUNCTIONS_GLY"></span>**fonctions de génération de clés**
</dt> <dd>

Ensemble de fonctions utilisées par les applications pour générer et personnaliser des clés de chiffrement. Ces fonctions incluent une prise en charge complète de la modification des modes de chaînage, des vecteurs d’initialisation et d’autres fonctionnalités de chiffrement.

</dd> <dt>

<span id="_security_key_length_gly"></span><span id="_SECURITY_KEY_LENGTH_GLY"></span>**longueur de la clé**
</dt> <dd>

Valeurs spécifiées par certains fournisseurs qui indiquent la longueur des paires de clés publiques/privées et des clés de session utilisées avec ce fournisseur.

</dd> <dt>

<span id="_security_key_pair_gly"></span><span id="_SECURITY_KEY_PAIR_GLY"></span>**paire de clés**
</dt> <dd>

Une clé privée et la clé publique associée.

</dd> <dt>

<span id="_security_key_storage_provider_gly"></span><span id="_SECURITY_KEY_STORAGE_PROVIDER_GLY"></span>**fournisseur de stockage de clés**
</dt> <dd>

KSP Module logiciel indépendant qui implémente des fonctionnalités permettant de créer, de gérer, de stocker et de récupérer des [*clés privées*](p-gly.md).

</dd> <dt>

<span id="_security_ksp_gly"></span><span id="_SECURITY_KSP_GLY"></span>**KSP**
</dt> <dd>

Consultez *fournisseur de stockage de clés*.

</dd> </dl>

 

 



