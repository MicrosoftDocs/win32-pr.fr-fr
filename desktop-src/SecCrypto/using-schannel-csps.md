---
description: Le moteur de protocole SSL (SChannel) utilise un fournisseur de services de chiffrement (CSP) pour effectuer des opérations de chiffrement. Les applications de chiffrement peuvent appeler CryptAcquireContext à l’aide des \_ \_ fournisseurs RSA SChannel et Prov \_ DH \_ Schannel.
ms.assetid: ad1eabf1-23bc-4d23-8f8b-13f0bda95120
title: Utilisation des fournisseurs de services de chiffrement Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289ed57d9f312ee1ef57aecf7534a8d585859126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534381"
---
# <a name="using-schannel-csps"></a>Utilisation des fournisseurs de services de chiffrement Schannel

Le moteur de protocole SSL ([*Schannel*](../secgloss/s-gly.md)) utilise un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) pour effectuer des opérations de chiffrement. Les applications de chiffrement peuvent appeler [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) à l’aide des \_ \_ fournisseurs RSA SChannel et Prov \_ DH \_ Schannel.

Cette section définit les [*types CSP*](../secgloss/c-gly.md) RSA et Diffie-Hellman Schannel, et décrit les fonctionnalités qu’un fournisseur de services de chiffrement doit prendre en charge pour être compatible avec Schannel.dll, le moteur de protocole de chiffrement. Un moteur de protocole est un programme qui établit un canal de communication sécurisé entre une application cliente et serveur.

Les applications ne doivent pas essayer d’utiliser les informations de cette documentation pour utiliser PROV- \_ RSA \_ Schannel ou Prov \_ DH \_ Schannel directement. Au lieu de cela, cette documentation explique comment les développeurs et les fournisseurs CSP doivent écrire des fournisseurs de services de chiffrement Schannel compatibles avec les fournisseurs Microsoft Schannel.

Cette documentation est destinée à aider les développeurs CSP à implémenter des fournisseurs de services de chiffrement RSA ou Diffie-Hellman Schannel compatibles. Les développeurs sont censés être familiarisés avec le protocole SSL ( [*Secure Socket Layer*](../secgloss/s-gly.md) ) version 3,0, le chiffrement à [*clé publique*](../secgloss/p-gly.md) , les [*certificats numériques*](../secgloss/d-gly.md)et la fonction CryptoAPI définie. Les développeurs qui débutent dans ces rubriques sont invités à lire la spécification du protocole SSL 3,0 et à la documentation sur [Cryptography Essentials](cryptography-essentials.md) dans ce kit de développement logiciel (SDK). En outre, les développeurs RSA et Diffie-Hellman CSP doivent connaître les spécifications de protocole TLS ( [*Transport Layer Security*](../secgloss/t-gly.md) ) ainsi que les [*algorithmes RSA et Diffie-Hellman*](../secgloss/d-gly.md)appropriés.

Pour obtenir un exemple d’utilisation d’un moteur de protocole Microsoft, consultez [création de la clé principale](creating-the-master-key.md). Les appels aux fonctions de chiffrement dans cet exemple entraînent des appels aux fonctions CP qu’un CSP doit implémenter. Pour écrire un CSP compatible, un développeur doit comprendre la spécification SSL 3,0 et combiner cette connaissance avec une compréhension du code du moteur de protocole semblable à celui utilisé dans cet exemple.

Étant donné que l’utilisation du protocole de technologie des communications privées est supposée être minime, les développeurs de nouveaux fournisseurs de services de chiffrement n’ont pas besoin de prendre en charge ce protocole. Le moteur de protocole Schannel le prend en charge strictement à des fins de compatibilité descendante.

 

 
