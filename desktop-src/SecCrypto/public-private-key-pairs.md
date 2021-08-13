---
description: Les clés asymétriques, également appelées paires de clés publiques/privées, sont utilisées pour le chiffrement asymétrique. Le chiffrement asymétrique est principalement utilisé pour chiffrer et déchiffrer les clés de session et les signatures numériques. Le chiffrement asymétrique utilise des algorithmes de chiffrement à clé publique.
ms.assetid: f75e5e6c-0a84-47ac-97db-5063327f7931
title: Clés asymétriques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374ba5ae17610154e306f7bdafd895116e83371ea446babfa19b5c92c29a2247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901471"
---
# <a name="asymmetric-keys"></a>Clés asymétriques

Les [*clés asymétriques*](../secgloss/a-gly.md), également appelées [*paires de clés publiques/privées*](../secgloss/p-gly.md), sont utilisées pour le chiffrement asymétrique. Le chiffrement asymétrique est principalement utilisé pour chiffrer et déchiffrer les [*clés de session*](../secgloss/s-gly.md) et les [*signatures numériques*](../secgloss/d-gly.md). Le chiffrement asymétrique utilise des algorithmes de [*chiffrement à clé publique*](../secgloss/p-gly.md) .

Les algorithmes de clé publique utilisent deux clés différentes : une [*clé publique*](../secgloss/p-gly.md) et une [*clé privée*](../secgloss/p-gly.md). Le membre de clé privée de la paire doit rester privé et sécurisé. Toutefois, la clé publique peut être distribuée à toute personne qui la demande. La clé publique d’une paire de clés est souvent distribuée au moyen d’un [*certificat numérique*](../secgloss/c-gly.md). Lorsqu’une clé d’une paire de clés est utilisée pour chiffrer un message, l’autre clé de cette paire est nécessaire pour déchiffrer le message. Par conséquent, si la clé publique de l’utilisateur A est utilisée pour chiffrer les données, seul l’utilisateur A (ou une personne qui a accès à la clé privée de l’utilisateur a) peut déchiffrer les données. Si la clé privée de l’utilisateur a est utilisée pour chiffrer un élément de données, seule la clé publique de l’utilisateur A déchiffre les données, indiquant ainsi que l’utilisateur A (ou une personne ayant accès à la clé privée de l’utilisateur A) a effectué le chiffrement.

Si la clé privée est utilisée pour signer un message, la clé publique de cette paire doit être utilisée pour valider la signature. Par exemple, si Alice souhaite envoyer un message signé numériquement, elle signe le message avec sa clé privée, et l’autre personne peut vérifier sa signature à l’aide de sa clé publique. Sachant que seul Alice a accès à sa clé privée, le fait que la signature puisse être vérifiée avec la clé publique d’Alice indique qu’Alice a créé la signature.

Malheureusement, les algorithmes de clé publique sont très lents, environ 1 000 fois plus lents que les algorithmes symétriques. Il n’est pas pratique de les utiliser pour chiffrer de grandes quantités de données. Dans la pratique, les algorithmes de clé publique sont utilisés pour chiffrer les [*clés de session*](../secgloss/s-gly.md). Les [*algorithmes symétriques*](../secgloss/s-gly.md) sont utilisés pour le chiffrement/déchiffrement de la plupart des données.

De même, étant donné que la signature d’un message, en effet, chiffre le message, il n’est pas pratique d’utiliser des algorithmes de signature de clé publique pour signer des messages volumineux. Au lieu de cela, un [*hachage*](../secgloss/h-gly.md) de longueur fixe est effectué du message et la valeur de hachage est signée. Pour plus d’informations, consultez [hachages et signatures numériques](hashes-and-digital-signatures.md).

Chaque utilisateur a généralement deux [*paires de clés publique/privée*](../secgloss/p-gly.md). Une paire de clés est utilisée pour chiffrer les clés de session et l’autre pour créer des [*signatures numériques*](../secgloss/d-gly.md). Il s’agit respectivement de la paire de clés d' [*échange*](../secgloss/k-gly.md) de clés et de la paire de [*clés de signature*](../secgloss/s-gly.md).

Notez que bien que les conteneurs de clés créés par la plupart des [*fournisseurs de services de chiffrement*](../secgloss/c-gly.md) (CSP) contiennent deux paires de clés, ce n’est pas obligatoire. Certains fournisseurs de services de chiffrement ne stockent aucune [*paire de clés*](../secgloss/k-gly.md) , tandis que d’autres fournisseurs stockent plus de deux paires.

Toutes les clés dans CryptoAPI sont stockées dans des fournisseurs de services de chiffrement. Les fournisseurs de services de chiffrement sont également chargés de créer les clés, de les détruire et de les utiliser pour effectuer diverses opérations de chiffrement. l’exportation de clés à partir du CSP afin qu’elles puissent être envoyées à d’autres utilisateurs est décrite dans [Stockage de clé de chiffrement et Exchange](cryptographic-key-storage-and-exchange.md).

 

 
