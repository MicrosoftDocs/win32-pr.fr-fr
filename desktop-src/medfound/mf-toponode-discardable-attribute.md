---
description: Spécifie si le pipeline peut supprimer des exemples d’un nœud de topologie.
ms.assetid: 8be20446-4876-4d6f-b0db-2eb1ffaef9aa
title: Attribut MF_TOPONODE_DISCARDABLE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d76e00a0f70735211cf06aca0adc00238ae5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536862"
---
# <a name="mf_toponode_discardable-attribute"></a><span data-ttu-id="45cce-103">\_ \_ Attribut supprimable MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="45cce-103">MF\_TOPONODE\_DISCARDABLE attribute</span></span>

<span data-ttu-id="45cce-104">Spécifie si le pipeline peut supprimer des exemples d’un nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="45cce-104">Specifies whether the pipeline can drop samples from a topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="45cce-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="45cce-105">Data type</span></span>

<span data-ttu-id="45cce-106">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="45cce-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="45cce-107">Notes</span><span class="sxs-lookup"><span data-stu-id="45cce-107">Remarks</span></span>

<span data-ttu-id="45cce-108">Cet attribut s’applique à tous les types de nœuds.</span><span class="sxs-lookup"><span data-stu-id="45cce-108">This attribute applies to all node types.</span></span> <span data-ttu-id="45cce-109">En général, vous définissez cet attribut sur les nœuds tee pour indiquer que les sorties secondaires ne sont pas essentielles.</span><span class="sxs-lookup"><span data-stu-id="45cce-109">Typically you would set this attribute on tee nodes, to indicate that the secondary outputs are not essential.</span></span>

<span data-ttu-id="45cce-110">La valeur de l’attribut est un tableau d’index vers des flux de sortie sur le nœud.</span><span class="sxs-lookup"><span data-stu-id="45cce-110">The value of the attribute is an array of indexes to output streams on the node.</span></span>

<span data-ttu-id="45cce-111">Si cet attribut est défini, le pipeline peut supprimer des échantillons des flux de sortie spécifiés, si le flux est en retard.</span><span class="sxs-lookup"><span data-stu-id="45cce-111">If this attribute is set, the pipeline might drop samples from the specified output streams, if the stream is falling behind.</span></span>

<span data-ttu-id="45cce-112">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="45cce-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="45cce-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45cce-113">Requirements</span></span>



| <span data-ttu-id="45cce-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45cce-114">Requirement</span></span> | <span data-ttu-id="45cce-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="45cce-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="45cce-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45cce-116">Minimum supported client</span></span><br/> | <span data-ttu-id="45cce-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="45cce-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="45cce-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45cce-118">Minimum supported server</span></span><br/> | <span data-ttu-id="45cce-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="45cce-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="45cce-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="45cce-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="45cce-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="45cce-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45cce-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45cce-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45cce-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="45cce-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="45cce-124">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="45cce-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="45cce-125">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="45cce-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="45cce-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="45cce-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="45cce-127">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="45cce-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




