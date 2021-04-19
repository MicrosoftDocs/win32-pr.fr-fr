---
description: Identificateur de flux du récepteur de flux associé à ce nœud de topologie.
ms.assetid: 0b8060ab-1463-45c2-8277-d15122561248
title: Attribut MF_TOPONODE_STREAMID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2377183927cf75c6e0a7436384426dcab94680c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518348"
---
# <a name="mf_toponode_streamid-attribute"></a><span data-ttu-id="a04a1-103">\_ \_ Attribut STREAMID TOPONODE MF</span><span class="sxs-lookup"><span data-stu-id="a04a1-103">MF\_TOPONODE\_STREAMID attribute</span></span>

<span data-ttu-id="a04a1-104">Identificateur de flux du récepteur de flux associé à ce nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="a04a1-104">The stream identifier of the stream sink associated with this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="a04a1-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="a04a1-105">Data type</span></span>

<span data-ttu-id="a04a1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a04a1-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a04a1-107">Notes</span><span class="sxs-lookup"><span data-stu-id="a04a1-107">Remarks</span></span>

<span data-ttu-id="a04a1-108">Cet attribut s’applique aux nœuds de sortie (**\_ nœud de \_ sortie \_ de topologie MF**).</span><span class="sxs-lookup"><span data-stu-id="a04a1-108">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="a04a1-109">Lorsque la session multimédia charge la topologie, elle interroge le récepteur de média pour obtenir un récepteur de flux avec l’identificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="a04a1-109">When the Media Session loads the topology, it queries the media sink for a stream sink with the specified identifier.</span></span> <span data-ttu-id="a04a1-110">En cas d’échec, elle tente d’ajouter un nouveau récepteur de flux au récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="a04a1-110">If that fails, it attempts to add a new stream sink to the media sink.</span></span>

<span data-ttu-id="a04a1-111">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a04a1-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a04a1-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a04a1-112">Requirements</span></span>



| <span data-ttu-id="a04a1-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a04a1-113">Requirement</span></span> | <span data-ttu-id="a04a1-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="a04a1-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a04a1-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a04a1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a04a1-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a04a1-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a04a1-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a04a1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a04a1-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a04a1-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a04a1-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="a04a1-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a04a1-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a04a1-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a04a1-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a04a1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a04a1-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a04a1-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a04a1-123">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a04a1-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a04a1-124">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a04a1-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a04a1-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="a04a1-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="a04a1-126">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="a04a1-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




