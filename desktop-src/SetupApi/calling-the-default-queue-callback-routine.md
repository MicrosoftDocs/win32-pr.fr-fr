---
description: Si la routine de rappel de file d’attente par défaut est initialisée et spécifiée lors de l’appel de SetupCommitFileQueue, la file d’attente appelle la routine de rappel de file d’attente par défaut en interne et vous n’avez rien d’autre à faire.
ms.assetid: a976c275-f128-490d-a544-efbfc6fd87f4
title: Appel de la routine de rappel de file d’attente par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24449fc1fcd92d8041de6f104092f45925a495b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523675"
---
# <a name="calling-the-default-queue-callback-routine"></a><span data-ttu-id="7ed88-103">Appel de la routine de rappel de file d’attente par défaut</span><span class="sxs-lookup"><span data-stu-id="7ed88-103">Calling the Default Queue Callback Routine</span></span>

<span data-ttu-id="7ed88-104">Si la routine de rappel de file d’attente par défaut est initialisée et spécifiée lors de l’appel de [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) , la file d’attente appelle la routine de rappel de file d’attente par défaut en interne et vous n’avez rien d’autre à faire.</span><span class="sxs-lookup"><span data-stu-id="7ed88-104">If the default queue callback routine is initialized and specified when [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) is called, the queue calls the default queue callback routine internally and you need do nothing more.</span></span>

<span data-ttu-id="7ed88-105">Si vous créez une routine de rappel de filtre qui s’appuie sur la routine de rappel de file d’attente par défaut pour gérer un sous-ensemble des notifications de la file d’attente, votre routine de rappel de filtre doit appeler [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explicitement.</span><span class="sxs-lookup"><span data-stu-id="7ed88-105">If you create a filter callback routine that relies on the default queue callback routine to handle a subset of the queue notifications, your filter callback routine must call [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explicitly.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7ed88-106">Lorsque vous appelez [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) de manière explicite, vous devez passer le pointeur void retourné par [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span><span class="sxs-lookup"><span data-stu-id="7ed88-106">When you call [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explicitly, you must pass in the void pointer returned by either [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span></span>

 

> [!Note]  
> <span data-ttu-id="7ed88-107">Une façon de procéder consiste à créer une structure de contexte pour votre routine de rappel personnalisée qui comprend comme un de ses membres le pointeur void retourné par [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span><span class="sxs-lookup"><span data-stu-id="7ed88-107">One way to do this is to create a context structure for your custom callback routine that includes as one of its members the void pointer returned by [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span></span>

 

 

 



