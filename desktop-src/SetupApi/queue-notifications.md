---
description: Une fois qu’une file d’attente a été validée par l’appel de SetupCommitFileQueue, elle commence à traiter les opérations en file d’attente. À chaque étape, la file d’attente envoie une notification à la routine de rappel spécifiée dans l’appel à SetupCommitFileQueue.
ms.assetid: 866e1066-b6e0-43d3-8af4-bd37fbc024e2
title: Notifications de file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 842a3ebc82640789fdb6e730e881d6790a0d642b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538922"
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

 

 



