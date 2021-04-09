---
description: Spécifie la priorité de thread relative pour une branche de la topologie.
ms.assetid: 7BCD2EE0-94FB-4438-9B6A-7B26DBFB5978
title: Attribut MF_TOPONODE_WORKQUEUE_MMCSS_PRIORITY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0667c91054f8711b8825cf421a2ee565b9161f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114019"
---
# <a name="mf_toponode_workqueue_mmcss_priority-attribute"></a><span data-ttu-id="0c1df-103">MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ Priority attribut</span><span class="sxs-lookup"><span data-stu-id="0c1df-103">MF\_TOPONODE\_WORKQUEUE\_MMCSS\_PRIORITY attribute</span></span>

<span data-ttu-id="0c1df-104">Spécifie la priorité de thread relative pour une branche de la topologie.</span><span class="sxs-lookup"><span data-stu-id="0c1df-104">Specifies the relative thread priority for a branch of the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="0c1df-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="0c1df-105">Data type</span></span>

<span data-ttu-id="0c1df-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0c1df-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0c1df-107">Notes</span><span class="sxs-lookup"><span data-stu-id="0c1df-107">Remarks</span></span>

<span data-ttu-id="0c1df-108">Cet attribut s’applique aux nœuds sources (**\_ \_ \_ nœud SOURCESTREAM de topologie MF**).</span><span class="sxs-lookup"><span data-stu-id="0c1df-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="0c1df-109">L’attribut est facultatif.</span><span class="sxs-lookup"><span data-stu-id="0c1df-109">The attribute is optional.</span></span>

<span data-ttu-id="0c1df-110">Cet attribut requiert l' [ \_ ID de \_ WORKQUEUE \_ MF TOPONODE](mf-toponode-workqueue-id-attribute.md) et les attributs de classe de la [ \_ \_ \_ \_ classe MMCSS TOPONODE WORKQUEUE](mf-toponode-workqueue-mmcss-class-attribute.md) sur le même nœud.</span><span class="sxs-lookup"><span data-stu-id="0c1df-110">This attribute requires the [MF\_TOPONODE\_WORKQUEUE\_ID](mf-toponode-workqueue-id-attribute.md) and [MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS](mf-toponode-workqueue-mmcss-class-attribute.md) attributes on the same node.</span></span>

<span data-ttu-id="0c1df-111">La valeur de l’attribut est la priorité de thread relative de la file d’attente de travail pour cette branche de la topologie.</span><span class="sxs-lookup"><span data-stu-id="0c1df-111">The value of the attribute is the relative thread priority of the work queue for this branch of the topology.</span></span> <span data-ttu-id="0c1df-112">Le [service Planificateur de classes multimédias](../procthread/multimedia-class-scheduler-service.md) (MMCSS) utilise la priorité relative lorsqu’il définit la priorité du thread.</span><span class="sxs-lookup"><span data-stu-id="0c1df-112">The [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) uses the relative priority when it sets the thread priority.</span></span> <span data-ttu-id="0c1df-113">Pour plus d’informations, consultez [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).</span><span class="sxs-lookup"><span data-stu-id="0c1df-113">For more information, see [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).</span></span>

<span data-ttu-id="0c1df-114">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0c1df-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c1df-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c1df-115">Requirements</span></span>



| <span data-ttu-id="0c1df-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c1df-116">Requirement</span></span> | <span data-ttu-id="0c1df-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c1df-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0c1df-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c1df-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0c1df-119">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c1df-119">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0c1df-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c1df-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0c1df-121">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c1df-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0c1df-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c1df-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c1df-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c1df-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c1df-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c1df-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c1df-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0c1df-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0c1df-126">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="0c1df-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="0c1df-127">Améliorations de la file d’attente de travail et du thread</span><span class="sxs-lookup"><span data-stu-id="0c1df-127">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[<span data-ttu-id="0c1df-128">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="0c1df-128">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="0c1df-129">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="0c1df-129">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="0c1df-130">**\_ID de \_ WORKQUEUE \_ TOPONODE MF**</span><span class="sxs-lookup"><span data-stu-id="0c1df-130">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[<span data-ttu-id="0c1df-131">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId**</span><span class="sxs-lookup"><span data-stu-id="0c1df-131">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> </dl>

 

 
