---
description: Un groupe de fonctions de haut niveau a été fourni pour simplifier et raccourcir la quantité de code nécessaire pour accomplir les tâches de manipulation de message habituelles.
ms.assetid: 7c1a4d6e-9b9d-43c8-b094-3c98b9a68490
title: Messages simplifiés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbacaac4dd8ef32b7bab1ff4e57ad04aa1263c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113543"
---
# <a name="simplified-messages"></a>Messages simplifiés

Un groupe de fonctions de haut niveau a été fourni pour simplifier et raccourcir la quantité de code nécessaire pour accomplir les tâches de manipulation de message habituelles. Ces fonctions sont appelées « fonctions de message simplifiées ». Les noms de toutes les fonctions de message simplifiées contiennent le mot « message ».

Les [*fonctions de message simplifiées*](../secgloss/s-gly.md) se trouvent à un niveau supérieur à celui des fonctions de chiffrement de base ou des fonctions de message de bas niveau. Elles encapsulent plusieurs fonctions de chiffrement de base, de message de bas niveau et de certificat dans une fonction unique qui effectue une tâche spécifique d’une manière spécifique, telle que le chiffrement d’un \# message PKCS 7 ou la signature d’un message. Les fonctions de message simplifiées offrent un moyen rapide de commencer à utiliser CryptoAPI en réduisant le nombre d’appels de fonction nécessaires pour accomplir une tâche.

Le tableau suivant répertorie les sections qui contiennent des descriptions de procédure détaillées ou des exemples de programme C d’utilisation des fonctions de message simplifiées.



| Section                                                                                                                                         | Contents                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Fonctions de message simplifiées](cryptography-functions.md)                                                         | Répertorie les fonctions de message simplifiées.                                                     |
| [Création d’un message signé](creating-a-signed-message.md)                                                                                      | Décrit en détail le processus de création d’un message signé.                                           |
| [Procédure de signature des données](procedure-for-signing-data.md)                                                                                    | Fournit une procédure qui permet d’utiliser les fonctions de message simplifiées pour créer un message signé. |
| [Vérification d’un message signé](verifying-a-signed-message.md)                                                                                    | Décrit en détail un processus de vérification de la signature d’un message signé.                          |
| [Chiffrement d’un message](../secauthn/encrypting-a-message.md)                                                                                           | Détaille les tâches nécessaires pour chiffrer et déchiffrer un message.                                  |
| [Déchiffrement d’un message](../secauthn/decrypting-a-message.md)                                                                                           | Détaille les tâches nécessaires au déchiffrement d’un message.                                              |
| [Exemple de programme C : utilisation de CryptEncryptMessage et CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) | Fournit une procédure et un exemple de code pour le chiffrement et le déchiffrement d’un message.               |



 

 

 
