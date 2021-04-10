---
title: Inscription auprès du gestionnaire de tables de routage
description: Pour qu’un client puisse accéder à la table de routage, il doit d’abord s’inscrire auprès du gestionnaire de tables de routage à l’aide de la fonction RtmRegisterEntity.
ms.assetid: 9bdbe138-d31b-42bb-9c51-5f1c5e8a4ca7
keywords:
- Gestionnaire de table de routage, version 2 RRAS, inscription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ce5a1b350ec5420b3fc32a4e5a68a213a61151
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196700"
---
# <a name="registering-with-the-routing-table-manager"></a>Inscription auprès du gestionnaire de tables de routage

Pour qu’un client puisse accéder à la table de routage, il doit d’abord s’inscrire auprès du gestionnaire de tables de routage à l’aide de la fonction [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) .

Lorsqu’un client s’inscrit, il passe au gestionnaire de table de routage une structure d' [**\_ \_ informations d’entité RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) . Cette structure contient les informations qui identifient de façon unique un client, la famille d’adresses et l’instance du gestionnaire de tables de routage avec lequel le client est inscrit. Un client peut également établir le rappel de [**\_ \_ rappel d’événement RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) . Le gestionnaire de tables de routage utilise ce rappel pour notifier au client des événements tels que les notifications de modifications et les inscriptions des clients.

Le gestionnaire de table de routage termine son traitement d’inscription et retourne un descripteur au client. Le client doit utiliser ce handle pour tous les appels suivants aux fonctions RTMv2.

La fonction [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) utilisée dans RTMv2 est analogue à la fonction [**RtmRegisterClient**](rtmregisterclient.md) utilisée dans RTMv1. La fonction **RtmRegisterClient** est obsolète, sauf pour les clients utilisant IPX.

Une fois qu’un client a terminé l’interaction avec le gestionnaire de tables de routage, il doit appeler [**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity). Le gestionnaire de tables de routage détruit le descripteur associé au client. Pour éviter les fuites de mémoire, le client doit s’assurer qu’il libère tous les descripteurs et supprime tous les itinéraires et tronçons suivants qu’il détient avant d’appeler **RtmDeregisterEntity**.

Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [s’inscrire auprès du gestionnaire de tables de routage](register-with-the-routing-table-manager.md) et [utiliser le rappel de notification d’événement](use-the-event-notification-callback.md).

 

 




