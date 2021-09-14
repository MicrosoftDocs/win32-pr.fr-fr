---
description: Les fonctions de message de bas niveau encodent les données pour transmettre et décoder les données qui ont été reçues. Les fonctions de message de bas niveau déchiffrent et vérifient également les signatures des messages reçus.
ms.assetid: 42c19920-c7f7-4a4d-9de3-3de9a34fbe0c
title: Fonctions de message de bas niveau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22654f19dfe5178dfb98006c17c2d0536f78cd46
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237533"
---
# <a name="low-level-message-functions"></a>Fonctions de message de bas niveau

Les [*fonctions de message de bas niveau*](../secgloss/l-gly.md) encodent les données pour transmettre et décoder les données qui ont été reçues. Les fonctions de message de bas niveau déchiffrent et vérifient également les signatures des messages reçus.

Lorsqu’un message est ouvert à l’aide d’une fonction d’ouverture de message de bas niveau, il reste ouvert et disponible (conserve son [*État*](../secgloss/s-gly.md)) jusqu’à ce qu’il soit fermé. Cela permet de construire un message fragmentaire à l’aide de plusieurs appels à la fonction [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) .

L’utilisation de fonctions de message de bas niveau requiert davantage d’appels de fonction que l’utilisation de fonctions de message simplifiées (voir [messages simplifiés](simplified-messages.md)). Si les fonctions de message simplifiées sont utilisées, une plus grande partie du travail est effectuée à l’intérieur des fonctions de l’API.

L’utilisation de fonctions de message de bas niveau implique l’exécution d’appels à d’autres fonctions de certificat ou de chiffrement. Par exemple, les données des appels aux fonctions de certificat peuvent être nécessaires pour initialiser les structures utilisées par ces fonctions de message de bas niveau. Les fonctions de message simplifiées initialisent un grand nombre de ces structures en interne.

Le tableau suivant répertorie les sections avec des descriptions de procédure et des exemples de code C qui utilisent les fonctions de message de bas niveau.



| Section                                                                               | Contents                                           |
|---------------------------------------------------------------------------------------|----------------------------------------------------|
| [Fonctions de message de bas niveau](cryptography-functions.md) | Répertorie les fonctions de message de bas niveau.             |
| [Signature des données](signing-data.md)                                                      | Détaille les tâches nécessaires à la signature des données.             |
| [Encodage de données enveloppées](encoding-enveloped-data.md)                                | Détaille les tâches nécessaires pour encoder les données enveloppées. |
| [Décodage des données enveloppées](decoding-enveloped-data.md)                                | Détaille les tâches nécessaires pour décoder les données enveloppées. |



 

 

 
