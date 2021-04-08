---
description: Spécifie si les types de média peuvent être modifiés sur ce nœud de topologie.
ms.assetid: 8805ed63-1408-40bc-bb82-f3c51576dfa4
title: Attribut MF_TOPONODE_LOCKED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70776b1a5ba9c5c35cd2a2d97618de4b3a65abb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753165"
---
# <a name="mf_toponode_locked-attribute"></a><span data-ttu-id="53b61-103">\_Attribut TOPONODE \_ verrouillé MF</span><span class="sxs-lookup"><span data-stu-id="53b61-103">MF\_TOPONODE\_LOCKED attribute</span></span>

<span data-ttu-id="53b61-104">Spécifie si les types de média peuvent être modifiés sur ce nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="53b61-104">Specifies whether the media types can be changed on this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="53b61-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="53b61-105">Data type</span></span>

<span data-ttu-id="53b61-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="53b61-106">**UINT32**</span></span>

<span data-ttu-id="53b61-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="53b61-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53b61-108">Notes</span><span class="sxs-lookup"><span data-stu-id="53b61-108">Remarks</span></span>

<span data-ttu-id="53b61-109">Cet attribut s’applique à tous les types de nœuds.</span><span class="sxs-lookup"><span data-stu-id="53b61-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="53b61-110">Si la valeur de cet attribut est différente de zéro, le chargeur de topologie ne modifiera pas les types de médias.</span><span class="sxs-lookup"><span data-stu-id="53b61-110">If value of this attribute is nonzero, the topology loader will not change the media types.</span></span> <span data-ttu-id="53b61-111">Cet attribut est défini sur **true** lorsque le nœud est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="53b61-111">This attribute is set to **TRUE** when the node is in use.</span></span>

<span data-ttu-id="53b61-112">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="53b61-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="53b61-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53b61-113">Requirements</span></span>



| <span data-ttu-id="53b61-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53b61-114">Requirement</span></span> | <span data-ttu-id="53b61-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="53b61-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="53b61-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53b61-116">Minimum supported client</span></span><br/> | <span data-ttu-id="53b61-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53b61-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="53b61-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53b61-118">Minimum supported server</span></span><br/> | <span data-ttu-id="53b61-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53b61-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="53b61-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="53b61-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="53b61-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="53b61-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53b61-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53b61-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53b61-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="53b61-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="53b61-124">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="53b61-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="53b61-125">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="53b61-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="53b61-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="53b61-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="53b61-127">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="53b61-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




