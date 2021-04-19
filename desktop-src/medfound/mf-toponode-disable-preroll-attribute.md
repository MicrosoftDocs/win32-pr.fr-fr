---
description: Spécifie si la session multimédia utilise le préroll sur le récepteur multimédia représenté par ce nœud de topologie.
ms.assetid: 1781f3a0-6baa-4e06-b2eb-9a8f572aa040
title: Attribut MF_TOPONODE_DISABLE_PREROLL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3d031a4ee50262e717731ae517d4441e9be9a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534750"
---
# <a name="mf_toponode_disable_preroll-attribute"></a><span data-ttu-id="032e7-103">TOPONODE MF- \_ \_ désactiver l’attribut de \_ préroll</span><span class="sxs-lookup"><span data-stu-id="032e7-103">MF\_TOPONODE\_DISABLE\_PREROLL attribute</span></span>

<span data-ttu-id="032e7-104">Spécifie si la session multimédia utilise le préroll sur le récepteur multimédia représenté par ce nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="032e7-104">Specifies whether the Media Session uses preroll on the media sink represented by this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="032e7-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="032e7-105">Data type</span></span>

<span data-ttu-id="032e7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="032e7-106">**UINT32**</span></span>

<span data-ttu-id="032e7-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="032e7-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="032e7-108">Notes</span><span class="sxs-lookup"><span data-stu-id="032e7-108">Remarks</span></span>

<span data-ttu-id="032e7-109">Cet attribut s’applique aux nœuds de sortie (**\_ nœud de \_ sortie \_ de topologie MF**).</span><span class="sxs-lookup"><span data-stu-id="032e7-109">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="032e7-110">Si la valeur de cet attribut est **true**, la session multimédia ne préroll aucune donnée au récepteur multimédia, même si le récepteur multimédia expose l’interface [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) .</span><span class="sxs-lookup"><span data-stu-id="032e7-110">If the value of this attribute is **TRUE**, the Media Session does not preroll any data to the media sink, even if the media sink exposes the [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) interface.</span></span> <span data-ttu-id="032e7-111">Si la valeur est **false**, la session multimédia préroll les données si le récepteur multimédia implémente **IMFMediaSinkPreroll**.</span><span class="sxs-lookup"><span data-stu-id="032e7-111">If the value is **FALSE**, the Media Session prerolls data if the media sink implements **IMFMediaSinkPreroll**.</span></span> <span data-ttu-id="032e7-112">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="032e7-112">The default value is **FALSE**.</span></span>

<span data-ttu-id="032e7-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="032e7-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="032e7-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="032e7-114">Requirements</span></span>



| <span data-ttu-id="032e7-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="032e7-115">Requirement</span></span> | <span data-ttu-id="032e7-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="032e7-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="032e7-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="032e7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="032e7-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="032e7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="032e7-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="032e7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="032e7-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="032e7-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="032e7-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="032e7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="032e7-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="032e7-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="032e7-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="032e7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="032e7-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="032e7-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="032e7-125">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="032e7-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="032e7-126">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="032e7-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="032e7-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="032e7-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="032e7-128">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="032e7-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




