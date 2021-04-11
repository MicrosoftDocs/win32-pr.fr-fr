---
description: Spécifie un descripteur de socket utilisé par les demandes d’envoi et de réception avec les extensions d’e/s inscrites par Winsock.
ms.assetid: 50E9516C-6078-4466-A593-3F29E4783740
title: RIO_RQ (Mswsockdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c25abebbe40842532f3cca180868b5b3786e756d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318873"
---
# <a name="rio_rq"></a><span data-ttu-id="5dad4-103">RIO \_ RQ</span><span class="sxs-lookup"><span data-stu-id="5dad4-103">RIO\_RQ</span></span>

<span data-ttu-id="5dad4-104">Le typedef **Rio \_ RQ** spécifie un descripteur de socket utilisé par les demandes d’envoi et de réception avec les extensions d’e/s inscrites Winsock.</span><span class="sxs-lookup"><span data-stu-id="5dad4-104">The **RIO\_RQ** typedef specifies a socket descriptor used by send and receive requests with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_RQ_t* RIO_RQ, **PRIO_RQ;
```



<dl> <dt>

<span data-ttu-id="5dad4-105">**RIO \_ RQ**</span><span class="sxs-lookup"><span data-stu-id="5dad4-105">**RIO\_RQ**</span></span>
</dt> <dd>

<span data-ttu-id="5dad4-106">Type de données qui spécifie un descripteur de socket utilisé par les demandes d’envoi et de réception.</span><span class="sxs-lookup"><span data-stu-id="5dad4-106">A data type that specifies a socket descriptor used by send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5dad4-107">Notes</span><span class="sxs-lookup"><span data-stu-id="5dad4-107">Remarks</span></span>

<span data-ttu-id="5dad4-108">Les extensions d’e/s inscrites par Winsock fonctionnent principalement sur un objet **Rio \_ RQ** plutôt que sur un Socket.</span><span class="sxs-lookup"><span data-stu-id="5dad4-108">The Winsock registered I/O extensions operate primarily on a **RIO\_RQ** object rather than a socket.</span></span> <span data-ttu-id="5dad4-109">Une application obtient un **Rio \_ RQ** pour un socket existant à l’aide de la fonction [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) .</span><span class="sxs-lookup"><span data-stu-id="5dad4-109">An application obtains a **RIO\_RQ** for an existing socket using the [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) function.</span></span> <span data-ttu-id="5dad4-110">Le socket d’entrée doit avoir été créé en appelant la fonction [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) avec l’indicateur WSA de l' **\_ indicateur \_ Rio** défini dans le paramètre *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="5dad4-110">The input socket must have been created by calling the [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) function with the **WSA\_FLAG\_RIO** flag set in the *dwFlags* parameter.</span></span>

<span data-ttu-id="5dad4-111">Après avoir obtenu un objet **Rio \_ RQ** , le descripteur de Socket sous-jacent reste valide.</span><span class="sxs-lookup"><span data-stu-id="5dad4-111">After obtaining a **RIO\_RQ** object, the underlying socket descriptor remains valid.</span></span> <span data-ttu-id="5dad4-112">Une application peut continuer à utiliser le Socket sous-jacent pour définir et interroger les options de socket, émettre des IOCTL et finalement fermer le Socket.</span><span class="sxs-lookup"><span data-stu-id="5dad4-112">An application may continue to use the underlying socket to set and query socket options, issue IOCTLs and ultimately close the socket.</span></span>

> [!Note]  
> <span data-ttu-id="5dad4-113">À des fins d’efficacité, l’accès aux files d’attente de saisie semi-automatique ([**Rio \_ CQ**](riocqueue.md) structs) et aux files d’attente de requêtes (structs de **Rio \_ RQ** ) ne sont pas protégés par les primitives de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="5dad4-113">For purposes of efficiency, access to the completion queues ([**RIO\_CQ**](riocqueue.md) structs) and request queues (**RIO\_RQ** structs) are not protected by synchronization primitives.</span></span> <span data-ttu-id="5dad4-114">Si vous avez besoin d’accéder à une file d’attente de saisie semi-automatique ou de demande à partir de plusieurs threads, l’accès doit être coordonné par une section critique, un verrou d’écriture de lecteur allégé ou un mécanisme similaire.</span><span class="sxs-lookup"><span data-stu-id="5dad4-114">If you need to access a completion or request queue from multiple threads, access should be coordinated by a critical section, slim reader write lock or similar mechanism.</span></span> <span data-ttu-id="5dad4-115">Ce verrouillage n’est pas nécessaire pour l’accès par un seul thread.</span><span class="sxs-lookup"><span data-stu-id="5dad4-115">This locking is not needed for access by a single thread.</span></span> <span data-ttu-id="5dad4-116">Différents threads peuvent accéder à des files d’attente de demandes/de saisie semi-automatique distinctes sans verrous.</span><span class="sxs-lookup"><span data-stu-id="5dad4-116">Different threads can access separate requests/completion queues without locks.</span></span> <span data-ttu-id="5dad4-117">La nécessité d’une synchronisation se produit uniquement lorsque plusieurs threads essaient d’accéder à la même file d’attente.</span><span class="sxs-lookup"><span data-stu-id="5dad4-117">The need for synchronization occurs only when multiple threads try to access the same queue.</span></span> <span data-ttu-id="5dad4-118">La synchronisation est également requise si plusieurs threads émettent un problème d’envoi et de réception sur le même socket, car les opérations d’envoi et de réception utilisent la file d’attente des demandes du Socket.</span><span class="sxs-lookup"><span data-stu-id="5dad4-118">Synchronization is also required if multiple threads issue sends and receives on the same socket because the send and receive operations use the socket’s request queue.</span></span>

 

<span data-ttu-id="5dad4-119">Le typedef [**Rio \_ RQ**](riocqueue.md) est défini dans le fichier d’en-tête *Mswsockdef. h* qui est automatiquement inclus dans le fichier d’en-tête *mswsock. h* .</span><span class="sxs-lookup"><span data-stu-id="5dad4-119">The [**RIO\_RQ**](riocqueue.md) typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="5dad4-120">Le fichier d’en-tête *Mswsockdef. h* ne doit jamais être utilisé directement.</span><span class="sxs-lookup"><span data-stu-id="5dad4-120">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dad4-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5dad4-121">Requirements</span></span>



| <span data-ttu-id="5dad4-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5dad4-122">Requirement</span></span> | <span data-ttu-id="5dad4-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5dad4-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dad4-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dad4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5dad4-125">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5dad4-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="5dad4-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dad4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5dad4-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5dad4-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="5dad4-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="5dad4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dad4-129"><dt>Mswsockdef. h (inclure mswsock. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5dad4-129"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dad4-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dad4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dad4-131">**RIOCreateRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="5dad4-131">**RIOCreateRequestQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[<span data-ttu-id="5dad4-132">**RIOReceive**</span><span class="sxs-lookup"><span data-stu-id="5dad4-132">**RIOReceive**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[<span data-ttu-id="5dad4-133">**RIOReceiveEx**</span><span class="sxs-lookup"><span data-stu-id="5dad4-133">**RIOReceiveEx**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

<span data-ttu-id="5dad4-134">[**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5dad4-134">[**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5dad4-135">**RIOSend**</span><span class="sxs-lookup"><span data-stu-id="5dad4-135">**RIOSend**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

<span data-ttu-id="5dad4-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5dad4-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5dad4-137">**WSASocket**</span><span class="sxs-lookup"><span data-stu-id="5dad4-137">**WSASocket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)
</dt> </dl>

 

 
