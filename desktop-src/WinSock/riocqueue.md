---
description: Spécifie un descripteur de file d’attente d’achèvement utilisé pour la notification d’achèvement d’e/s par envoi et réception de demandes avec les extensions d’e/s inscrites Winsock.
ms.assetid: 9196F8AF-3C48-445D-B2D5-E22A99759D92
title: RIO_CQ (Mswsockdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ca4376c5b130cccaefd7170f62878f31fd1457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518418"
---
# <a name="rio_cq"></a><span data-ttu-id="181ab-103">RIO \_ CQ</span><span class="sxs-lookup"><span data-stu-id="181ab-103">RIO\_CQ</span></span>

<span data-ttu-id="181ab-104">**Rio \_ CQ** typedef spécifie un descripteur de file d’attente d’achèvement utilisé pour la notification d’achèvement d’e/s par envoi et réception de demandes avec les extensions d’e/s inscrites Winsock.</span><span class="sxs-lookup"><span data-stu-id="181ab-104">The **RIO\_CQ** typedef specifies a completion queue descriptor used for I/O completion notification by send and receive requests with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_CQ_t* RIO_CQ, **PRIO_CQ;
```



<dl> <dt>

<span data-ttu-id="181ab-105">**RIO \_ CQ**</span><span class="sxs-lookup"><span data-stu-id="181ab-105">**RIO\_CQ**</span></span>
</dt> <dd>

<span data-ttu-id="181ab-106">Type de données qui spécifie un descripteur de file d’attente d’achèvement utilisé pour la notification d’achèvement d’e/s par les demandes d’envoi et de réception.</span><span class="sxs-lookup"><span data-stu-id="181ab-106">A data type that specifies a completion queue descriptor used for I/O completion notification by send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="181ab-107">Notes</span><span class="sxs-lookup"><span data-stu-id="181ab-107">Remarks</span></span>

<span data-ttu-id="181ab-108">L’objet **Rio \_ CQ** est utilisé pour la notification d’achèvement d’e/s des demandes d’envoi et de réception de réseau par les extensions d’e/s inscrites par Winsock.</span><span class="sxs-lookup"><span data-stu-id="181ab-108">The **RIO\_CQ** object is used for I/O completion notification of send and receive networking requests by the Winsock registered I/O extensions.</span></span>

<span data-ttu-id="181ab-109">Une application peut utiliser la fonction [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) pour demander une notification quand une file d’attente de saisie semi-automatique **Rio \_ CQ** n’est pas vide.</span><span class="sxs-lookup"><span data-stu-id="181ab-109">An application can use the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) function to request notification when a **RIO\_CQ** completion queue is not empty.</span></span> <span data-ttu-id="181ab-110">Une application peut également interroger l’État à tout moment d’une file d’attente de saisie semi-automatique **Rio \_ CQ** de façon non bloquante à l’aide de la fonction [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) .</span><span class="sxs-lookup"><span data-stu-id="181ab-110">An application can also poll the status at any time of a **RIO\_CQ** completion queue in a non-blocking way using the [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) function.</span></span>

<span data-ttu-id="181ab-111">L’objet **Rio \_ CQ** est créé à l’aide de la fonction [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) .</span><span class="sxs-lookup"><span data-stu-id="181ab-111">The **RIO\_CQ** object is created using the [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) function.</span></span> <span data-ttu-id="181ab-112">Au moment de la création, l’application doit spécifier la taille de la file d’attente, qui détermine le nombre d’entrées de saisie semi-automatique qu’elle peut contenir.</span><span class="sxs-lookup"><span data-stu-id="181ab-112">At creation time, the application must specify the size of the queue, which determines how many completion entries it can hold.</span></span> <span data-ttu-id="181ab-113">Quand une application appelle la fonction [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) pour obtenir une poignée [**Rio \_ RQ**](riorqueue.md) , l’application doit spécifier un handle de **Rio \_ CQ** pour les saisies semi-automatiques d’envoi et un handle de **Rio \_ CQ** pour les saisies semi-automatiques.</span><span class="sxs-lookup"><span data-stu-id="181ab-113">When an application calls the [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) function to obtain a [**RIO\_RQ**](riorqueue.md) handle, the application must specify a **RIO\_CQ** handle for send completions and a **RIO\_CQ** handle for receive completions.</span></span> <span data-ttu-id="181ab-114">Ces handles peuvent être identiques lorsque la même file d’attente doit être utilisée pour l’envoi et la réception.</span><span class="sxs-lookup"><span data-stu-id="181ab-114">These handles may be identical when the same queue should be used for send and receive completion.</span></span> <span data-ttu-id="181ab-115">La fonction **RIOCreateRequestQueue** nécessite également un nombre maximal d’opérations d’envoi et de réception en attente, qui sont facturées en fonction de la capacité de la file d’attente de saisie semi-automatique ou des files d’attente associées.</span><span class="sxs-lookup"><span data-stu-id="181ab-115">The **RIOCreateRequestQueue** function also requires a maximum number of outstanding send and receive operations, which are charged against the capacity of the associated completion queue or queues.</span></span> <span data-ttu-id="181ab-116">Si les files d’attente n’ont pas suffisamment de capacité restante, l’appel **RIOCreateRequestQueue** échoue avec [WSAENOBUFS](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="181ab-116">If the queues do not have sufficient capacity remaining, the **RIOCreateRequestQueue** call will fail with [WSAENOBUFS](windows-sockets-error-codes-2.md).</span></span>

<span data-ttu-id="181ab-117">Le comportement de notification pour une file d’attente de saisie semi-automatique est défini lors de la création de **Rio \_ CQ** .</span><span class="sxs-lookup"><span data-stu-id="181ab-117">The notification behavior for a completion queue is set when the **RIO\_CQ** is created.</span></span>

<span data-ttu-id="181ab-118">Pour une file d’attente de saisie semi-automatique qui utilise un événement, le membre de **type** de la structure de [**\_ \_ fin de notification Rio**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) est défini sur l’exécution de l' **\_ événement \_ Rio**.</span><span class="sxs-lookup"><span data-stu-id="181ab-118">For a completion queue that uses an event, the **Type** member of the [**RIO\_NOTIFICATION\_COMPLETION**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) structure is set to **RIO\_EVENT\_COMPLETION**.</span></span> <span data-ttu-id="181ab-119">Le membre **Event. EventHandle** doit contenir le descripteur d’un événement créé par la fonction [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) ou [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) .</span><span class="sxs-lookup"><span data-stu-id="181ab-119">The **Event.EventHandle** member should contain the handle for an event created by the [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) or [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function.</span></span> <span data-ttu-id="181ab-120">Pour recevoir la saisie semi-automatique de [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) , l’application doit attendre le handle d’événement spécifié à l’aide de [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) ou d’une routine d’attente similaire.</span><span class="sxs-lookup"><span data-stu-id="181ab-120">To receive the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) completion, the application should wait on the specified event handle using [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) or a similar wait routine.</span></span> <span data-ttu-id="181ab-121">Si l’application prévoit de réinitialiser et de réutiliser l’événement, l’application peut réduire la charge en définissant le membre **Event. NotifyReset** sur une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="181ab-121">If the application plans to reset and reuse the event, the application can reduce overhead by setting the **Event.NotifyReset** member to a non-zero value.</span></span> <span data-ttu-id="181ab-122">Cela entraîne la réinitialisation automatique de l’événement par la fonction **RIONotify** lorsque la notification se produit.</span><span class="sxs-lookup"><span data-stu-id="181ab-122">This causes the event to be automatically reset by the **RIONotify** function when the notification occurs.</span></span> <span data-ttu-id="181ab-123">Cela réduit le besoin d’appeler la fonction [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) pour réinitialiser l’événement entre les appels à la fonction **RIONotify** .</span><span class="sxs-lookup"><span data-stu-id="181ab-123">This mitigates the need to call the [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) function to reset the event between calls to the **RIONotify** function.</span></span>

<span data-ttu-id="181ab-124">Pour une file d’attente de saisie semi-automatique qui utilise un port de terminaison d’e/s, le membre de **type** de la structure de [**\_ \_ fin de notification Rio**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) a la valeur **Rio \_ IOCP \_ completion**.</span><span class="sxs-lookup"><span data-stu-id="181ab-124">For a completion queue that uses an I/O completion port, the **Type** member of the [**RIO\_NOTIFICATION\_COMPLETION**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) structure is set to **RIO\_IOCP\_COMPLETION**.</span></span> <span data-ttu-id="181ab-125">Le membre **Iocp. IocpHandle** doit contenir le descripteur d’un port de terminaison d’e/s créé par la fonction [**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport) .</span><span class="sxs-lookup"><span data-stu-id="181ab-125">The **Iocp.IocpHandle** member should contain the handle for an I/O completion port created by the [**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport) function.</span></span> <span data-ttu-id="181ab-126">Pour recevoir la saisie semi-automatique de [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) , l’application doit appeler la fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) ou [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) .</span><span class="sxs-lookup"><span data-stu-id="181ab-126">To receive the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) completion, the application should call the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) or [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) function.</span></span> <span data-ttu-id="181ab-127">L’application doit fournir un objet [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) dédié pour la file d’attente de saisie semi-automatique, et elle peut également utiliser le membre **Iocp. CompletionKey** pour distinguer les demandes **RIONotify** sur la file d’attente d’achèvement des autres terminaisons d’e/s, y compris les saisies semi-automatiques **RIONotify** pour d’autres files d’attente de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="181ab-127">The application should provide a dedicated [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) object for the completion queue, and it may also use the **Iocp.CompletionKey** member to distinguish **RIONotify** requests on the completion queue from other I/O completions including **RIONotify** completions for other completion queues.</span></span>

> [!Note]  
> <span data-ttu-id="181ab-128">À des fins d’efficacité, l’accès aux files d’attente de saisie semi-automatique (**Rio \_ CQ** structs) et aux files d’attente de requêtes (structs de [**Rio \_ RQ**](riorqueue.md) ) ne sont pas protégés par les primitives de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="181ab-128">For purposes of efficiency, access to the completion queues (**RIO\_CQ** structs) and request queues ([**RIO\_RQ**](riorqueue.md) structs) are not protected by synchronization primitives.</span></span> <span data-ttu-id="181ab-129">Si vous avez besoin d’accéder à une file d’attente de saisie semi-automatique ou de demande à partir de plusieurs threads, l’accès doit être coordonné par une section critique, un verrou d’écriture de lecteur allégé ou un mécanisme similaire.</span><span class="sxs-lookup"><span data-stu-id="181ab-129">If you need to access a completion or request queue from multiple threads, access should be coordinated by a critical section, slim reader write lock or similar mechanism.</span></span> <span data-ttu-id="181ab-130">Ce verrouillage n’est pas nécessaire pour l’accès par un seul thread.</span><span class="sxs-lookup"><span data-stu-id="181ab-130">This locking is not needed for access by a single thread.</span></span> <span data-ttu-id="181ab-131">Différents threads peuvent accéder à des files d’attente de demandes/de saisie semi-automatique distinctes sans verrous.</span><span class="sxs-lookup"><span data-stu-id="181ab-131">Different threads can access separate requests/completion queues without locks.</span></span> <span data-ttu-id="181ab-132">La nécessité d’une synchronisation se produit uniquement lorsque plusieurs threads essaient d’accéder à la même file d’attente.</span><span class="sxs-lookup"><span data-stu-id="181ab-132">The need for synchronization occurs only when multiple threads try to access the same queue.</span></span> <span data-ttu-id="181ab-133">La synchronisation est également requise si plusieurs threads émettent un problème d’envoi et de réception sur le même socket, car les opérations d’envoi et de réception utilisent la file d’attente des demandes du Socket.</span><span class="sxs-lookup"><span data-stu-id="181ab-133">Synchronization is also required if multiple threads issue sends and receives on the same socket because the send and receive operations use the socket’s request queue.</span></span>

 

<span data-ttu-id="181ab-134">Si plusieurs threads tentent d’accéder au même **Rio \_ CQ** à l’aide de [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), l’accès doit être coordonné par une section critique, un verrou de writer de lecteur Slim ou un mécanisme d’exclusion mutuelle similaire.</span><span class="sxs-lookup"><span data-stu-id="181ab-134">If multiple threads attempt to access the same **RIO\_CQ** using [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), access must be coordinated by a critical section, slim reader writer lock , or similar mutual exclusion mechanism.</span></span> <span data-ttu-id="181ab-135">Si les files d’attente de saisie semi-automatique ne sont pas partagées, l’exclusion mutuelle n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="181ab-135">If the completion queues are not shared, mutual exclusion is not required.</span></span>

<span data-ttu-id="181ab-136">Lorsqu’une file d’attente de saisie semi-automatique n’est plus nécessaire, une application peut la fermer à l’aide de la fonction [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="181ab-136">When a completion queue is no longer needed, an application can close it using the [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) function.</span></span>

<span data-ttu-id="181ab-137">Le **typedef \_ CQ CQ** est défini dans le fichier d’en-tête *Mswsockdef. h* qui est automatiquement inclus dans le fichier d’en-tête *mswsock. h* .</span><span class="sxs-lookup"><span data-stu-id="181ab-137">The **RIO\_CQ** typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="181ab-138">Le fichier d’en-tête *Mswsockdef. h* ne doit jamais être utilisé directement.</span><span class="sxs-lookup"><span data-stu-id="181ab-138">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="181ab-139">Cohérence de thread</span><span class="sxs-lookup"><span data-stu-id="181ab-139">Thread Safety</span></span>

<span data-ttu-id="181ab-140">Si plusieurs threads tentent d’accéder au même **Rio \_ CQ** à l’aide de [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), l’accès doit être coordonné par une section critique, un verrou de writer de lecteur Slim ou un mécanisme d’exclusion mutuelle similaire.</span><span class="sxs-lookup"><span data-stu-id="181ab-140">If multiple threads attempt to access the same **RIO\_CQ** using [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), access must be coordinated by a critical section, slim reader writer lock , or similar mutual exclusion mechanism.</span></span> <span data-ttu-id="181ab-141">Si les files d’attente de saisie semi-automatique ne sont pas partagées, l’exclusion mutuelle n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="181ab-141">If the completion queues are not shared, mutual exclusion is not required.</span></span>

## <a name="requirements"></a><span data-ttu-id="181ab-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="181ab-142">Requirements</span></span>



| <span data-ttu-id="181ab-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="181ab-143">Requirement</span></span> | <span data-ttu-id="181ab-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="181ab-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="181ab-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="181ab-145">Minimum supported client</span></span><br/> | <span data-ttu-id="181ab-146">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="181ab-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="181ab-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="181ab-147">Minimum supported server</span></span><br/> | <span data-ttu-id="181ab-148">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="181ab-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="181ab-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="181ab-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="181ab-150"><dt>Mswsockdef. h (inclure mswsock. h)</dt></span><span class="sxs-lookup"><span data-stu-id="181ab-150"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="181ab-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="181ab-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="181ab-152">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="181ab-152">**CreateIoCompletionPort**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport)
</dt> <dt>

[<span data-ttu-id="181ab-153">**CreateEvent**</span><span class="sxs-lookup"><span data-stu-id="181ab-153">**CreateEvent**</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="181ab-154">**GetQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="181ab-154">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="181ab-155">**GetQueuedCompletionStatusEx**</span><span class="sxs-lookup"><span data-stu-id="181ab-155">**GetQueuedCompletionStatusEx**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex)
</dt> <dt>

[<span data-ttu-id="181ab-156">**AVEC chevauchement**</span><span class="sxs-lookup"><span data-stu-id="181ab-156">**OVERLAPPED**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)
</dt> <dt>

[<span data-ttu-id="181ab-157">**achèvement de la \_ notification Rio \_**</span><span class="sxs-lookup"><span data-stu-id="181ab-157">**RIO\_NOTIFICATION\_COMPLETION**</span></span>](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion)
</dt> <dt>

[<span data-ttu-id="181ab-158">**\_type de \_ fin de notification Rio \_**</span><span class="sxs-lookup"><span data-stu-id="181ab-158">**RIO\_NOTIFICATION\_COMPLETION\_TYPE**</span></span>](/windows/desktop/api/Mswsock/ne-mswsock-rio_notification_completion_type)
</dt> <dt>

[<span data-ttu-id="181ab-159">**RIO \_ RQ**</span><span class="sxs-lookup"><span data-stu-id="181ab-159">**RIO\_RQ**</span></span>](riorqueue.md)
</dt> <dt>

<span data-ttu-id="181ab-160">[**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="181ab-160">[**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="181ab-161">**RIOCreateCompletionQueue**</span><span class="sxs-lookup"><span data-stu-id="181ab-161">**RIOCreateCompletionQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[<span data-ttu-id="181ab-162">**RIOCreateRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="181ab-162">**RIOCreateRequestQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[<span data-ttu-id="181ab-163">**RIODequeueCompletion**</span><span class="sxs-lookup"><span data-stu-id="181ab-163">**RIODequeueCompletion**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[<span data-ttu-id="181ab-164">**RIONotify**</span><span class="sxs-lookup"><span data-stu-id="181ab-164">**RIONotify**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify)
</dt> <dt>

[<span data-ttu-id="181ab-165">**WSACreateEvent**</span><span class="sxs-lookup"><span data-stu-id="181ab-165">**WSACreateEvent**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent)
</dt> <dt>

[<span data-ttu-id="181ab-166">**WSAResetEvent**</span><span class="sxs-lookup"><span data-stu-id="181ab-166">**WSAResetEvent**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)
</dt> <dt>

[<span data-ttu-id="181ab-167">**WSAWaitForMultipleEvents**</span><span class="sxs-lookup"><span data-stu-id="181ab-167">**WSAWaitForMultipleEvents**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)
</dt> </dl>

 

 
