---
description: La fonction CreateTimerQueue crée une file d’attente pour les minuteurs.
ms.assetid: ee85a6c3-3a1d-4f94-9112-cb8247b2a189
title: Files d’attente du minuteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ad2f94612c234b3ec0d1d75fa723c4e86e6fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518713"
---
# <a name="timer-queues"></a><span data-ttu-id="43612-103">Files d’attente du minuteur</span><span class="sxs-lookup"><span data-stu-id="43612-103">Timer Queues</span></span>

<span data-ttu-id="43612-104">La fonction [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) crée une file d’attente pour les minuteurs.</span><span class="sxs-lookup"><span data-stu-id="43612-104">The [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) function creates a queue for timers.</span></span> <span data-ttu-id="43612-105">Les minuteries de cette file d’attente, appelées *minuteries de file d’attente du minuteur*, sont des objets légers qui vous permettent de spécifier une fonction de rappel à appeler lorsque l’heure d’échéance spécifiée arrive.</span><span class="sxs-lookup"><span data-stu-id="43612-105">Timers in this queue, known as *timer-queue timers*, are lightweight objects that enable you to specify a callback function to be called when the specified due time arrives.</span></span> <span data-ttu-id="43612-106">L’opération d’attente est effectuée par un thread dans le [pool de threads](../procthread/thread-pooling.md).</span><span class="sxs-lookup"><span data-stu-id="43612-106">The wait operation is performed by a thread in the [thread pool](../procthread/thread-pooling.md).</span></span>

<span data-ttu-id="43612-107">Pour ajouter un minuteur à la file d’attente, appelez la fonction [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) .</span><span class="sxs-lookup"><span data-stu-id="43612-107">To add a timer to the queue, call the [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function.</span></span> <span data-ttu-id="43612-108">Pour mettre à jour un minuteur de file d’attente de minuterie, appelez la fonction [**ChangeTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) .</span><span class="sxs-lookup"><span data-stu-id="43612-108">To update a timer-queue timer, call the [**ChangeTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) function.</span></span> <span data-ttu-id="43612-109">Vous pouvez spécifier une fonction de rappel à exécuter par un thread de travail à partir du pool de threads lorsque le minuteur expire.</span><span class="sxs-lookup"><span data-stu-id="43612-109">You can specify a callback function to be executed by a worker thread from the thread pool when the timer expires.</span></span>

<span data-ttu-id="43612-110">Pour annuler un minuteur en attente, appelez la fonction [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) .</span><span class="sxs-lookup"><span data-stu-id="43612-110">To cancel a pending timer, call the [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) function.</span></span> <span data-ttu-id="43612-111">Lorsque vous avez terminé avec la file d’attente des minuteries, appelez la fonction [**DeleteTimerQueueEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) pour supprimer la file d’attente du minuteur.</span><span class="sxs-lookup"><span data-stu-id="43612-111">When you are finished with the queue of timers, call the [**DeleteTimerQueueEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) function to delete the timer queue.</span></span> <span data-ttu-id="43612-112">Les minuteries en attente dans la file d’attente sont annulées et supprimées.</span><span class="sxs-lookup"><span data-stu-id="43612-112">Any pending timers in the queue are canceled and deleted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43612-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="43612-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43612-114">Utilisation des files d’attente du minuteur</span><span class="sxs-lookup"><span data-stu-id="43612-114">Using Timer Queues</span></span>](using-timer-queues.md)
</dt> </dl>

 

 
