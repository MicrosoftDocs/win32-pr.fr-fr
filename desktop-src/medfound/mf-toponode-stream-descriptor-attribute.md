---
description: Contient un pointeur vers le descripteur de flux pour la source du média.
ms.assetid: 5acafbc1-823f-4b6d-8737-04b3a6a0cf87
title: Attribut MF_TOPONODE_STREAM_DESCRIPTOR (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f074a1c1ffde3671779362724676f884c3b6b0b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518968"
---
# <a name="mf_toponode_stream_descriptor-attribute"></a><span data-ttu-id="1b274-103">\_Attribut de \_ descripteur de flux TOPONODE MF \_</span><span class="sxs-lookup"><span data-stu-id="1b274-103">MF\_TOPONODE\_STREAM\_DESCRIPTOR attribute</span></span>

<span data-ttu-id="1b274-104">Contient un pointeur vers le descripteur de flux pour la source du média.</span><span class="sxs-lookup"><span data-stu-id="1b274-104">Contains a pointer to the stream descriptor for the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="1b274-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="1b274-105">Data type</span></span>

<span data-ttu-id="1b274-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="1b274-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="1b274-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1b274-107">Remarks</span></span>

<span data-ttu-id="1b274-108">Cet attribut s’applique aux nœuds sources (_ \* MF \_ Topology \_ SOURCESTREAM \_ node \* \*).</span><span class="sxs-lookup"><span data-stu-id="1b274-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="1b274-109">La valeur de l’attribut est un pointeur vers l’interface [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) du descripteur de flux.</span><span class="sxs-lookup"><span data-stu-id="1b274-109">The value of the attribute is a pointer to the stream descriptor's [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) interface.</span></span> <span data-ttu-id="1b274-110">Cet attribut est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1b274-110">This attribute is required.</span></span>

<span data-ttu-id="1b274-111">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1b274-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b274-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b274-112">Requirements</span></span>



| <span data-ttu-id="1b274-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b274-113">Requirement</span></span> | <span data-ttu-id="1b274-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b274-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1b274-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b274-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1b274-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b274-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1b274-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b274-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1b274-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b274-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1b274-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b274-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b274-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b274-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b274-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b274-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b274-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1b274-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1b274-123">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="1b274-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="1b274-124">**IMFAttributes :: Setunknown,**</span><span class="sxs-lookup"><span data-stu-id="1b274-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="1b274-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="1b274-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="1b274-126">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="1b274-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




