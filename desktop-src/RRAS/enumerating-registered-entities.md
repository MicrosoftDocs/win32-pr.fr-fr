---
title: Énumération des entités inscrites
description: Une fois qu’un client est inscrit, le client peut obtenir une liste de tous les autres clients qui se sont inscrits auprès du gestionnaire de tables de routage. Certains clients doivent effectuer certaines opérations si la présence d’un type particulier de client est détectée.
ms.assetid: d94de573-7c1e-4179-a41f-5836d2c5d44a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1d67a810806c1bc29f8f18c4cdea9f3a36e5b5a95922e8f66a943a99923ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674159"
---
# <a name="enumerating-registered-entities"></a>Énumération des entités inscrites

Une fois qu’un client est inscrit, le client peut obtenir une liste de tous les autres clients qui se sont inscrits auprès du gestionnaire de tables de routage. Certains clients doivent effectuer certaines opérations si la présence d’un type particulier de client est détectée.

Le client peut appeler la fonction [**RtmGetRegisteredEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) . Une mémoire tampon des structures d' [**\_ \_ informations d’entité RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) est retournée. Une fois que le client a traité ces informations, le client doit appeler [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) pour libérer les descripteurs dans les structures d' **\_ \_ informations d’entité RTM** .

Si le client du gestionnaire de table de routage a fourni une fonction de rappel dans l’appel à [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity), le client est averti lorsque d’autres clients s’inscrivent ou annulent l’inscription.

Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [énumérer les entités inscrites](enumerate-the-registered-entities.md) et [utiliser le rappel de notification d’événement](use-the-event-notification-callback.md).

 

 




