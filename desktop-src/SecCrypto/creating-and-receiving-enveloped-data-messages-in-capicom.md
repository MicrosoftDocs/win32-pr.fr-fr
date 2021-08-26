---
description: Le message enveloppé est constitué du message chiffré, des certificats des destinataires prévus et de l’ensemble des clés chiffrées, une pour chaque destinataire. Le message généré est au \# format PKCS 7/CMS.
ms.assetid: 2acd0b58-1028-478d-bfa1-b02fa457d7e3
title: Création et réception de messages de données enveloppés dans CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4024516333b7dd416f788f181f2ac36e5e0f4e015953cdab26d08b48da16c49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876538"
---
# <a name="creating-and-receiving-enveloped-data-messages-in-capicom"></a>Création et réception de messages de données enveloppés dans CAPICOM

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité. Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]

Un message enveloppé est un message chiffré pour un ensemble de destinataires. Dans le processus d’encapsulement, une clé de chiffrement de session est générée et le message est chiffré avec cette clé. La clé de chiffrement est ensuite chiffrée séparément pour chaque destinataire à l’aide des clés publiques de chaque certificat de destinataire prévu. Le message enveloppé est constitué du message chiffré, des certificats des destinataires prévus et de l’ensemble des clés chiffrées, une pour chaque destinataire. Le message généré est au \# format PKCS 7/CMS.

Les sections suivantes présentent des procédures et des exemples de tâches de messages enveloppés :

-   [Envoi d’un message de données enveloppées](sending-an-enveloped-data-message.md)
-   [Réception d’un message de données enveloppées](receiving-an-enveloped-data-message.md)

 

 



