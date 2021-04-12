---
description: Un code d’authentification de message (MAC) est utilisé pour détecter la falsification et la falsification de messages.
ms.assetid: 44f50407-8f55-49c4-9e42-2f1666c9da7c
title: Codes d’authentification de message dans Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93939c0c4b4550ad0c24f8e6ef0e0b8bf9f1b07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204162"
---
# <a name="message-authentication-codes-in-schannel"></a>Codes d’authentification de message dans Schannel

Un [*code d’Authentification de message*](../secgloss/m-gly.md) (Mac) est utilisé pour détecter la falsification et la falsification de messages. L’expéditeur d’un message crée un MAC en chiffrant un [*hachage*](../secgloss/h-gly.md) unidirectionnel du corps du message à l’aide d’une [*clé de session*](../secgloss/s-gly.md) partagée par l’expéditeur et le destinataire. Le MAC est ajouté au message envoyé au destinataire. Le destinataire du message génère à nouveau le MAC, à l’aide de la clé de session partagée et du corps du message, et compare le MAC généré au MAC reçu de l’expéditeur. Si les deux sont identiques, l’expéditeur doit avoir la clé de session partagée et le message n’a pas été modifié en transit.

Dans les protocoles Schannel, l’algorithme utilisé pour générer le MAC est déterminé par la [suite de chiffrement](cipher-suites-in-schannel.md) utilisée par l’expéditeur et le destinataire.

 

 
