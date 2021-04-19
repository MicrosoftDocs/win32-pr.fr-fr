---
description: Spécifie si le récepteur multimédia associé à ce nœud de topologie est sans débit.
ms.assetid: 81ef7005-a9ab-4f26-bc39-68b27c4f92aa
title: Attribut MF_TOPONODE_RATELESS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5c5ded4d8d09e8d45f766b03737954329c9202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524077"
---
# <a name="mf_toponode_rateless-attribute"></a><span data-ttu-id="f2f24-103">\_Attribut sans \_ débit MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="f2f24-103">MF\_TOPONODE\_RATELESS attribute</span></span>

<span data-ttu-id="f2f24-104">Spécifie si le récepteur multimédia associé à ce nœud de topologie est sans débit.</span><span class="sxs-lookup"><span data-stu-id="f2f24-104">Specifies whether the media sink associated with this topology node is rateless.</span></span>

## <a name="data-type"></a><span data-ttu-id="f2f24-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="f2f24-105">Data type</span></span>

<span data-ttu-id="f2f24-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f2f24-106">**UINT32**</span></span>

<span data-ttu-id="f2f24-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="f2f24-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2f24-108">Notes</span><span class="sxs-lookup"><span data-stu-id="f2f24-108">Remarks</span></span>

<span data-ttu-id="f2f24-109">Cet attribut s’applique aux nœuds de sortie (**\_ nœud de \_ sortie \_ de topologie MF**).</span><span class="sxs-lookup"><span data-stu-id="f2f24-109">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="f2f24-110">Si la valeur de cet attribut est différente de zéro, la session multimédia traite le récepteur multimédia comme un récepteur sans débit, que le récepteur multimédia renvoie ou non la caractéristique de **\_ débit MEDIASINK** .</span><span class="sxs-lookup"><span data-stu-id="f2f24-110">If the value of this attribute is nonzero, the Media Session treats the media sink as a rateless sink, regardless of whether the media sink returns the **MEDIASINK\_RATELESS** characteristic.</span></span> <span data-ttu-id="f2f24-111">Si cet attribut n’est pas défini, le récepteur multimédia est supposé ne pas être sans débit.</span><span class="sxs-lookup"><span data-stu-id="f2f24-111">If this attribute is not set, the media sink is assumed not to be rateless.</span></span>

<span data-ttu-id="f2f24-112">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f2f24-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2f24-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2f24-113">Requirements</span></span>



| <span data-ttu-id="f2f24-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2f24-114">Requirement</span></span> | <span data-ttu-id="f2f24-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2f24-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f2f24-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2f24-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f2f24-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2f24-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f2f24-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2f24-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f2f24-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2f24-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f2f24-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2f24-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2f24-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2f24-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2f24-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2f24-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2f24-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f2f24-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f2f24-124">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f2f24-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f2f24-125">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f2f24-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f2f24-126">**IMFMediaSink::GetCharacteristics**</span><span class="sxs-lookup"><span data-stu-id="f2f24-126">**IMFMediaSink::GetCharacteristics**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics)
</dt> <dt>

[<span data-ttu-id="f2f24-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="f2f24-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="f2f24-128">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="f2f24-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




