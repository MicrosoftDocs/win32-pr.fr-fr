---
description: Une clé principale est un matériau de données clé à partir duquel d’autres clés sont dérivées.
ms.assetid: c8445f74-659a-470b-9007-07ea98d36dcd
title: Création de la clé principale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35a6aef52525bdce622355ede4ae9723f7cd8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525738"
---
# <a name="creating-the-master-key"></a>Création de la clé principale

Une [*clé principale*](../secgloss/m-gly.md) est un matériau de données clé à partir duquel d’autres clés sont dérivées. En fonction du protocole et de la suite de chiffrement utilisés, la longueur de la clé principale peut être comprise entre 5 et 48 octets. Pour le [](../secgloss/r-gly.md) / fournisseur CSP RSA [*Schannel*](../secgloss/s-gly.md) , la clé principale est créée par le côté client et transférée vers le serveur dans une enveloppe RSA. Pour un CSP/Schannel [*Diffie-Hellman*](../secgloss/d-gly.md), la clé principale est créée en effectuant une Diffie-Hellman échange de clés.

Le code pour la création et l’échange de clés principales est illustré dans :

-   [Code client Diffie-Hellman pour la création de la clé principale](diffie-hellman-client-code-for-creating-the-master-key.md)
-   [Code serveur Diffie-Hellman pour la création de la clé principale](diffie-hellman-server-code-for-creating-the-master-key.md)
-   [Code client RSA pour la création de la clé principale](rsa-client-code-for-creating-the-master-key.md)
-   [Code du serveur RSA pour la création de la clé principale](rsa-server-code-for-creating-the-master-key.md)
-   [Spécification des algorithmes](specifying-the-algorithms.md)

 

 
