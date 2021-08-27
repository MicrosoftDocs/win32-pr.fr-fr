---
description: Parfois, un message signé requiert une contre-signature.
ms.assetid: de83a9ad-4e88-4477-8c9e-6dd7d5ec9e8f
title: Contre-signatures de messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d95f9d082a2814501bdb948d1bfebdc5c2699012446c5189c5c3fc18612c1ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080639"
---
# <a name="message-countersignatures"></a>Contre-signatures de messages

Parfois, un message signé requiert une contre- [*signature*](../secgloss/c-gly.md). Par exemple, l’utilisateur A peut envoyer un message signé aux données à l’utilisateur B, en attendant que B confirme un accord avec les termes contenus dans le document. L’utilisateur B décode le message, lit les termes et, si dans l’accord, en contresigné le message. Le message contresigné est ensuite renvoyé à l’utilisateur A. l’utilisateur A sait maintenant et peut prouver que l’utilisateur B a accepté les conditions.

Le tableau suivant répertorie les sections qui contiennent des descriptions de procédure ou des exemples de programme C de signature de message.



| Section                                                                                                                                 | Contents                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Fonctions de message](cryptography-functions.md)                                                                       | Répertorie les fonctions de signature de compteur.                             |
| [Contre-signature d’un message](countersigning-a-message.md)                                                                                | Détaille le processus de signature de compteur d’un message.                  |
| [Vérification d’une contre-signature](verifying-a-countersignature.md)                                                                        | Détaille la procédure de vérification d’une signature de compteur.           |
| [Vérification d’un message signé](verifying-a-signed-message.md)                                                                            | Décrit en détail un processus de vérification de la signature d’un message signé. |
| [Exemple de programme C : encodage et décodage d’un message contresigné](example-c-program-encoding-and-decoding-a-countersigned-message.md) | Exemple de programme C qui encode et décode un message contresigné. |



 

 

 
