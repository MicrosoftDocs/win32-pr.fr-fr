---
description: Un message enveloppé est un message chiffré pour un destinataire ou un ensemble de destinataires.
ms.assetid: caf86ec8-48b6-4017-95ad-7a21fcaed4cf
title: Création et réception des messages de données enveloppés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a63abf31d582ae9ae184dc15d85d827a3741d317e3bad75c8b07cce25e457bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768904"
---
# <a name="creating-and-receiving-enveloped-data-messages"></a>Création et réception des messages de données enveloppés

Un message enveloppé est un message chiffré pour un ensemble de destinataires. Dans le processus d’encapsulement, une clé de chiffrement de session est générée et le message est chiffré avec cette clé. La clé de chiffrement est ensuite chiffrée séparément pour chaque destinataire à l’aide des clés publiques de chaque certificat de destinataire prévu. Le message enveloppé est constitué du message chiffré, des certificats des destinataires prévus et de l’ensemble des clés chiffrées, une pour chaque destinataire. Le message généré est au format [*PKCS \# 7*](../secgloss/p-gly.md)/CMS.

Les sections suivantes présentent des procédures et des exemples de tâches de messages enveloppés :

-   [Encodage de données enveloppées](encoding-enveloped-data.md)
-   [Décodage des données enveloppées](decoding-enveloped-data.md)
-   [Autre code pour l’encodage d’un message enveloppé](alternate-code-for-encoding-an-enveloped-message.md)
-   [Exemple de programme C : encodage d’un message signé et enveloppé](example-c-program-encoding-an-enveloped-signed-message.md)

 

 
