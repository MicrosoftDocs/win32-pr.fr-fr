---
description: Contient le code d’erreur de l’échec de connexion le plus récent pour ce nœud topologie.
ms.assetid: fae90e06-0ae0-43a1-aaf2-7a2d1dabc79b
title: Attribut MF_TOPONODE_ERRORCODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b4b28c8f630d06f3545ca44c5b064c0bb6dac32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114027"
---
# <a name="mf_toponode_errorcode-attribute"></a><span data-ttu-id="3be14-103">\_Attribut ERRORCODE d’TOPONODE MF \_</span><span class="sxs-lookup"><span data-stu-id="3be14-103">MF\_TOPONODE\_ERRORCODE attribute</span></span>

<span data-ttu-id="3be14-104">Contient le code d’erreur de l’échec de connexion le plus récent pour ce nœud topologie.</span><span class="sxs-lookup"><span data-stu-id="3be14-104">Contains the error code from the most recent connection failure for this toplogy node.</span></span>

## <a name="data-type"></a><span data-ttu-id="3be14-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="3be14-105">Data type</span></span>

<span data-ttu-id="3be14-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3be14-106">**UINT32**</span></span>

<span data-ttu-id="3be14-107">Ttreat en tant que valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3be14-107">Ttreat as an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3be14-108">Notes</span><span class="sxs-lookup"><span data-stu-id="3be14-108">Remarks</span></span>

<span data-ttu-id="3be14-109">Cet attribut s’applique à tous les types de nœuds.</span><span class="sxs-lookup"><span data-stu-id="3be14-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="3be14-110">La valeur de cet attribut est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3be14-110">The value of this attribute is an **HRESULT** value.</span></span>

<span data-ttu-id="3be14-111">La session multimédia ou le chargeur topologique peut définir l’attribut.</span><span class="sxs-lookup"><span data-stu-id="3be14-111">The Media Session or the topology loader might set the attribute.</span></span> <span data-ttu-id="3be14-112">Les applications lisent généralement cet attribut, mais ne la définissent pas.</span><span class="sxs-lookup"><span data-stu-id="3be14-112">Applications typically read this attribute but do not set it.</span></span>

<span data-ttu-id="3be14-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3be14-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3be14-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3be14-114">Requirements</span></span>



| <span data-ttu-id="3be14-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3be14-115">Requirement</span></span> | <span data-ttu-id="3be14-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3be14-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3be14-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3be14-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3be14-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3be14-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3be14-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3be14-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3be14-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3be14-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3be14-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3be14-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3be14-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3be14-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3be14-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3be14-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3be14-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3be14-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3be14-125">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3be14-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="3be14-126">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3be14-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="3be14-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="3be14-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="3be14-128">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="3be14-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




