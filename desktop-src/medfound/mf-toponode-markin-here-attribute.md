---
description: Spécifie si le pipeline applique la marque dans ce nœud.
ms.assetid: 406145e8-e00e-460d-b282-85face457605
title: Attribut MF_TOPONODE_MARKIN_HERE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa355cc070a7371ff2e294b3ca3ad558a4749b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545802"
---
# <a name="mf_toponode_markin_here-attribute"></a><span data-ttu-id="56434-103">\_ \_ Attribut Mark TOPONODE MF \_ ici</span><span class="sxs-lookup"><span data-stu-id="56434-103">MF\_TOPONODE\_MARKIN\_HERE attribute</span></span>

<span data-ttu-id="56434-104">Spécifie si le pipeline applique la marque dans ce nœud.</span><span class="sxs-lookup"><span data-stu-id="56434-104">Specifies whether the pipeline applies mark-in at this node.</span></span> <span data-ttu-id="56434-105">Mark-in est l’endroit où commence une présentation.</span><span class="sxs-lookup"><span data-stu-id="56434-105">Mark-in is the point where a presentation starts.</span></span> <span data-ttu-id="56434-106">Si les composants de pipeline génèrent des données avant le point de marque, les données ne sont pas rendues.</span><span class="sxs-lookup"><span data-stu-id="56434-106">If pipeline components generate data before the mark-in point, the data is not rendered.</span></span>

## <a name="data-type"></a><span data-ttu-id="56434-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="56434-107">Data type</span></span>

<span data-ttu-id="56434-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="56434-108">**UINT32**</span></span>

<span data-ttu-id="56434-109">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="56434-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="56434-110">Notes</span><span class="sxs-lookup"><span data-stu-id="56434-110">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="56434-111">La plupart des applications n’ont pas besoin d’utiliser cet attribut.</span><span class="sxs-lookup"><span data-stu-id="56434-111">Most applications do not need to use this attribute.</span></span> <span data-ttu-id="56434-112">La [session multimédia](media-session.md) définit automatiquement cet attribut, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="56434-112">The [Media Session](media-session.md) automatically sets this attribute if needed.</span></span>

 

<span data-ttu-id="56434-113">Cet attribut s’applique à tous les types de nœuds.</span><span class="sxs-lookup"><span data-stu-id="56434-113">This attribute applies to all node types.</span></span> <span data-ttu-id="56434-114">Si l’attribut a la **valeur true**, le pipeline Media Foundation supprime les exemples de sortie de ce nœud afin qu’il corresponde à l’heure de début de la présentation.</span><span class="sxs-lookup"><span data-stu-id="56434-114">If the attribute is **TRUE**, the Media Foundation pipeline trims the output samples from this node to match the start time for the presentation.</span></span> <span data-ttu-id="56434-115">Le chargeur de topologie définit cet attribut lorsqu’il résout une topologie.</span><span class="sxs-lookup"><span data-stu-id="56434-115">The topology loader sets this attribute when it resolves a topology.</span></span>

<span data-ttu-id="56434-116">Il est recommandé que cet attribut soit défini sur **true** pour chaque branche de la topologie.</span><span class="sxs-lookup"><span data-stu-id="56434-116">It is recommended that exactly one node in every branch of the topology should have this attribute set to **TRUE**.</span></span> <span data-ttu-id="56434-117">Une branche de topologie est définie en tant que chemin d’accès d’un nœud source à un nœud de sortie.</span><span class="sxs-lookup"><span data-stu-id="56434-117">A topology branch is defined as the path from a source node to an output node.</span></span> <span data-ttu-id="56434-118">Au sein d’une branche, les attributs [MF \_ TOPONODE \_ MARKOUT \_ ici](mf-toponode-markout-here-attribute.md) et MF \_ TOPONODE \_ Mark \_ here doivent être définis sur le même nœud dans la branche.</span><span class="sxs-lookup"><span data-stu-id="56434-118">Within a branch, the [MF\_TOPONODE\_MARKOUT\_HERE](mf-toponode-markout-here-attribute.md) and MF\_TOPONODE\_MARKIN\_HERE attributes must be set on the same node in the branch.</span></span> <span data-ttu-id="56434-119">Ils ne peuvent pas être définis sur des nœuds différents dans la même branche.</span><span class="sxs-lookup"><span data-stu-id="56434-119">They cannot be set on different nodes within the same branch.</span></span>

<span data-ttu-id="56434-120">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="56434-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="56434-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56434-121">Requirements</span></span>



| <span data-ttu-id="56434-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56434-122">Requirement</span></span> | <span data-ttu-id="56434-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="56434-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="56434-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56434-124">Minimum supported client</span></span><br/> | <span data-ttu-id="56434-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56434-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="56434-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56434-126">Minimum supported server</span></span><br/> | <span data-ttu-id="56434-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56434-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="56434-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="56434-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="56434-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="56434-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56434-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56434-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56434-131">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="56434-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="56434-132">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="56434-132">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="56434-133">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="56434-133">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="56434-134">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="56434-134">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="56434-135">**\_MARKOUT TOPONODE \_ MF \_ ici**</span><span class="sxs-lookup"><span data-stu-id="56434-135">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="56434-136">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="56434-136">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




