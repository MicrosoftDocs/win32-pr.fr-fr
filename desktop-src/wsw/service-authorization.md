---
title: Autorisation du service
description: Une application peut implémenter une autorisation personnalisée pour les messages entrants sur un hôte de service.
ms.assetid: 75bcf051-3983-48fc-8121-0984ac9cdcb9
keywords:
- Services Web d’autorisation de service pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b84b9947d088d5f594ac11f0ee83cc03925f8a3bbc9aeceae0bc7d5cb120477
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109839"
---
# <a name="service-authorization"></a>Autorisation du service

Une application peut implémenter une autorisation personnalisée pour les messages entrants sur un hôte de service.


Un hôte de service reçoit un rappel de sécurité de [**service Web de rappel \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) de sécurité dans le cadre du [**\_ point de \_ terminaison de service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) qui est passé à la fonction [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) . Ce rappel est appelé lors de la réception du [ \_ message WS](ws-message.md) .

L’application peut s’appuyer sur ce rappel pour implémenter l’autorisation personnalisée pour les messages entrants sur l’hôte de service. Si l’autorisation échoue, la fonction de rappel de sécurité retourne un échec HR et l’hôte de service abandonne le canal.

Pour obtenir un exemple d’implémentation, consultez l’exemple nom d’utilisateur sur SSL [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md).

 

 




