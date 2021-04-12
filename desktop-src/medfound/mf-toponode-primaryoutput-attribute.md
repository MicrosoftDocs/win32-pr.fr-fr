---
description: Indique quelle sortie est la sortie principale sur un nœud tee.
ms.assetid: f7d98837-75da-48cc-8307-091be2d95392
title: Attribut MF_TOPONODE_PRIMARYOUTPUT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4130f1df4789ad910ae013eab43168983b47c316
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318642"
---
# <a name="mf_toponode_primaryoutput-attribute"></a><span data-ttu-id="dee0f-103">\_ \_ Attribut PRIMARYOUTPUT, car TOPONODE MF</span><span class="sxs-lookup"><span data-stu-id="dee0f-103">MF\_TOPONODE\_PRIMARYOUTPUT attribute</span></span>

<span data-ttu-id="dee0f-104">Indique quelle sortie est la sortie principale sur un nœud tee.</span><span class="sxs-lookup"><span data-stu-id="dee0f-104">Indicates which output is the primary output on a tee node.</span></span>

## <a name="data-type"></a><span data-ttu-id="dee0f-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="dee0f-105">Data type</span></span>

<span data-ttu-id="dee0f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dee0f-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="dee0f-107">Notes</span><span class="sxs-lookup"><span data-stu-id="dee0f-107">Remarks</span></span>

<span data-ttu-id="dee0f-108">Cet attribut s’applique aux nœuds tee (**\_ \_ \_ nœud tee de topologie MF**).</span><span class="sxs-lookup"><span data-stu-id="dee0f-108">This attribute applies to tee nodes (**MF\_TOPOLOGY\_TEE\_NODE**).</span></span>

<span data-ttu-id="dee0f-109">La valeur de cet attribut est l’index de base zéro d’une connexion de sortie sur ce nœud tee.</span><span class="sxs-lookup"><span data-stu-id="dee0f-109">The value of this attribute is the zero-based index of an output connection on this tee node.</span></span> <span data-ttu-id="dee0f-110">Cette valeur indique la sortie qui est le flux de sortie principal.</span><span class="sxs-lookup"><span data-stu-id="dee0f-110">This value indicates which output is the primary output stream.</span></span> <span data-ttu-id="dee0f-111">Le pipeline attend une demande de la sortie principale avant de traiter les demandes des autres sorties.</span><span class="sxs-lookup"><span data-stu-id="dee0f-111">The pipeline waits for a request from the primary output before processing requests from the other outputs.</span></span>

<span data-ttu-id="dee0f-112">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="dee0f-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="dee0f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dee0f-113">Requirements</span></span>



| <span data-ttu-id="dee0f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dee0f-114">Requirement</span></span> | <span data-ttu-id="dee0f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="dee0f-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dee0f-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dee0f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dee0f-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dee0f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dee0f-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dee0f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dee0f-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dee0f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dee0f-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="dee0f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dee0f-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dee0f-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dee0f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dee0f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dee0f-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dee0f-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dee0f-124">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="dee0f-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="dee0f-125">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="dee0f-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="dee0f-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="dee0f-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="dee0f-127">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="dee0f-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




