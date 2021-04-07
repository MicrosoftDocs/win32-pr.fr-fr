---
description: Une fois toutes les opérations de fichier en attente, la file d’attente doit être validée. Cela entraîne le traitement des opérations de fichier mises en file d’attente.
ms.assetid: 536f47f5-785e-4a83-a500-c769442e3e68
title: Validation d’une file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d995f6811dbd19bba9e13f29bc119cdf2f471f74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759790"
---
# <a name="committing-a-queue"></a><span data-ttu-id="64197-104">Validation d’une file d’attente</span><span class="sxs-lookup"><span data-stu-id="64197-104">Committing a Queue</span></span>

<span data-ttu-id="64197-105">Une fois toutes les opérations de fichier en attente, la file d’attente doit être validée.</span><span class="sxs-lookup"><span data-stu-id="64197-105">After all the desired file operations have been queued, the queue must be committed.</span></span> <span data-ttu-id="64197-106">Cela entraîne le traitement des opérations de fichier mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="64197-106">This causes the enqueued file operations to be processed.</span></span>

<span data-ttu-id="64197-107">Une file d’attente de fichiers ne peut pas être réutilisée une fois qu’elle a été validée.</span><span class="sxs-lookup"><span data-stu-id="64197-107">A file queue cannot be reused after it has been committed.</span></span> <span data-ttu-id="64197-108">La meilleure pratique consiste à collecter toutes les opérations de fichier requises pour la file d’attente de fichiers et à valider la file d’attente une seule fois.</span><span class="sxs-lookup"><span data-stu-id="64197-108">The best practice is to collect all the required file operations for the file queue and commit the queue only once.</span></span> <span data-ttu-id="64197-109">Si un traitement supplémentaire de la file d’attente est requis après sa validation, le descripteur de la file d’attente doit être fermé et une nouvelle file d’attente de fichiers doit être créée.</span><span class="sxs-lookup"><span data-stu-id="64197-109">If additional processing of the queue is required after it has been committed, the handle to the queue should be closed and a new file queue created.</span></span> <span data-ttu-id="64197-110">Pour valider la file d’attente de fichiers, appelez la fonction [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) , en spécifiant une routine de rappel.</span><span class="sxs-lookup"><span data-stu-id="64197-110">To commit the file queue, call the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function, specifying a callback routine.</span></span> <span data-ttu-id="64197-111">La routine de rappel recevra des notifications de **SetupCommitFileQueue** lors du traitement des opérations de fichier.</span><span class="sxs-lookup"><span data-stu-id="64197-111">The callback routine will receive notifications from **SetupCommitFileQueue** as the file operations are processed.</span></span> <span data-ttu-id="64197-112">Si vous souhaitez utiliser la routine de rappel de file d’attente par défaut, vous devez d’abord initialiser le contexte nécessaire en appelant [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span><span class="sxs-lookup"><span data-stu-id="64197-112">If you want to use the default queue callback routine, you must first initialize the necessary context by calling either [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span></span> <span data-ttu-id="64197-113">Pour plus d’informations sur la routine de rappel de file d’attente par défaut, consultez [routine de rappel de file d’attente par défaut](default-queue-callback-routine.md).</span><span class="sxs-lookup"><span data-stu-id="64197-113">For more information about the default queue callback routine, see [Default Queue Callback Routine](default-queue-callback-routine.md).</span></span>

> [!Note]  
> <span data-ttu-id="64197-114">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) doit être appelé avant la fermeture de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="64197-114">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) should be called before the queue is closed.</span></span> <span data-ttu-id="64197-115">Toutes les opérations qui ne sont pas validées quand [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) est appelé ne sont pas exécutées.</span><span class="sxs-lookup"><span data-stu-id="64197-115">Any operations that are uncommitted when [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) is called will not be performed.</span></span>

 

 

 



