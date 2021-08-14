---
description: Microsoft Digest effectue une authentification initiale lorsque le serveur reçoit la première réponse à la demande d’un client.
ms.assetid: c65bb134-d480-4a71-872c-30e2884237a6
title: Microsoft Digest Authentication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 135e5374515acb0604ee14a6770b9523e9bf31fd0e2d6c946fec26d2ad789c2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921828"
---
# <a name="microsoft-digest-authentication"></a>Microsoft Digest Authentication

Microsoft Digest effectue une authentification initiale lorsque le serveur reçoit la première réponse à la demande d’un client. Le serveur vérifie que le client n’a pas été authentifié, puis effectue l’authentification initiale en accédant aux services d’un contrôleur de domaine. Pour obtenir une description détaillée de cette procédure, consultez [authentification initiale à l’aide de Microsoft Digest](initial-authentication-using-microsoft-digest.md).

Lorsque l’authentification initiale est réussie, le serveur reçoit une [*clé de session*](../secgloss/s-gly.md)Digest. Le serveur met en cache cette clé et l’utilise pour authentifier les demandes ultérieures de ressources du client. Cette authentification est locale, c’est-à-dire qu’elle n’a pas besoin d’accéder à un contrôleur de domaine. Pour obtenir une description détaillée de cette procédure, consultez [authentification des demandes ultérieures à l’aide de Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).

Si vous utilisez le protocole HTTP, aucune connexion n’est maintenue entre le client et le serveur. Pour réduire le trafic des contrôleurs de domaine et améliorer les performances, Microsoft Digest met en cache les informations reçues après une authentification réussie. Pour plus d’informations sur ce processus, consultez [maintenance du contexte de sécurité entre les connexions](maintaining-the-security-context-between-connections.md).

 

 
