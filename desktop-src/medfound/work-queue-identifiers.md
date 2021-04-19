---
description: Les constantes suivantes identifient les files d’attente de travail de Media Foundation standard.
ms.assetid: c769f876-83ca-4b04-a054-22fa7146310e
title: Identificateurs de file d’attente de travail (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecff594bad2a4595862f0bc6457644f86949d42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529869"
---
# <a name="work-queue-identifiers"></a><span data-ttu-id="d350a-103">Identificateurs de file d’attente de travail</span><span class="sxs-lookup"><span data-stu-id="d350a-103">Work Queue Identifiers</span></span>

<span data-ttu-id="d350a-104">Les constantes suivantes identifient les files d’attente de travail de Media Foundation standard.</span><span class="sxs-lookup"><span data-stu-id="d350a-104">The following constants identify the standard Media Foundation work queues.</span></span>

<span data-ttu-id="d350a-105">Les applications doivent utiliser \_ \_ la file d’attente de rappel MFASYNC \_ multithread ou utiliser une file d’attente de travail obtenue à partir de [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) si elles souhaitent contrôler la priorité d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d350a-105">Applications should use MFASYNC\_CALLBACK\_QUEUE\_MULTITHREADED or use a work queue obtained from [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) if they want to control the execution priority.</span></span> <span data-ttu-id="d350a-106">Notez que les priorités de la file d’attente de travail de la plateforme par défaut peuvent changer dynamiquement lorsqu’une application appelle [**RegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss).</span><span class="sxs-lookup"><span data-stu-id="d350a-106">Note that the default platform work queue priorities can dynamically change when an application calls [**RegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss).</span></span> <span data-ttu-id="d350a-107">Pour plus d’informations sur les files d’attente de travail, consultez [files d’attente de travail](work-queues.md).</span><span class="sxs-lookup"><span data-stu-id="d350a-107">For more information about work queues, see [Work Queues](work-queues.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="d350a-108">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="d350a-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="d350a-109">Description</span><span class="sxs-lookup"><span data-stu-id="d350a-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_STANDARD"></span><span id="mfasync_callback_queue_standard"></span><dl> <span data-ttu-id="d350a-110"><dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="d350a-110"><dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d350a-111">Dans la plupart des cas, les applications doivent utiliser <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span><span class="sxs-lookup"><span data-stu-id="d350a-111">In most cases, applications should use <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span></span><br/> <span data-ttu-id="d350a-112">Cette file d’attente de travail est utilisée pour les opérations synchrones.</span><span class="sxs-lookup"><span data-stu-id="d350a-112">This work queue is used for synchronous operations.</span></span> <span data-ttu-id="d350a-113">L’utilisation de la file d’attente de travail standard peut courir le risque de blocage.</span><span class="sxs-lookup"><span data-stu-id="d350a-113">Using the standard work queue may run the risk of deadlocking.</span></span> <span data-ttu-id="d350a-114">Les applications peuvent créer une file d’attente synchrone privée en plus de la file d’attente multithread à l’aide de <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MFAllocateSerialWorkQueue</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d350a-114">Applications can create a private synchronous queue on top of the multithreaded queue by using <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MFAllocateSerialWorkQueue</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_RT"></span><span id="mfasync_callback_queue_rt"></span><dl> <span data-ttu-id="d350a-115"><dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt> <dt>0x00000002</dt> </span><span class="sxs-lookup"><span data-stu-id="d350a-115"><dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt> <dt>0x00000002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d350a-116">Pas pour l’utilisation générale des applications.</span><span class="sxs-lookup"><span data-stu-id="d350a-116">Not for general application use.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_IO"></span><span id="mfasync_callback_queue_io"></span><dl> <span data-ttu-id="d350a-117"><dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt> <dt>0x00000003</dt> </span><span class="sxs-lookup"><span data-stu-id="d350a-117"><dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt> <dt>0x00000003</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d350a-118">Pas pour l’utilisation générale des applications.</span><span class="sxs-lookup"><span data-stu-id="d350a-118">Not for general application use.</span></span><br/> <span data-ttu-id="d350a-119">Cette file d’attente de travail est utilisée en interne pour les opérations d’e/s telles que la lecture de fichiers et la lecture à partir du réseau.</span><span class="sxs-lookup"><span data-stu-id="d350a-119">This work queue is used internally for I/O operations such as reading files and reading from the network.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_TIMER"></span><span id="mfasync_callback_queue_timer"></span><dl> <span data-ttu-id="d350a-120"><dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt> <dt>0x00000004</dt> </span><span class="sxs-lookup"><span data-stu-id="d350a-120"><dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt> <dt>0x00000004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d350a-121">Pas pour l’utilisation générale des applications.</span><span class="sxs-lookup"><span data-stu-id="d350a-121">Not for general application use.</span></span><br/> <span data-ttu-id="d350a-122">Cette file d’attente de travail est utilisée pour les rappels périodiques et les éléments de travail planifiés.</span><span class="sxs-lookup"><span data-stu-id="d350a-122">This work queue is used for periodic callbacks and scheduled work items.</span></span> <span data-ttu-id="d350a-123">Les fonctions suivantes placent les éléments de travail dans cette file d’attente :</span><span class="sxs-lookup"><span data-stu-id="d350a-123">The following functions put work items in this queue:</span></span><br/>
<ul>
<li><span data-ttu-id="d350a-124"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>MFAddPeriodicCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="d350a-124"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>MFAddPeriodicCallback</strong></a></span></span></li>
<li><span data-ttu-id="d350a-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MFScheduleWorkItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="d350a-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MFScheduleWorkItem</strong></a></span></span></li>
<li><span data-ttu-id="d350a-126"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MFScheduleWorkItemEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="d350a-126"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MFScheduleWorkItemEx</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_MULTITHREADED"></span><span id="mfasync_callback_queue_multithreaded"></span><dl> <span data-ttu-id="d350a-127"><dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt> <dt>0x00000005</dt> </span><span class="sxs-lookup"><span data-stu-id="d350a-127"><dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt> <dt>0x00000005</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d350a-128">Cette file d’attente de travail multithread doit être utilisée dans la plupart des cas.</span><span class="sxs-lookup"><span data-stu-id="d350a-128">This multithreaded work queue should be used in most cases.</span></span> <br/> <span data-ttu-id="d350a-129">Cette file d’attente de travail est utilisée pour les opérations asynchrones tout au long de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d350a-129">This work queue is used for asynchronous operations throughout Media Foundation.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION"></span><span id="mfasync_callback_queue_long_function"></span><dl> <span data-ttu-id="d350a-130"><dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt> <dt>0x00000007</dt> </span><span class="sxs-lookup"><span data-stu-id="d350a-130"><dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt> <dt>0x00000007</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d350a-131">Pas pour l’utilisation générale des applications.</span><span class="sxs-lookup"><span data-stu-id="d350a-131">Not for general application use.</span></span> <span data-ttu-id="d350a-132">À la place, les applications doivent utiliser <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span><span class="sxs-lookup"><span data-stu-id="d350a-132">Applications should instead use <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



<span data-ttu-id="d350a-133">En outre, les constantes suivantes sont utilisées dans le cadre de la connexion aux files d’attente de travail.</span><span class="sxs-lookup"><span data-stu-id="d350a-133">In addition, the following constants are used in connection with work queues.</span></span>



| <span data-ttu-id="d350a-134">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="d350a-134">Constant/value</span></span>                                                                                                                                                                                                                                                                                     | <span data-ttu-id="d350a-135">Description</span><span class="sxs-lookup"><span data-stu-id="d350a-135">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASYNC_CALLBACK_QUEUE_UNDEFINED"></span><span id="mfasync_callback_queue_undefined"></span><dl> <span data-ttu-id="d350a-136"><dt>**MFASYNC \_ \_File d’attente de rappels \_ non définie**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="d350a-136"><dt>**MFASYNC\_CALLBACK\_QUEUE\_UNDEFINED**</dt> <dt>0x00000000</dt></span></span> </dl>           | <span data-ttu-id="d350a-137">File d’attente de travail non définie.</span><span class="sxs-lookup"><span data-stu-id="d350a-137">Undefined work queue.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK"></span><span id="mfasync_callback_queue_private_mask"></span><dl> <span data-ttu-id="d350a-138"><dt>**MFASYNC \_ \_ \_ \_ Masque privé de la file d’attente de rappel**</dt> <dt>0xFFFF0000</dt></span><span class="sxs-lookup"><span data-stu-id="d350a-138"><dt>**MFASYNC\_CALLBACK\_QUEUE\_PRIVATE\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl> | <span data-ttu-id="d350a-139">Masque de bits pour distinguer les files d’attente de travail de plateforme de celles créées en appelant [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span><span class="sxs-lookup"><span data-stu-id="d350a-139">Bit mask to distinguish platform work queues from those created by calling [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span></span><br/> <span data-ttu-id="d350a-140">Pour une file d’attente de travail créée par [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue), la valeur suivante est différente de zéro :</span><span class="sxs-lookup"><span data-stu-id="d350a-140">For a work queue created by [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue), the following value is nonzero:</span></span><br/> `(identifier & MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK)`<br/> |
| <span id="MFASYNC_CALLBACK_QUEUE_ALL"></span><span id="mfasync_callback_queue_all"></span><dl> <span data-ttu-id="d350a-141"><dt>**MFASYNC \_ Mise en \_ file d’attente de rappel \_ toutes les**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="d350a-141"><dt>**MFASYNC\_CALLBACK\_QUEUE\_ALL**</dt> <dt>0xFFFFFFFF</dt></span></span> </dl>                             | <span data-ttu-id="d350a-142">Toutes les files d’attente de travail de plateforme.</span><span class="sxs-lookup"><span data-stu-id="d350a-142">All platform work queues.</span></span><br/>                                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="d350a-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d350a-143">Requirements</span></span>



| <span data-ttu-id="d350a-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d350a-144">Requirement</span></span> | <span data-ttu-id="d350a-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="d350a-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d350a-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d350a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d350a-147">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d350a-147">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d350a-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d350a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d350a-149">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d350a-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d350a-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="d350a-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="d350a-151"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d350a-151"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d350a-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d350a-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d350a-153">Constantes Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d350a-153">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> <dt>

[<span data-ttu-id="d350a-154">Files d’attente de travail</span><span class="sxs-lookup"><span data-stu-id="d350a-154">Work Queues</span></span>](work-queues.md)
</dt> <dt>

[<span data-ttu-id="d350a-155">Améliorations de la file d’attente de travail et du thread</span><span class="sxs-lookup"><span data-stu-id="d350a-155">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 




