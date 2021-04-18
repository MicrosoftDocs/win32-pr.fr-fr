---
description: Spécifie si le pipeline applique le marquage sur ce nœud. Le marquage est l’endroit où se termine une présentation. Si les composants de pipeline génèrent des données au-delà du point de marquage, les données ne sont pas rendues.
ms.assetid: adf2361a-90c7-4650-a486-5c450a41ab54
title: Attribut MF_TOPONODE_MARKOUT_HERE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c5dc21f39f45aa04860f3374bead54d260f0821
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519770"
---
# <a name="mf_toponode_markout_here-attribute"></a><span data-ttu-id="1442e-105">\_TOPONODE MF \_ MARKOUT \_ ici, attribut</span><span class="sxs-lookup"><span data-stu-id="1442e-105">MF\_TOPONODE\_MARKOUT\_HERE attribute</span></span>

<span data-ttu-id="1442e-106">Spécifie si le pipeline applique le marquage sur ce nœud.</span><span class="sxs-lookup"><span data-stu-id="1442e-106">Specifies whether the pipeline applies mark-out at this node.</span></span> <span data-ttu-id="1442e-107">Le marquage est l’endroit où se termine une présentation.</span><span class="sxs-lookup"><span data-stu-id="1442e-107">Mark-out is the point where a presentation ends.</span></span> <span data-ttu-id="1442e-108">Si les composants de pipeline génèrent des données au-delà du point de marquage, les données ne sont pas rendues.</span><span class="sxs-lookup"><span data-stu-id="1442e-108">If pipeline components generate data past the mark-out point, the data is not rendered.</span></span>

## <a name="data-type"></a><span data-ttu-id="1442e-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="1442e-109">Data type</span></span>

<span data-ttu-id="1442e-110">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1442e-110">**UINT32**</span></span>

<span data-ttu-id="1442e-111">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="1442e-111">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1442e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="1442e-112">Remarks</span></span>

<span data-ttu-id="1442e-113">Cet attribut s’applique à tous les types de nœuds.</span><span class="sxs-lookup"><span data-stu-id="1442e-113">This attribute applies to all node types.</span></span>

<span data-ttu-id="1442e-114">Si cet attribut a la **valeur true**, le pipeline Media Foundation supprime les exemples de sortie de ce nœud pour qu’ils correspondent à l’heure d’arrêt de la présentation.</span><span class="sxs-lookup"><span data-stu-id="1442e-114">If this attribute is **TRUE**, the Media Foundation pipeline trims the output samples from this node to match the stop time for the presentation.</span></span> <span data-ttu-id="1442e-115">Le chargeur de topologie définit cet attribut lorsqu’il résout une topologie.</span><span class="sxs-lookup"><span data-stu-id="1442e-115">The topology loader sets this attribute when it resolves a topology.</span></span> <span data-ttu-id="1442e-116">La plupart des applications n’ont pas besoin de définir ou de récupérer cet attribut.</span><span class="sxs-lookup"><span data-stu-id="1442e-116">Most applications do not need to set or retrieve this attribute.</span></span>

<span data-ttu-id="1442e-117">Il est recommandé que cet attribut soit défini sur **true** pour chaque branche de la topologie.</span><span class="sxs-lookup"><span data-stu-id="1442e-117">It is recommended that exactly one node in every branch of the topology should have this attribute set to **TRUE**.</span></span> <span data-ttu-id="1442e-118">Une branche de topologie est définie en tant que chemin d’accès d’un nœud source à un nœud de sortie.</span><span class="sxs-lookup"><span data-stu-id="1442e-118">A topology branch is defined as the path from a source node to an output node.</span></span> <span data-ttu-id="1442e-119">Au sein d’une branche, \_ les \_ attributs MF TOPONODE MARKOUT \_ ici et [MF \_ TOPONODE \_ Mark \_ here](mf-toponode-markin-here-attribute.md) doivent être définis sur le même nœud dans la branche.</span><span class="sxs-lookup"><span data-stu-id="1442e-119">Within a branch, the MF\_TOPONODE\_MARKOUT\_HERE and [MF\_TOPONODE\_MARKIN\_HERE](mf-toponode-markin-here-attribute.md) attributes must be set on the same node in the branch.</span></span> <span data-ttu-id="1442e-120">Ils ne peuvent pas être définis sur des nœuds différents dans la même branche.</span><span class="sxs-lookup"><span data-stu-id="1442e-120">They cannot be set on different nodes within the same branch.</span></span>

<span data-ttu-id="1442e-121">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1442e-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1442e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1442e-122">Requirements</span></span>



| <span data-ttu-id="1442e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1442e-123">Requirement</span></span> | <span data-ttu-id="1442e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="1442e-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1442e-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1442e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1442e-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1442e-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1442e-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1442e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1442e-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1442e-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1442e-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="1442e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1442e-130"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1442e-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1442e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1442e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1442e-132">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1442e-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1442e-133">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1442e-133">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="1442e-134">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1442e-134">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="1442e-135">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="1442e-135">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="1442e-136">**\_Mark MF TOPONODE \_ \_ ici**</span><span class="sxs-lookup"><span data-stu-id="1442e-136">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="1442e-137">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="1442e-137">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




