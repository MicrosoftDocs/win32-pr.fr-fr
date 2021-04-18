---
description: Explique l’architecture système CryptoAPI.
ms.assetid: 244329bb-fc71-4ab9-8831-a9478108ffa3
title: Architecture du système CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d5dcf1756c9b581d75d4e52d57fbce089976a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318233"
---
# <a name="cryptoapi-system-architecture"></a>Architecture du système CryptoAPI

L’architecture système CryptoAPI est composée de cinq domaines fonctionnels majeurs :

-   [Fonctions de chiffrement de base](#base-cryptographic-functions)
-   [Fonctions de codage/décodage de certificat](#certificate-encodedecode-functions)
-   [Fonctions du magasin de certificats](#certificate-store-functions)
-   [Fonctions de message simplifiées](#simplified-message-functions)
-   [Fonctions de message de bas niveau](#low-level-message-functions)

## <a name="base-cryptographic-functions"></a>Fonctions de chiffrement de base

-   *Fonctions de contexte* utilisées pour se connecter à un CSP. Ces fonctions permettent aux applications de choisir un CSP spécifique par nom ou de choisir un CSP spécifique qui peut fournir une classe de fonctionnalité nécessaire.
-   [*Fonctions de génération de clés*](../secgloss/k-gly.md) utilisées pour générer et stocker des [*clés de chiffrement*](../secgloss/c-gly.md). La prise en charge complète est incluse pour la modification des [*modes de chaînage*](../secgloss/c-gly.md), des [*vecteurs d’initialisation*](../secgloss/i-gly.md)et d’autres fonctionnalités de chiffrement. Pour plus d’informations, consultez [génération de clés et fonctions d’échange](cryptography-functions.md).
-   *Fonctions d’échange de clés* utilisées pour échanger ou transmettre des clés. Pour plus d’informations, consultez [stockage de clé de chiffrement et Exchange](cryptographic-key-storage-and-exchange.md) , [génération de clés et fonctions Exchange](cryptography-functions.md).

## <a name="certificate-encodedecode-functions"></a>Fonctions de codage/décodage de certificat

-   Fonctions utilisées pour chiffrer ou déchiffrer des données. La prise en charge est également incluse pour le [*hachage*](../secgloss/h-gly.md) des données. Pour plus d’informations, consultez [fonctions de chiffrement et](cryptography-functions.md) de déchiffrement des données et [chiffrement et déchiffrement des données](data-encryption-and-decryption.md).

## <a name="certificate-store-functions"></a>Fonctions du magasin de certificats

-   Fonctions utilisées pour gérer les collections de certificats numériques. Pour plus d’informations, consultez [certificats numériques](digital-certificates.md) et [fonctions du magasin de certificats](cryptography-functions.md).

## <a name="simplified-message-functions"></a>Fonctions de message simplifiées

-   Fonctions utilisées pour chiffrer et déchiffrer les messages et les données.
-   Fonctions utilisées pour signer les messages et les données.
-   Fonctions utilisées pour vérifier l’authenticité des signatures sur les messages reçus et les données associées.

Pour plus d’informations, consultez [messages simplifiés](simplified-messages.md) et [fonctions de message simplifiées](cryptography-functions.md).

## <a name="low-level-message-functions"></a>Fonctions de message de bas niveau

-   Fonctions utilisées pour effectuer toutes les tâches effectuées par les fonctions de message simplifiées. Les fonctions de message de bas niveau offrent plus de flexibilité que les fonctions de message simplifiées, mais nécessitent davantage d’appels de fonction. Pour plus d’informations, consultez [messages de bas niveau](low-level-messages.md) et [fonctions de message de bas niveau](cryptography-functions.md).

![architecture CryptoAPI](images/cryparch.png)

Chacune des zones fonctionnelles a un mot clé dans son nom de fonction qui indique sa zone fonctionnelle.



| Zone fonctionnelle              | Convention de nom de fonction |
|------------------------------|--------------------------|
| Fonctions de chiffrement de base | Compliqué                    |
| Fonctions d’encodage/décodage  | Compliqué                    |
| Fonctions du magasin de certificats  | Magasin                    |
| Fonctions de message simplifiées | Message                  |
| Fonctions de message de bas niveau  | Fragment                      |



 

Les applications utilisent des fonctions dans tous ces domaines. Ces fonctions, prises ensemble, composent CryptoAPI. Les [*fonctions de chiffrement de base*](../secgloss/b-gly.md) utilisent les CSP pour les algorithmes de chiffrement nécessaires et pour la génération et le stockage sécurisé des [clés de chiffrement](cryptographic-keys.md).

Deux types de clés de chiffrement sont utilisés : les [*clés de session*](../secgloss/s-gly.md), qui sont utilisées pour un chiffrement/déchiffrement unique, et les [*paires de clés publique/privée*](../secgloss/p-gly.md), qui sont utilisées de façon plus permanente.

> [!Note]  
> Bien qu’une application puisse communiquer directement avec l’une des cinq zones fonctionnelles, elle ne peut pas communiquer directement avec un CSP. Toutes les communications entre les applications et CSP se produisent par le biais des [*fonctions de chiffrement de base*](../secgloss/b-gly.md). Les fonctions de chiffrement de base ont un paramètre qui spécifie le fournisseur de services de chiffrement à utiliser. Ce paramètre peut avoir la valeur **null** pour sélectionner un CSP par défaut.

 

 

 
