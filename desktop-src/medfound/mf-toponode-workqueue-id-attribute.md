---
description: Spécifie une file d’attente de travail pour une branche de topologie.
ms.assetid: 5bc7e2db-cfd2-4b94-b4d6-fe2b9ea9daf8
title: Attribut MF_TOPONODE_WORKQUEUE_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9acda95895a1812f6cebbe64cbf3cd3bcdea4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114022"
---
# <a name="mf_toponode_workqueue_id-attribute"></a><span data-ttu-id="59ff5-103">\_Attribut d' \_ ID WORKQUEUE TOPONODE \_ MF</span><span class="sxs-lookup"><span data-stu-id="59ff5-103">MF\_TOPONODE\_WORKQUEUE\_ID attribute</span></span>

<span data-ttu-id="59ff5-104">Spécifie une file d’attente de travail pour une branche de topologie.</span><span class="sxs-lookup"><span data-stu-id="59ff5-104">Specifies a work queue for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="59ff5-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="59ff5-105">Data type</span></span>

<span data-ttu-id="59ff5-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="59ff5-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="59ff5-107">Notes</span><span class="sxs-lookup"><span data-stu-id="59ff5-107">Remarks</span></span>

<span data-ttu-id="59ff5-108">Cet attribut s’applique aux nœuds sources (**\_ \_ \_ nœud SOURCESTREAM de topologie MF**).</span><span class="sxs-lookup"><span data-stu-id="59ff5-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="59ff5-109">L’attribut est facultatif.</span><span class="sxs-lookup"><span data-stu-id="59ff5-109">The attribute is optional.</span></span>

<span data-ttu-id="59ff5-110">La valeur de l’attribut est un identificateur défini par l’application pour la file d’attente de travail.</span><span class="sxs-lookup"><span data-stu-id="59ff5-110">The value of the attribute is an application-defined identifier for the work queue.</span></span>

<span data-ttu-id="59ff5-111">Les applications peuvent utiliser cet attribut pour assigner des files d’attente de travail à des branches de la topologie.</span><span class="sxs-lookup"><span data-stu-id="59ff5-111">Applications can use this attribute to assign work queues to branches of the topology.</span></span> <span data-ttu-id="59ff5-112">Chaque nœud source de la topologie définit une branche.</span><span class="sxs-lookup"><span data-stu-id="59ff5-112">Each source node in the topology defines one branch.</span></span> <span data-ttu-id="59ff5-113">La branche comprend chaque nœud de topologie qui reçoit des données de ce nœud.</span><span class="sxs-lookup"><span data-stu-id="59ff5-113">The branch includes every topology node that receives data from that node.</span></span>

<span data-ttu-id="59ff5-114">Si vous définissez cet attribut, appelez la méthode [**IMFWorkQueueServices :: BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) sur la topologie résolue.</span><span class="sxs-lookup"><span data-stu-id="59ff5-114">If you set this attribute, call the [**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) method on the resolved topology.</span></span> <span data-ttu-id="59ff5-115">Plusieurs branches de la topologie peuvent partager la même file d’attente de travail, et les files d’attente de travail peuvent être réutilisées entre les topologies.</span><span class="sxs-lookup"><span data-stu-id="59ff5-115">Multiple branches in the topology can share the same work queue, and work queues can be re-used across topologies.</span></span>

> [!Note]  
> <span data-ttu-id="59ff5-116">La valeur de cet attribut n’est pas la même que celle de l’identificateur retourné par la fonction [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) .</span><span class="sxs-lookup"><span data-stu-id="59ff5-116">The value of this attribute is not the same as the identifier that is returned by the [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) function.</span></span> <span data-ttu-id="59ff5-117">La valeur de l’attribut est un identificateur défini par l’application et est utilisée pour associer des branches de topologie à des files d’attente de travail.</span><span class="sxs-lookup"><span data-stu-id="59ff5-117">The value of the attribute is an application-defined identifier, and is used to associate topology branches with work queues.</span></span> <span data-ttu-id="59ff5-118">Lorsque la session multimédia alloue une nouvelle file d’attente de travail, elle stocke l’identificateur de file d’attente de travail réel en interne.</span><span class="sxs-lookup"><span data-stu-id="59ff5-118">When the Media Session allocates a new work queue, it stores the actual work-queue identifier internally.</span></span>

 

<span data-ttu-id="59ff5-119">Si cet attribut est défini, l’application peut également affecter la branche à une tâche du service Planificateur de classes multimédias (MMCSS), en définissant l’attribut de [**\_ \_ \_ \_ classe WORKQUEUE MMCSS TOPONODE MF**](mf-toponode-workqueue-mmcss-class-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="59ff5-119">If this attribute it set, the application can also assign the branch to a Multimedia Class Scheduler Service (MMCSS) task, by setting the [**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**](mf-toponode-workqueue-mmcss-class-attribute.md) attribute.</span></span>

<span data-ttu-id="59ff5-120">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="59ff5-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="59ff5-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59ff5-121">Requirements</span></span>



| <span data-ttu-id="59ff5-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59ff5-122">Requirement</span></span> | <span data-ttu-id="59ff5-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="59ff5-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="59ff5-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59ff5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="59ff5-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59ff5-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="59ff5-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59ff5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="59ff5-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59ff5-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="59ff5-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="59ff5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="59ff5-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="59ff5-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59ff5-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59ff5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59ff5-131">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59ff5-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="59ff5-132">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="59ff5-132">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="59ff5-133">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="59ff5-133">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="59ff5-134">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="59ff5-134">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="59ff5-135">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="59ff5-135">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="59ff5-136">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS, \_ classe**</span><span class="sxs-lookup"><span data-stu-id="59ff5-136">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)
</dt> <dt>

[<span data-ttu-id="59ff5-137">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId**</span><span class="sxs-lookup"><span data-stu-id="59ff5-137">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[<span data-ttu-id="59ff5-138">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="59ff5-138">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="59ff5-139">Files d’attente de travail</span><span class="sxs-lookup"><span data-stu-id="59ff5-139">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 




