---
description: Contient le type de média principal pour un nœud de topologie. Cet attribut est défini lorsque le chargement de la topologie échoue car le décodeur approprié est introuvable.
ms.assetid: eb837fe6-12c9-479c-a0be-63b24093e6fd
title: Attribut MF_TOPONODE_ERROR_MAJORTYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68ace0cd3bec4f32536e7d0d8d29bcea60d997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544240"
---
# <a name="mf_toponode_error_majortype-attribute"></a><span data-ttu-id="e0d53-104">\_Attribut MAJORTYPE de l’erreur TOPONODE MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="e0d53-104">MF\_TOPONODE\_ERROR\_MAJORTYPE attribute</span></span>

<span data-ttu-id="e0d53-105">Contient le type de média principal pour un nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="e0d53-105">Contains the major media type for a topology node.</span></span> <span data-ttu-id="e0d53-106">Cet attribut est défini lorsque le chargement de la topologie échoue car le décodeur approprié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="e0d53-106">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span>

## <a name="data-type"></a><span data-ttu-id="e0d53-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="e0d53-107">Data type</span></span>

<span data-ttu-id="e0d53-108">**GUID**</span><span class="sxs-lookup"><span data-stu-id="e0d53-108">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="e0d53-109">Notes</span><span class="sxs-lookup"><span data-stu-id="e0d53-109">Remarks</span></span>

<span data-ttu-id="e0d53-110">Cet attribut s’applique à tous les types de nœuds.</span><span class="sxs-lookup"><span data-stu-id="e0d53-110">This attribute applies to all node types.</span></span>

<span data-ttu-id="e0d53-111">Le chargeur de topologie peut définir l’attribut.</span><span class="sxs-lookup"><span data-stu-id="e0d53-111">The topology loader might set the attribute.</span></span> <span data-ttu-id="e0d53-112">Les applications lisent généralement cet attribut, mais ne la définissent pas.</span><span class="sxs-lookup"><span data-stu-id="e0d53-112">Applications typically read this attribute but do not set it.</span></span>

<span data-ttu-id="e0d53-113">Pour obtenir la liste des valeurs possibles, consultez [types de média majeurs](media-type-guids.md).</span><span class="sxs-lookup"><span data-stu-id="e0d53-113">For a list of possible values, see [Major Media Types](media-type-guids.md).</span></span>

<span data-ttu-id="e0d53-114">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e0d53-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0d53-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0d53-115">Requirements</span></span>



| <span data-ttu-id="e0d53-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0d53-116">Requirement</span></span> | <span data-ttu-id="e0d53-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0d53-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e0d53-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0d53-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e0d53-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0d53-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e0d53-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0d53-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e0d53-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0d53-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e0d53-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e0d53-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0d53-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0d53-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0d53-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0d53-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0d53-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e0d53-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e0d53-126">**IMFAttributes :: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="e0d53-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="e0d53-127">**IMFAttributes :: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="e0d53-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="e0d53-128">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="e0d53-128">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="e0d53-129">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="e0d53-129">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




