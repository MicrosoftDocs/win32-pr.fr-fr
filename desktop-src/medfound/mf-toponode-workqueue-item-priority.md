---
description: Spécifie la priorité de l’élément de travail pour une branche de la topologie.
ms.assetid: B2FA1151-08D3-46F9-A38D-AC8908EFA6A2
title: Attribut MF_TOPONODE_WORKQUEUE_ITEM_PRIORITY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5f7df6630e41a32eeb069c2a07b8030da79929
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201720"
---
# <a name="mf_toponode_workqueue_item_priority-attribute"></a><span data-ttu-id="9d6f3-103">Attribut de priorité de l' \_ \_ élément WORKQUEUE TOPONODE \_ MF \_</span><span class="sxs-lookup"><span data-stu-id="9d6f3-103">MF\_TOPONODE\_WORKQUEUE\_ITEM\_PRIORITY attribute</span></span>

<span data-ttu-id="9d6f3-104">Spécifie la priorité de l’élément de travail pour une branche de la topologie.</span><span class="sxs-lookup"><span data-stu-id="9d6f3-104">Specifies the work-item priority for a branch of the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="9d6f3-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="9d6f3-105">Data type</span></span>

<span data-ttu-id="9d6f3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9d6f3-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="9d6f3-107">Notes</span><span class="sxs-lookup"><span data-stu-id="9d6f3-107">Remarks</span></span>

<span data-ttu-id="9d6f3-108">Cet attribut s’applique aux nœuds sources (**\_ \_ \_ nœud SOURCESTREAM de topologie MF**).</span><span class="sxs-lookup"><span data-stu-id="9d6f3-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="9d6f3-109">L’attribut est facultatif.</span><span class="sxs-lookup"><span data-stu-id="9d6f3-109">The attribute is optional.</span></span>

<span data-ttu-id="9d6f3-110">Cet attribut requiert l’attribut d' [ \_ \_ \_ ID WORKQUEUE MF TOPONODE](mf-toponode-workqueue-id-attribute.md) sur le même nœud.</span><span class="sxs-lookup"><span data-stu-id="9d6f3-110">This attribute requires the [MF\_TOPONODE\_WORKQUEUE\_ID](mf-toponode-workqueue-id-attribute.md) attribute on the same node.</span></span>

<span data-ttu-id="9d6f3-111">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="9d6f3-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d6f3-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d6f3-112">Requirements</span></span>



| <span data-ttu-id="9d6f3-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d6f3-113">Requirement</span></span> | <span data-ttu-id="9d6f3-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d6f3-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9d6f3-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d6f3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9d6f3-116">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d6f3-116">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9d6f3-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d6f3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9d6f3-118">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d6f3-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9d6f3-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d6f3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d6f3-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d6f3-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d6f3-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d6f3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d6f3-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9d6f3-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9d6f3-123">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="9d6f3-123">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="9d6f3-124">Améliorations de la file d’attente de travail et du thread</span><span class="sxs-lookup"><span data-stu-id="9d6f3-124">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[<span data-ttu-id="9d6f3-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="9d6f3-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="9d6f3-126">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="9d6f3-126">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="9d6f3-127">**\_ID de \_ WORKQUEUE \_ TOPONODE MF**</span><span class="sxs-lookup"><span data-stu-id="9d6f3-127">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
</dt> </dl>

 

 




