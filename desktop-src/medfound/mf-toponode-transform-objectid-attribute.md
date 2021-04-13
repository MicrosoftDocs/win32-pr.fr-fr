---
description: Identificateur de classe (CLSID) de la Media Foundation transformation (MFT) associée à ce nœud de topologie.
ms.assetid: 6aa6e649-d23d-4d8d-be80-2b8814b07a57
title: Attribut MF_TOPONODE_TRANSFORM_OBJECTID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea96e09a75374bfe048b531492fc913f764d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527418"
---
# <a name="mf_toponode_transform_objectid-attribute"></a><span data-ttu-id="d689e-103">\_ \_ Attribut ObjectID de transformation TOPONODE MF \_</span><span class="sxs-lookup"><span data-stu-id="d689e-103">MF\_TOPONODE\_TRANSFORM\_OBJECTID attribute</span></span>

<span data-ttu-id="d689e-104">Identificateur de classe (CLSID) de la Media Foundation transformation (MFT) associée à ce nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="d689e-104">The class identifier (CLSID) of the Media Foundation transform (MFT) associated with this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="d689e-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="d689e-105">Data type</span></span>

<span data-ttu-id="d689e-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="d689e-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="d689e-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d689e-107">Remarks</span></span>

<span data-ttu-id="d689e-108">Cet attribut s’applique aux nœuds de transformation (**\_ nœud de \_ transformation \_ de topologie MF**).</span><span class="sxs-lookup"><span data-stu-id="d689e-108">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="d689e-109">Les applications peuvent utiliser cet attribut pour initialiser une de nœud.</span><span class="sxs-lookup"><span data-stu-id="d689e-109">Applications can use this attribute to initialize a transfrom node.</span></span> <span data-ttu-id="d689e-110">Si vous définissez cet attribut, il n’est pas nécessaire d’appeler [**IMFTopologyNode :: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) avec un pointeur vers un objet MFT ou activation.</span><span class="sxs-lookup"><span data-stu-id="d689e-110">If you set this attribute, you do not have to call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) with a pointer to an MFT or activation object.</span></span> <span data-ttu-id="d689e-111">À l’inverse, si vous appelez **setObject**, vous n’avez pas besoin de définir cet attribut.</span><span class="sxs-lookup"><span data-stu-id="d689e-111">Conversely, if you call **SetObject**, you do not need to set this attribute.</span></span> <span data-ttu-id="d689e-112">Pour plus d’informations, consultez [création de topologies](creating-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="d689e-112">For more information, see [Creating Topologies](creating-topologies.md).</span></span>

<span data-ttu-id="d689e-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d689e-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d689e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d689e-114">Requirements</span></span>



| <span data-ttu-id="d689e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d689e-115">Requirement</span></span> | <span data-ttu-id="d689e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d689e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d689e-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d689e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d689e-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d689e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d689e-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d689e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d689e-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d689e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d689e-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="d689e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d689e-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d689e-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d689e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d689e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d689e-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d689e-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d689e-125">**IMFAttributes :: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="d689e-125">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="d689e-126">**IMFAttributes :: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="d689e-126">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="d689e-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="d689e-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="d689e-128">Attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d689e-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d689e-129">Création de topologies</span><span class="sxs-lookup"><span data-stu-id="d689e-129">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="d689e-130">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="d689e-130">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




