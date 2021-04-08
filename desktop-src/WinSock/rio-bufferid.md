---
description: Spécifie un descripteur de mémoire tampon inscrit utilisé avec les extensions d’e/s inscrites Winsock.
ms.assetid: 87D0A3F6-A44C-4D7F-B276-7FD5DC2DE7A3
title: RIO_BUFFERID (Mswsockdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75bb439a567c361a056b750728d986891a1da468
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034263"
---
# <a name="rio_bufferid"></a><span data-ttu-id="65ed8-103">\_l’élément BUFFERID Rio</span><span class="sxs-lookup"><span data-stu-id="65ed8-103">RIO\_BUFFERID</span></span>

<span data-ttu-id="65ed8-104">Le **typedef \_ l’élément bufferID** typedef spécifie un descripteur de mémoire tampon inscrit utilisé avec les extensions d’e/s inscrites Winsock.</span><span class="sxs-lookup"><span data-stu-id="65ed8-104">The **RIO\_BUFFERID** typedef specifies a registered buffer descriptor used with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_BUFFERID_t* RIO_BUFFERID, **PRIO_BUFFERID;
```



<dl> <dt>

<span data-ttu-id="65ed8-105">**\_l’élément BUFFERID Rio**</span><span class="sxs-lookup"><span data-stu-id="65ed8-105">**RIO\_BUFFERID**</span></span>
</dt> <dd>

<span data-ttu-id="65ed8-106">Type de données qui spécifie un descripteur de mémoire tampon inscrit utilisé avec les demandes d’envoi et de réception.</span><span class="sxs-lookup"><span data-stu-id="65ed8-106">A data type that specifies a registered buffer descriptor used with send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65ed8-107">Notes</span><span class="sxs-lookup"><span data-stu-id="65ed8-107">Remarks</span></span>

<span data-ttu-id="65ed8-108">Les extensions d’e/s inscrites par Winsock fonctionnent principalement sur les mémoires tampons enregistrées à l’aide d’objets **Rio \_ l’élément bufferID** .</span><span class="sxs-lookup"><span data-stu-id="65ed8-108">The Winsock registered I/O extensions operate primarily on registered buffers using **RIO\_BUFFERID** objects.</span></span> <span data-ttu-id="65ed8-109">Une application obtient un **\_ l’élément bufferID Rio** pour une mémoire tampon existante à l’aide de la fonction [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="65ed8-109">An application obtains a **RIO\_BUFFERID** for an existing buffer using the [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) function.</span></span> <span data-ttu-id="65ed8-110">Une application peut libérer une inscription à l’aide de la fonction [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) .</span><span class="sxs-lookup"><span data-stu-id="65ed8-110">An application can release a registration using the [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) function.</span></span>

<span data-ttu-id="65ed8-111">Lorsqu’une mémoire tampon existante est inscrite en tant qu’objet **Rio \_ l’élément bufferID** à l’aide de la fonction [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) , certaines ressources internes sont allouées à partir de la mémoire physique et la mémoire tampon de l’application existante est verrouillée dans la mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="65ed8-111">When an existing buffer is registered as a **RIO\_BUFFERID** object using the [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) function, certain internal resources are allocated from physical memory, and the existing application buffer will be locked into physical memory.</span></span> <span data-ttu-id="65ed8-112">La fonction [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) est appelée pour annuler l’inscription de la mémoire tampon, libérer ces ressources internes et autoriser le déverrouillage et la libération de la mémoire tampon à partir de la mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="65ed8-112">The [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) function is called to deregister the buffer, free these internal resources, and allow the buffer to be unlocked and released from physical memory.</span></span>

<span data-ttu-id="65ed8-113">L’inscription et la désinscription répétées des tampons d’application à l’aide des extensions d’e/s inscrites par Winsock peuvent entraîner une dégradation significative des performances.</span><span class="sxs-lookup"><span data-stu-id="65ed8-113">Repeated registration and deregistration of application buffers using the Winsock registered I/O extensions may cause significant performance degradation.</span></span> <span data-ttu-id="65ed8-114">Les approches de gestion des mémoires tampons suivantes doivent être prises en compte lors de la conception d’une application à l’aide des extensions d’e/s inscrites par Winsock pour réduire l’inscription et la désinscription répétées des mémoires tampons d’application :</span><span class="sxs-lookup"><span data-stu-id="65ed8-114">The following buffer management approaches should be considered when designing an application using the Winsock registered I/O extensions to minimize repeated registration and deregistration of application buffers:</span></span>

-   <span data-ttu-id="65ed8-115">• Optimisez la réutilisation des tampons.</span><span class="sxs-lookup"><span data-stu-id="65ed8-115">• Maximize the reuse of buffers.</span></span>
-   <span data-ttu-id="65ed8-116">• Conserver un pool limité de mémoires tampons enregistrées inutilisées pour une utilisation par l’application.</span><span class="sxs-lookup"><span data-stu-id="65ed8-116">• Maintain a limited pool of unused registered buffers for use by the application.</span></span>
-   <span data-ttu-id="65ed8-117">• Gérer un pool limité de mémoires tampons enregistrées et effectuer des copies de tampon entre ces mémoires tampons enregistrées et d’autres tampons non inscrits.</span><span class="sxs-lookup"><span data-stu-id="65ed8-117">• Maintain a limited pool of registered buffers and perform buffer copies between these registered buffers and other unregistered buffers.</span></span>

<span data-ttu-id="65ed8-118">Le **typedef \_ l’élément bufferID** typedef est défini dans le fichier d’en-tête *Mswsockdef. h* qui est automatiquement inclus dans le fichier d’en-tête *mswsock. h* .</span><span class="sxs-lookup"><span data-stu-id="65ed8-118">The **RIO\_BUFFERID** typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="65ed8-119">Le fichier d’en-tête *Mswsockdef. h* ne doit jamais être utilisé directement.</span><span class="sxs-lookup"><span data-stu-id="65ed8-119">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="65ed8-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65ed8-120">Requirements</span></span>



| <span data-ttu-id="65ed8-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65ed8-121">Requirement</span></span> | <span data-ttu-id="65ed8-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="65ed8-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65ed8-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65ed8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="65ed8-124">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65ed8-124">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="65ed8-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65ed8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="65ed8-126">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65ed8-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="65ed8-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="65ed8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="65ed8-128"><dt>Mswsockdef. h (inclure mswsock. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65ed8-128"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65ed8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65ed8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ed8-130">**RIO \_ buf**</span><span class="sxs-lookup"><span data-stu-id="65ed8-130">**RIO\_BUF**</span></span>](/windows/desktop/api/Mswsockdef/ns-mswsockdef-rio_buf)
</dt> <dt>

[<span data-ttu-id="65ed8-131">**RIODeregisterBuffer**</span><span class="sxs-lookup"><span data-stu-id="65ed8-131">**RIODeregisterBuffer**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer)
</dt> <dt>

[<span data-ttu-id="65ed8-132">**RIOReceive**</span><span class="sxs-lookup"><span data-stu-id="65ed8-132">**RIOReceive**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[<span data-ttu-id="65ed8-133">**RIOReceiveEx**</span><span class="sxs-lookup"><span data-stu-id="65ed8-133">**RIOReceiveEx**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

<span data-ttu-id="65ed8-134">[**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="65ed8-134">[**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="65ed8-135">**RIOSend**</span><span class="sxs-lookup"><span data-stu-id="65ed8-135">**RIOSend**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

<span data-ttu-id="65ed8-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="65ed8-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span></span>
</dt> </dl>

 

 
