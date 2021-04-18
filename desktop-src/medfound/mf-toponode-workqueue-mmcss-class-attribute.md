---
description: Spécifie une tâche du service Planificateur de classes multimédias (MMCSS) pour une branche de topologie.
ms.assetid: 8668d0f1-9d54-4c56-bb19-09498252bec4
title: Attribut MF_TOPONODE_WORKQUEUE_MMCSS_CLASS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 824c9dbdc9b12bbc8fead9ab6ae722fca1e6643a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533769"
---
# <a name="mf_toponode_workqueue_mmcss_class-attribute"></a><span data-ttu-id="ec0d0-103">MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ Class attribut</span><span class="sxs-lookup"><span data-stu-id="ec0d0-103">MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS attribute</span></span>

<span data-ttu-id="ec0d0-104">Spécifie une tâche du [service Planificateur de classes multimédias](../procthread/multimedia-class-scheduler-service.md) (MMCSS) pour une branche de topologie.</span><span class="sxs-lookup"><span data-stu-id="ec0d0-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) task for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="ec0d0-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ec0d0-105">Data type</span></span>

<span data-ttu-id="ec0d0-106">Chaîne de caractères larges</span><span class="sxs-lookup"><span data-stu-id="ec0d0-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="ec0d0-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ec0d0-107">Remarks</span></span>

<span data-ttu-id="ec0d0-108">Cet attribut s’applique aux nœuds sources (**\_ \_ \_ nœud SOURCESTREAM de topologie MF**).</span><span class="sxs-lookup"><span data-stu-id="ec0d0-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="ec0d0-109">Cet attribut est facultatif.</span><span class="sxs-lookup"><span data-stu-id="ec0d0-109">This attribute is optional.</span></span>

<span data-ttu-id="ec0d0-110">Cet attribut requiert l’attribut d' [ \_ \_ \_ ID WORKQUEUE TOPONODE MF](mf-toponode-workqueue-id-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="ec0d0-110">This attribute requires the [MF\_TOPONODE\_WORKQUEUE\_ID](mf-toponode-workqueue-id-attribute.md) attribute.</span></span> <span data-ttu-id="ec0d0-111">Si vous définissez cet attribut, vous devez également définir l’attribut d' **\_ \_ \_ ID de WORKQUEUE TOPONODE MF** sur le même nœud.</span><span class="sxs-lookup"><span data-stu-id="ec0d0-111">If you set this attribute, also set the **MF\_TOPONODE\_WORKQUEUE\_ID** attribute is set on the same node.</span></span>

<span data-ttu-id="ec0d0-112">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ec0d0-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec0d0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec0d0-113">Requirements</span></span>



| <span data-ttu-id="ec0d0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec0d0-114">Requirement</span></span> | <span data-ttu-id="ec0d0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec0d0-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ec0d0-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec0d0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ec0d0-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec0d0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ec0d0-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec0d0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ec0d0-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec0d0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ec0d0-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec0d0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec0d0-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec0d0-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec0d0-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec0d0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec0d0-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ec0d0-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ec0d0-124">**IMFAttributes :: GetString**</span><span class="sxs-lookup"><span data-stu-id="ec0d0-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="ec0d0-125">**IMFAttributes :: SetString**</span><span class="sxs-lookup"><span data-stu-id="ec0d0-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="ec0d0-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="ec0d0-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="ec0d0-127">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="ec0d0-127">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="ec0d0-128">**\_ID de \_ WORKQUEUE \_ TOPONODE MF**</span><span class="sxs-lookup"><span data-stu-id="ec0d0-128">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[<span data-ttu-id="ec0d0-129">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId**</span><span class="sxs-lookup"><span data-stu-id="ec0d0-129">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[<span data-ttu-id="ec0d0-130">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="ec0d0-130">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="ec0d0-131">Files d’attente de travail</span><span class="sxs-lookup"><span data-stu-id="ec0d0-131">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 
