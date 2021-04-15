---
description: Spécifie si la transformation associée à un nœud de topologie prend en charge l’accélération vidéo DirectX (DXVA).
ms.assetid: b9e393be-0bc0-4cf6-be44-e9e95339c434
title: Attribut MF_TOPONODE_D3DAWARE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d94d06f2834092159fb813ecffd69ec8a157c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485809"
---
# <a name="mf_toponode_d3daware-attribute"></a><span data-ttu-id="5bee2-103">\_ \_ Attribut D3DAWARE TOPONODE MF</span><span class="sxs-lookup"><span data-stu-id="5bee2-103">MF\_TOPONODE\_D3DAWARE attribute</span></span>

<span data-ttu-id="5bee2-104">Spécifie si la transformation associée à un nœud de topologie prend en charge l’accélération vidéo DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="5bee2-104">Specifies whether the transform associated with a topology node supports DirectX Video Acceleration (DXVA).</span></span>

## <a name="data-type"></a><span data-ttu-id="5bee2-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5bee2-105">Data type</span></span>

<span data-ttu-id="5bee2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5bee2-106">**UINT32**</span></span>

<span data-ttu-id="5bee2-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="5bee2-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bee2-108">Notes</span><span class="sxs-lookup"><span data-stu-id="5bee2-108">Remarks</span></span>

<span data-ttu-id="5bee2-109">Cet attribut s’applique aux nœuds de transformation (**\_ nœud de \_ transformation \_ de topologie MF**).</span><span class="sxs-lookup"><span data-stu-id="5bee2-109">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="5bee2-110">En général, les applications n’utilisent pas cet attribut directement.</span><span class="sxs-lookup"><span data-stu-id="5bee2-110">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="5bee2-111">La session multimédia définit cet attribut sur un nœud de transformation si la transformation de Media Foundation sous-jacente a l’attribut [**\_ \_ \_ compatible Direct3D sa**](mf-sa-d3d-aware-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="5bee2-111">The Media Session sets this attribute on a transform node if the underlying Media Foundation transform has the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute.</span></span>

<span data-ttu-id="5bee2-112">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5bee2-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bee2-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5bee2-113">Requirements</span></span>



| <span data-ttu-id="5bee2-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5bee2-114">Requirement</span></span> | <span data-ttu-id="5bee2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5bee2-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5bee2-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bee2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5bee2-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5bee2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5bee2-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bee2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5bee2-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5bee2-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5bee2-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="5bee2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bee2-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bee2-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bee2-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bee2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bee2-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5bee2-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5bee2-124">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5bee2-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5bee2-125">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5bee2-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="5bee2-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="5bee2-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="5bee2-127">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="5bee2-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




