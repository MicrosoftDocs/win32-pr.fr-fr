---
description: Microsoft Digest effectue une authentification initiale lorsque le serveur reçoit la première réponse à la demande d’un client.
ms.assetid: c65bb134-d480-4a71-872c-30e2884237a6
title: Microsoft Digest Authentication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d5eb9c2d114bae70c28d07ed9fef64f9d0514
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123426"
---
# <a name="microsoft-digest-authentication"></a>Microsoft Digest Authentication

Microsoft Digest effectue une authentification initiale lorsque le serveur reçoit la première réponse à la demande d’un client. Le serveur vérifie que le client n’a pas été authentifié, puis effectue l’authentification initiale en accédant aux services d’un contrôleur de domaine. Pour obtenir une description détaillée de cette procédure, consultez [authentification initiale à l’aide de Microsoft Digest](initial-authentication-using-microsoft-digest.md).

Lorsque l’authentification initiale est réussie, le serveur reçoit une [*clé de session*](../secgloss/s-gly.md)Digest. Le serveur met en cache cette clé et l’utilise pour authentifier les demandes ultérieures de ressources du client. Cette authentification est locale, c’est-à-dire qu’elle n’a pas besoin d’accéder à un contrôleur de domaine. Pour obtenir une description détaillée de cette procédure, consultez [authentification des demandes ultérieures à l’aide de Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).

Si vous utilisez le protocole HTTP, aucune connexion n’est maintenue entre le client et le serveur. Pour réduire le trafic des contrôleurs de domaine et améliorer les performances, Microsoft Digest met en cache les informations reçues après une authentification réussie. Pour plus d’informations sur ce processus, consultez [maintenance du contexte de sécurité entre les connexions](maintaining-the-security-context-between-connections.md).

 

 
