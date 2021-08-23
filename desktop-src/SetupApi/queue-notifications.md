---
description: Une fois qu’une file d’attente a été validée par l’appel de SetupCommitFileQueue, elle commence à traiter les opérations en file d’attente. À chaque étape, la file d’attente envoie une notification à la routine de rappel spécifiée dans l’appel à SetupCommitFileQueue.
ms.assetid: 866e1066-b6e0-43d3-8af4-bd37fbc024e2
title: Notifications de file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06858eeb5c6e9abe200792f83edcc83503270ed2706450d35ef36d5dddc80d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665489"
---
# <a name="queue-notifications"></a>Notifications de file d’attente

Une fois qu’une file d’attente a été validée par l’appel de [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), elle commence à traiter les opérations en file d’attente. À chaque étape, la file d’attente envoie une notification à la routine de rappel spécifiée dans l’appel à **SetupCommitFileQueue**.

Voici la syntaxe utilisée par [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) pour envoyer une notification à la routine de rappel.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //queue notification code
    Param1,          //additional notification information
    Param2               //additional notification information
);
```

Les valeurs de *param1* et de *param2* contiennent des informations supplémentaires relatives à la notification envoyée à la routine de rappel. Chaque notification, ses valeurs *param1* et *param2* et comment la routine de rappel de file d’attente par défaut gère cette notification, est décrite en détail dans [notifications de file d’attente de fichiers](file-queue-notifications.md).

 

 



