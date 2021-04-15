---
description: Contient un pointeur vers la source du média associée à un nœud de topologie.
ms.assetid: 73b84ab6-bdc2-4b22-9ce4-b79b954476e5
title: Attribut MF_TOPONODE_SOURCE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57904e9797e0f669b2cb782750e4ae9199059d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527423"
---
# <a name="mf_toponode_source-attribute"></a><span data-ttu-id="31c06-103">\_ \_ Attribut source MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="31c06-103">MF\_TOPONODE\_SOURCE attribute</span></span>

<span data-ttu-id="31c06-104">Contient un pointeur vers la source du média associée à un nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="31c06-104">Contains a pointer to the media source associated with a topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="31c06-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="31c06-105">Data type</span></span>

<span data-ttu-id="31c06-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="31c06-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="31c06-107">Notes</span><span class="sxs-lookup"><span data-stu-id="31c06-107">Remarks</span></span>

<span data-ttu-id="31c06-108">Cet attribut s’applique aux nœuds sources (_ \* MF \_ Topology \_ SOURCESTREAM \_ node \* \*).</span><span class="sxs-lookup"><span data-stu-id="31c06-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="31c06-109">La valeur de l’attribut est un pointeur vers l’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) de la source du média.</span><span class="sxs-lookup"><span data-stu-id="31c06-109">The value of the attribute is a pointer to the media source's [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="31c06-110">Cet attribut est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="31c06-110">This attribute is required.</span></span>

<span data-ttu-id="31c06-111">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="31c06-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="31c06-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31c06-112">Requirements</span></span>



| <span data-ttu-id="31c06-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31c06-113">Requirement</span></span> | <span data-ttu-id="31c06-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="31c06-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="31c06-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31c06-115">Minimum supported client</span></span><br/> | <span data-ttu-id="31c06-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31c06-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="31c06-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31c06-117">Minimum supported server</span></span><br/> | <span data-ttu-id="31c06-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31c06-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="31c06-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="31c06-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="31c06-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="31c06-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31c06-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31c06-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31c06-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="31c06-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="31c06-123">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="31c06-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="31c06-124">**IMFAttributes :: Setunknown,**</span><span class="sxs-lookup"><span data-stu-id="31c06-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="31c06-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="31c06-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="31c06-126">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="31c06-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




