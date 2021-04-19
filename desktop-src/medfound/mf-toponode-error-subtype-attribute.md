---
description: Contient le sous-type de média pour un nœud de topologie. Cet attribut est défini lorsque le chargement de la topologie échoue car le décodeur approprié est introuvable.
ms.assetid: 89da33c8-97af-4c56-8bdb-2ac588810d77
title: Attribut MF_TOPONODE_ERROR_SUBTYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1233fb62c271a6f4fd84ec8b2c0b34aa6c49b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524078"
---
# <a name="mf_toponode_error_subtype-attribute"></a><span data-ttu-id="58e6c-104">\_Attribut de \_ sous-type d’erreur MF TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="58e6c-104">MF\_TOPONODE\_ERROR\_SUBTYPE attribute</span></span>

<span data-ttu-id="58e6c-105">Contient le sous-type de média pour un nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="58e6c-105">Contains the media subtype for a topology node.</span></span> <span data-ttu-id="58e6c-106">Cet attribut est défini lorsque le chargement de la topologie échoue car le décodeur approprié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="58e6c-106">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span>

## <a name="data-type"></a><span data-ttu-id="58e6c-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="58e6c-107">Data type</span></span>

<span data-ttu-id="58e6c-108">**GUID**</span><span class="sxs-lookup"><span data-stu-id="58e6c-108">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="58e6c-109">Notes</span><span class="sxs-lookup"><span data-stu-id="58e6c-109">Remarks</span></span>

<span data-ttu-id="58e6c-110">Cet attribut s’applique à tous les types de nœuds.</span><span class="sxs-lookup"><span data-stu-id="58e6c-110">This attribute applies to all node types.</span></span>

<span data-ttu-id="58e6c-111">Le chargeur de topologie peut définir l’attribut.</span><span class="sxs-lookup"><span data-stu-id="58e6c-111">The topology loader might set the attribute.</span></span> <span data-ttu-id="58e6c-112">Les applications lisent généralement cet attribut, mais ne la définissent pas.</span><span class="sxs-lookup"><span data-stu-id="58e6c-112">Applications typically read this attribute but do not set it.</span></span>

<span data-ttu-id="58e6c-113">Pour obtenir la liste des valeurs possibles, consultez [GUID type Media](media-type-guids.md).</span><span class="sxs-lookup"><span data-stu-id="58e6c-113">For a list of possible values, see [Media Type GUIDs](media-type-guids.md).</span></span>

<span data-ttu-id="58e6c-114">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="58e6c-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="58e6c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58e6c-115">Requirements</span></span>



| <span data-ttu-id="58e6c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58e6c-116">Requirement</span></span> | <span data-ttu-id="58e6c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="58e6c-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="58e6c-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58e6c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="58e6c-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58e6c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="58e6c-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58e6c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="58e6c-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58e6c-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="58e6c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="58e6c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="58e6c-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="58e6c-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58e6c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58e6c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58e6c-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="58e6c-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="58e6c-126">**IMFAttributes :: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="58e6c-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="58e6c-127">**IMFAttributes :: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="58e6c-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="58e6c-128">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="58e6c-128">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="58e6c-129">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="58e6c-129">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




