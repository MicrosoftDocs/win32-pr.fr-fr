---
description: Spécifie l’élément qui contient ce nœud source.
ms.assetid: f5fa5c10-8f30-43bd-8054-a39996f807a3
title: Attribut MF_TOPONODE_SEQUENCE_ELEMENTID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3cd2c66c40a0bc3776d2fd2b7d78535cf24b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543096"
---
# <a name="mf_toponode_sequence_elementid-attribute"></a><span data-ttu-id="cdbf5-103">\_ \_ Attribut ELEMENTID de séquence TOPONODE MF \_</span><span class="sxs-lookup"><span data-stu-id="cdbf5-103">MF\_TOPONODE\_SEQUENCE\_ELEMENTID attribute</span></span>

<span data-ttu-id="cdbf5-104">Spécifie l’élément qui contient ce nœud source.</span><span class="sxs-lookup"><span data-stu-id="cdbf5-104">Specifies the element that contains this source node.</span></span>

## <a name="data-type"></a><span data-ttu-id="cdbf5-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="cdbf5-105">Data type</span></span>

<span data-ttu-id="cdbf5-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="cdbf5-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="cdbf5-107">Notes</span><span class="sxs-lookup"><span data-stu-id="cdbf5-107">Remarks</span></span>

<span data-ttu-id="cdbf5-108">Cet attribut s’applique aux nœuds sources (**\_ \_ \_ nœud SOURCESTREAM de topologie MF**).</span><span class="sxs-lookup"><span data-stu-id="cdbf5-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span>

<span data-ttu-id="cdbf5-109">Le pipeline multimédia utilise cet attribut pour déterminer quand les sources multimédias font partie du même élément.</span><span class="sxs-lookup"><span data-stu-id="cdbf5-109">The media pipeline uses this attribute to discover when media sources are part of the same element.</span></span> <span data-ttu-id="cdbf5-110">Le pipeline traite tous les nœuds sources qui font partie du même élément comme ayant la même horloge.</span><span class="sxs-lookup"><span data-stu-id="cdbf5-110">The pipeline treats all source nodes that are part of the same element as having the same clock.</span></span>

<span data-ttu-id="cdbf5-111">Lorsque le pipeline met en file d’attente une nouvelle topologie qui contient des nœuds sources qui font partie d’un élément présent dans la topologie précédente, le pipeline traite ces nœuds sources comme ayant la même horloge que les nœuds sources de cet élément dans la topologie précédente.</span><span class="sxs-lookup"><span data-stu-id="cdbf5-111">When the pipeline queues up a new topology that contains source nodes that are part of an element that is present in the previous topology, the pipeline treats these source nodes as having the same clock as the source nodes from that element in the previous topology.</span></span>

> [!Note]  
> <span data-ttu-id="cdbf5-112">Le pipeline de média ne corrige pas les horodatages pour les nœuds sources ayant des taux d’horloge différents.</span><span class="sxs-lookup"><span data-stu-id="cdbf5-112">The media pipeline does not correct time stamps for source nodes with different clock rates.</span></span>

 

<span data-ttu-id="cdbf5-113">Une source de média qui peut fournir des topologies doit implémenter l’interface [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) ou l’interface [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) .</span><span class="sxs-lookup"><span data-stu-id="cdbf5-113">A media source that can provide topologies should implement the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface or the [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) interface.</span></span> <span data-ttu-id="cdbf5-114">Une source de média qui fournit des topologies doit définir l’attribut d' **\_ \_ \_ ELEMENTID de séquence TOPONODE MF** sur chaque nœud source qu’elle crée.</span><span class="sxs-lookup"><span data-stu-id="cdbf5-114">A media source that provides topologies should set the **MF\_TOPONODE\_SEQUENCE\_ELEMENTID** attribute on every source node that it creates.</span></span>

<span data-ttu-id="cdbf5-115">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="cdbf5-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdbf5-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cdbf5-116">Requirements</span></span>



| <span data-ttu-id="cdbf5-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cdbf5-117">Requirement</span></span> | <span data-ttu-id="cdbf5-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdbf5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cdbf5-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdbf5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cdbf5-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdbf5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cdbf5-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdbf5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cdbf5-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdbf5-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cdbf5-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="cdbf5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdbf5-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdbf5-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdbf5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdbf5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdbf5-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cdbf5-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cdbf5-127">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="cdbf5-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="cdbf5-128">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="cdbf5-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="cdbf5-129">**IMFMediaSourceTopologyProvider**</span><span class="sxs-lookup"><span data-stu-id="cdbf5-129">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
</dt> <dt>

[<span data-ttu-id="cdbf5-130">**IMFSequencerSource**</span><span class="sxs-lookup"><span data-stu-id="cdbf5-130">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)
</dt> <dt>

[<span data-ttu-id="cdbf5-131">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="cdbf5-131">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="cdbf5-132">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="cdbf5-132">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="cdbf5-133">Source de Sequencer</span><span class="sxs-lookup"><span data-stu-id="cdbf5-133">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




