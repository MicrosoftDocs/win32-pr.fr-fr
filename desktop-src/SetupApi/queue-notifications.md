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
# <a name="queue-notifications"></a><span data-ttu-id="7a036-104">Notifications de file d’attente</span><span class="sxs-lookup"><span data-stu-id="7a036-104">Queue Notifications</span></span>

<span data-ttu-id="7a036-105">Une fois qu’une file d’attente a été validée par l’appel de [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), elle commence à traiter les opérations en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="7a036-105">After a queue is committed by calling [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), it will begin to process the queued operations.</span></span> <span data-ttu-id="7a036-106">À chaque étape, la file d’attente envoie une notification à la routine de rappel spécifiée dans l’appel à **SetupCommitFileQueue**.</span><span class="sxs-lookup"><span data-stu-id="7a036-106">At each step, the queue sends a notification to the callback routine specified in the call to **SetupCommitFileQueue**.</span></span>

<span data-ttu-id="7a036-107">Voici la syntaxe utilisée par [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) pour envoyer une notification à la routine de rappel.</span><span class="sxs-lookup"><span data-stu-id="7a036-107">Following is the syntax that [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) uses to send a notification to the callback routine.</span></span>

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //queue notification code
    Param1,          //additional notification information
    Param2               //additional notification information
);
```

<span data-ttu-id="7a036-108">Les valeurs de *param1* et de *param2* contiennent des informations supplémentaires relatives à la notification envoyée à la routine de rappel.</span><span class="sxs-lookup"><span data-stu-id="7a036-108">The values of *Param1* and *Param2* contain additional information relevant to the notification being sent to the callback routine.</span></span> <span data-ttu-id="7a036-109">Chaque notification, ses valeurs *param1* et *param2* et comment la routine de rappel de file d’attente par défaut gère cette notification, est décrite en détail dans [notifications de file d’attente de fichiers](file-queue-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="7a036-109">Each notification, its *Param1* and *Param2* values, and how the default queue callback routine handles that notification, is described in detail in [File Queue Notifications](file-queue-notifications.md).</span></span>

 

 



