---
description: Spécifie si un objet sous-jacent de nœuds de topologie est un décodeur.
ms.assetid: b6d576dc-b12f-49bf-b938-db2c629df400
title: Attribut MF_TOPONODE_DECODER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab16d14a91608fb6b21c901e3fb055ce5e4dfbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210363"
---
# <a name="mf_toponode_decoder-attribute"></a><span data-ttu-id="2f450-103">\_Attribut de \_ décodeur MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="2f450-103">MF\_TOPONODE\_DECODER attribute</span></span>

<span data-ttu-id="2f450-104">Spécifie si l’objet sous-jacent d’un nœud de topologie est un décodeur.</span><span class="sxs-lookup"><span data-stu-id="2f450-104">Specifies whether a topology node's underlying object is a decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="2f450-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="2f450-105">Data type</span></span>

<span data-ttu-id="2f450-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2f450-106">**UINT32**</span></span>

<span data-ttu-id="2f450-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="2f450-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f450-108">Notes</span><span class="sxs-lookup"><span data-stu-id="2f450-108">Remarks</span></span>

<span data-ttu-id="2f450-109">Cet attribut s’applique à tous les types de nœuds.</span><span class="sxs-lookup"><span data-stu-id="2f450-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="2f450-110">Si la valeur de cet attribut est différente de zéro, l’objet sous-jacent du nœud est un décodeur.</span><span class="sxs-lookup"><span data-stu-id="2f450-110">If the value of this attribute is nonzero, the node's underlying object is a decoder.</span></span>

<span data-ttu-id="2f450-111">Le chargeur de topologie définit cet attribut lorsqu’il crée un nœud de décodeur.</span><span class="sxs-lookup"><span data-stu-id="2f450-111">The topology loader sets this attribute when it creates a decoder node.</span></span> <span data-ttu-id="2f450-112">Une application doit définir cet attribut si l’application ajoute manuellement un décodeur à la topologie.</span><span class="sxs-lookup"><span data-stu-id="2f450-112">An application should set this attribute if the application manually adds a decoder to the topology.</span></span>

<span data-ttu-id="2f450-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="2f450-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f450-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f450-114">Requirements</span></span>



| <span data-ttu-id="2f450-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f450-115">Requirement</span></span> | <span data-ttu-id="2f450-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f450-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2f450-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f450-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2f450-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f450-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2f450-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f450-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2f450-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f450-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2f450-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f450-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f450-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f450-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f450-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f450-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f450-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2f450-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2f450-125">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="2f450-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="2f450-126">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="2f450-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="2f450-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="2f450-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="2f450-128">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="2f450-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




