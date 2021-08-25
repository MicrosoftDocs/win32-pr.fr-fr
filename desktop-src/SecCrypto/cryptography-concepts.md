---
description: 'La communication sécurisée sur des réseaux non sécurisés implique généralement trois principaux domaines de préoccupation : la confidentialité, l’authentification et l’intégrité.'
ms.assetid: bfffe87d-8392-4b4a-8bbc-01b9c13fba47
title: Concepts de chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1909cf999bd5eb2f91bd5c7e0243b13969e692792c4ff32804e7c9a7d2940b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876153"
---
# <a name="cryptography-concepts"></a>Concepts de chiffrement

La communication sécurisée sur des réseaux non sécurisés implique généralement trois principaux domaines de préoccupation : la [confidentialité](#privacy), [l’authentification](#authentication)et [l’intégrité](#integrity). L’API de chiffrement Microsoft ([*CryptoAPI*](../secgloss/c-gly.md)) est un ensemble de fonctions, d’interfaces et d’outils que les applications peuvent utiliser pour améliorer la confiance de la sécurité dans ces domaines.

Outre les fonctionnalités de confidentialité, d’authentification et d’intégrité, [*CryptoAPI*](../secgloss/c-gly.md) fournit également les éléments suivants :

-   Encodage des messages au format ASN. 1 ( [*Abstract Syntax Notation One*](../secgloss/a-gly.md) ).
-   Décodage des messages ASN. 1.
-   Gestion des regroupements de [*certificats*](../secgloss/c-gly.md) dans les [*magasins de certificats*](../secgloss/c-gly.md).
-   Utilisation des [*listes*](../secgloss/c-gly.md) de certificats de confiance et des chaînes de certificats pour vérifier la validité des certificats.

## <a name="privacy"></a>Confidentialité

Pour garantir la confidentialité, les utilisateurs doivent empêcher quiconque à l’exception du destinataire prévu de lire un message. L’amélioration de la probabilité de confidentialité implique généralement l’utilisation d’une forme de [*chiffrement*](../secgloss/c-gly.md). Les techniques de chiffrement sont utilisées pour chiffrer (brouiller) les messages avant leur stockage et leur transmission.

Le chiffrement des données transforme le [*texte en clair*](../secgloss/p-gly.md) en texte [*chiffré*](../secgloss/c-gly.md). Les données à chiffrer peuvent être du texte [*ASCII*](../secgloss/a-gly.md) , un fichier de base de données ou toute autre donnée. Dans cette documentation, le terme [*message*](../secgloss/m-gly.md) est utilisé pour faire référence à n’importe quel élément de données, le texte en clair fait référence à des données qui n’ont pas été chiffrées, et le *texte chiffré* fait référence aux données qui ont été chiffrées. Un bon système de chiffrement de données rend difficile la transformation des données chiffrées en texte en clair sans clé secrète.

Les données chiffrées peuvent être stockées sur un support non sécurisé ou transmises sur un réseau non sécurisé. Plus tard, les données peuvent être déchiffrées dans leur forme d’origine. Ce processus est illustré dans l’illustration suivante.

![contribuer à conserver la confidentialité tout au long du chiffrement et du déchiffrement](images/capi01.png)

Lorsque les données sont chiffrées, le message et une clé de [*chiffrement*](../secgloss/e-gly.md) sont passés à l’algorithme de chiffrement. Pour déchiffrer les données, le texte chiffré et une clé de [*déchiffrement*](../secgloss/d-gly.md) sont passés à l’algorithme de déchiffrement. Le chiffrement et le déchiffrement peuvent être effectués à l’aide d’une clé unique dans un processus appelé chiffrement symétrique.

Les clés utilisées pour déchiffrer un message doivent être gardées comme secrètes et sécurisées, et doivent être transmises à d’autres utilisateurs à l’aide de techniques d’amélioration de la sécurité. Ce sujet est abordé plus en détail dans [chiffrement et déchiffrement des données](data-encryption-and-decryption.md). Le principal défi consiste à limiter l’accès à la clé de déchiffrement, car quiconque le possède pourra déchiffrer tous les messages qui ont été chiffrés avec sa clé de chiffrement correspondante.

Pour répondre aux objectifs de confidentialité énoncés, les développeurs peuvent utiliser [*CryptoAPI*](../secgloss/c-gly.md) pour chiffrer et signer numériquement les données de manière flexible, tout en aidant à fournir une protection pour les données sensibles de la clé privée de l’utilisateur.

[*CryptoAPI*](../secgloss/c-gly.md) fournit les zones de fonctionnalités suivantes pour effectuer les tâches de chiffrement/déchiffrement, de signature de messages et de stockage de clés :

-   [Fonctions de chiffrement de base](cryptography-functions.md)
-   [Fonctions de message simplifiées](cryptography-functions.md)
-   [Fonctions de message de bas niveau](cryptography-functions.md)

## <a name="authentication"></a>Authentification

Les communications sécurisées requièrent que les personnes communiquant connaissent l’identité de ceux avec lesquels ils communiquent. L’authentification est le processus de vérification de l’identité d’une personne ou d’une entité.

Par exemple, dans la durée de vie quotidienne, la documentation physique, souvent appelée informations d’identification, est utilisée pour vérifier l’identité d’une personne. Lorsqu’une vérification est encaissée, la personne qui le contrôle peut demander à voir la licence d’un pilote. La licence du pilote est un document physique qui augmente la confiance du commerçant dans l’identité de la personne qui prolonge la vérification. Dans ce cas, la personne qui prolancera la vérification approuve que l’État émettant la licence a vérifié correctement l’identité du titulaire de la licence.

Les passeports fournissent un autre exemple. Un fonctionnaire douanier examine un passeport et l’accepte comme preuve qu’une personne est l’auteur du message. L’approbation officielle que le gouvernement a fait un travail suffisant pour identifier le détenteur de Passport avant d’émettre le passeport. Dans les deux exemples, un niveau d’approbation existe dans l’émetteur du document physique.

L’authentification implique également de s’assurer que les données reçues sont celles qui ont été envoyées. Si le tiers A envoie un message au tiers B, le tiers B doit être en mesure de prouver que le message reçu était le message envoyé par le tiers et non un message qui a été remplacé pour ce message. Pour fournir cette forme d’authentification, [*CryptoAPI*](../secgloss/c-gly.md) fournit des fonctions pour la signature des données et la vérification des signatures à l’aide de paires de clés publiques/privées.

Étant donné que les communications sur un réseau informatique sont effectuées sans aucun contact physique entre les communicateurs, la vérification de l’identité dépend souvent d’informations d’identification qui peuvent être envoyées et reçues sur un réseau. Ces informations d’identification doivent être émises par un émetteur approuvé des informations d’identification. Les certificats numériques, communément appelés certificats, sont simplement des informations d’identification. Il s’agit d’un moyen de vérifier l’identité et d’obtenir une authentification sur un réseau informatique.

Un certificat numérique est une information d’identification émise par une organisation ou une entité approuvée appelée autorité de certification (CA). Cette information d’identification contient une clé publique (voir les [paires de clés publiques/privées](public-private-key-pairs.md)) et des données qui identifient le sujet du certificat. Un certificat est émis par une autorité de certification uniquement une fois que l’autorité de certification a vérifié l’identité du sujet du certificat et a confirmé que la clé publique incluse avec le certificat appartient à cet objet.

La communication entre une autorité de certification et un demandeur de certificat peut être effectuée par le demandeur qui transporte physiquement les informations nécessaires, éventuellement stockées sur une disquette, à l’autorité de certification. Toutefois, la communication est généralement effectuée avec un message signé envoyé sur un réseau. L’autorité de certification utilise souvent une application approuvée appelée serveur de certificats pour délivrer des certificats.

[*CryptoAPI*](../secgloss/c-gly.md) prend en charge l’authentification via l’utilisation de certificats numériques, avec des fonctions de codage/décodage de certificats et des fonctions de [*magasin de certificats*](../secgloss/c-gly.md) .

Pour plus d’informations sur la vérification d’identité et l’authentification par le biais de l’utilisation de certificats, consultez [certificats numériques](digital-certificates.md).

## <a name="integrity"></a>Intégrité

Toutes les données envoyées sur un support non sécurisé peuvent être modifiées par accident ou à la fin de l’utilisation. Dans le monde réel, les scellements servent à fournir et à prouver l’intégrité. Une bouteille de Aspirin, par exemple, peut se trouver dans un emballage inviolable qui a un sceau non brisé pour prouver que rien n’a été placé dans le package une fois que le package a quitté le fabricant.

De la même manière, un récepteur de données doit être en mesure de vérifier l’identité de l’expéditeur des données et de s’assurer que les données reçues sont exactement les données qui ont été envoyées. autrement dit, il n’a pas été falsifié. L’établissement de l' [*intégrité*](../secgloss/i-gly.md) des données reçues est souvent effectué en envoyant non seulement les données d’origine, mais également un message de vérification, appelé [*hachage*](../secgloss/h-gly.md), à propos de ces données. Les données et le message de vérification peuvent être envoyés avec une [*signature numérique*](../secgloss/d-gly.md) qui prouve l’origine des deux.

L’intégrité est fournie dans CryptoAPI au moyen d’une [signature numérique](digital-signatures.md) et de [hachages de données](data-hashes.md).

[*CryptoAPI*](../secgloss/c-gly.md) prend en charge l’intégrité via l’utilisation de fonctions de message pour signer des données et vérifier les signatures numériques.

 

 
