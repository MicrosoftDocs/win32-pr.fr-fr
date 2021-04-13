---
description: Spécifie un identificateur de tâche du service Planificateur de classes multimédias (MMCSS) pour une branche de topologie.
ms.assetid: ccecc1e6-2d30-4e89-849f-c3acad97f312
title: Attribut MF_TOPONODE_WORKQUEUE_MMCSS_TASKID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53af119c58d725d42ec5737ffd9bf96286a65ac1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527411"
---
# <a name="mf_toponode_workqueue_mmcss_taskid-attribute"></a><span data-ttu-id="adcb8-103">MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId, attribut</span><span class="sxs-lookup"><span data-stu-id="adcb8-103">MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID attribute</span></span>

<span data-ttu-id="adcb8-104">Spécifie un identificateur de tâche du service Planificateur de classes multimédias (MMCSS) pour une branche de topologie.</span><span class="sxs-lookup"><span data-stu-id="adcb8-104">Specifies a Multimedia Class Scheduler Service (MMCSS) task identifier for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="adcb8-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="adcb8-105">Data type</span></span>

<span data-ttu-id="adcb8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="adcb8-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="adcb8-107">Notes</span><span class="sxs-lookup"><span data-stu-id="adcb8-107">Remarks</span></span>

<span data-ttu-id="adcb8-108">Cet attribut s’applique aux nœuds sources (**\_ \_ \_ nœud SOURCESTREAM de topologie MF**).</span><span class="sxs-lookup"><span data-stu-id="adcb8-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="adcb8-109">Cet attribut est facultatif.</span><span class="sxs-lookup"><span data-stu-id="adcb8-109">This attribute is optional.</span></span>

<span data-ttu-id="adcb8-110">Cet attribut est ignoré, sauf si les attributs suivants sont également définis :</span><span class="sxs-lookup"><span data-stu-id="adcb8-110">This attribute is ignored unless the following attributes are also set:</span></span>

-   [<span data-ttu-id="adcb8-111">**\_ID de \_ WORKQUEUE \_ TOPONODE MF**</span><span class="sxs-lookup"><span data-stu-id="adcb8-111">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
-   [<span data-ttu-id="adcb8-112">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS, \_ classe**</span><span class="sxs-lookup"><span data-stu-id="adcb8-112">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)

<span data-ttu-id="adcb8-113">Si l’application inscrit l’un de ses propres threads avec MMCSS, vous pouvez utiliser cet attribut pour associer la file d’attente de travail de la topologie au groupe MMCSS de l’application.</span><span class="sxs-lookup"><span data-stu-id="adcb8-113">If the application registers one of its own threads with MMCSS, you can use this attribute to associate the topology work queue with the application's MMCSS group.</span></span> <span data-ttu-id="adcb8-114">Affectez à l’attribut une valeur égale à l’identificateur de tâche que l’application a reçu quand elle est inscrite auprès de MMCSS.</span><span class="sxs-lookup"><span data-stu-id="adcb8-114">Set the attribute value equal to the task identifier that the application received when it registered with MMCSS.</span></span> <span data-ttu-id="adcb8-115">(L’identificateur de tâche est retourné dans le paramètre *TaskIndex* de la fonction [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) .</span><span class="sxs-lookup"><span data-stu-id="adcb8-115">(The task identifier is returned in the *TaskIndex* parameter of the [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) function.</span></span> <span data-ttu-id="adcb8-116">Pour plus d’informations, consultez la rubrique [fonctions de processus et de thread](../procthread/process-and-thread-functions.md).)</span><span class="sxs-lookup"><span data-stu-id="adcb8-116">For more information, see the topic [Process and Thread Functions](../procthread/process-and-thread-functions.md).)</span></span>

<span data-ttu-id="adcb8-117">Si vous souhaitez que MMCSS assigne un nouvel identificateur de tâche pour la topologie, définissez l’attribut de [**\_ \_ \_ \_ classe WORKQUEUE MMCSS TOPONODE MF**](mf-toponode-workqueue-mmcss-class-attribute.md) , mais ne définissez pas l’attribut **MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId** .</span><span class="sxs-lookup"><span data-stu-id="adcb8-117">If you want MMCSS to assign a new task identifier for the topology, set the [**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**](mf-toponode-workqueue-mmcss-class-attribute.md) attribute, but do not set the **MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID** attribute.</span></span>

<span data-ttu-id="adcb8-118">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="adcb8-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="adcb8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adcb8-119">Requirements</span></span>



| <span data-ttu-id="adcb8-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="adcb8-120">Requirement</span></span> | <span data-ttu-id="adcb8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="adcb8-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="adcb8-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="adcb8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="adcb8-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="adcb8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="adcb8-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="adcb8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="adcb8-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="adcb8-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="adcb8-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="adcb8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="adcb8-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="adcb8-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adcb8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adcb8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adcb8-129">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="adcb8-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="adcb8-130">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="adcb8-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="adcb8-131">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="adcb8-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="adcb8-132">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="adcb8-132">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="adcb8-133">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="adcb8-133">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="adcb8-134">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="adcb8-134">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="adcb8-135">Files d’attente de travail</span><span class="sxs-lookup"><span data-stu-id="adcb8-135">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 
