---
description: Si la fonction de rappel par défaut va être appelée au cours de l’engagement de la file d’attente, le contexte de celle-ci doit être initialisé à l’aide des fonctions SetupInitDefaultQueueCallback ou SetupInitDefaultQueueCallbackEx.
ms.assetid: e87f8a66-33e5-4065-98ce-2e904c115b38
title: Validation de la file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ed721c60457a77a168218aa0294bf448889129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106517897"
---
# <a name="committing-the-queue"></a><span data-ttu-id="58943-103">Validation de la file d’attente</span><span class="sxs-lookup"><span data-stu-id="58943-103">Committing the Queue</span></span>

<span data-ttu-id="58943-104">Si la fonction de rappel par défaut va être appelée au cours de l’engagement de la file d’attente, le contexte de celle-ci doit être initialisé à l’aide des fonctions [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) .</span><span class="sxs-lookup"><span data-stu-id="58943-104">If the default callback function is going to be called during the queue commitment, the context for it must be initialized using the [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) functions.</span></span> <span data-ttu-id="58943-105">Si vous utilisez une fonction de rappel personnalisée qui n’appelle jamais la fonction de rappel par défaut, cette étape n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="58943-105">If you are using a custom callback function that never calls the default callback function, this step is not necessary.</span></span>

<span data-ttu-id="58943-106">Une fois la file d’attente générée et la fonction de rappel qui traite les notifications de file d’attente a été initialisée, vous pouvez appeler [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) pour valider les opérations qui ont été mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="58943-106">After the queue is built and the callback function that will process queue notifications has been initialized, you can call [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) to commit the operations that have been enqueued.</span></span>

<span data-ttu-id="58943-107">L’exemple suivant utilise [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) pour valider la file d’attente à l’aide de la routine de rappel par défaut.</span><span class="sxs-lookup"><span data-stu-id="58943-107">The following example uses [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) to commit the queue using the default callback routine.</span></span>

``` syntax
test = SetupCommitFileQueue (
     OwnerWindow,          //window that will own dialog boxes
                           //created by the callback routine
     MyQueue,              //the queue to commit
  
                           //use the default callback routine
     SetupDefaultQueueCallback,  
  
     Context               //context information that will be 
                           //  used by the callback routine
);
```

<span data-ttu-id="58943-108">Dans l’exemple précédent, MyQueue est la file d’attente à valider, OwnerWindow est la fenêtre qui possède toutes les boîtes de dialogue créées par la routine de rappel par défaut, SetupDefaultQueueCallback spécifie que la fonction de rappel par défaut sera utilisée, et *Context* est un pointeur vers la structure retournée par l’appel précédent à [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback).</span><span class="sxs-lookup"><span data-stu-id="58943-108">In the preceding example, MyQueue is the queue to commit, OwnerWindow is the window that will own any dialog boxes created by the default callback routine, SetupDefaultQueueCallback specifies that the default callback function will be used, and *Context* is a pointer to the structure returned by the previous call to [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback).</span></span>

 

 



