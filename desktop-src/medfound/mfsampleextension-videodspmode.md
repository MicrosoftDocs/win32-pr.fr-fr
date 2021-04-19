---
description: Indique si la stabilisation vidéo a été appliquée à une image vidéo.
ms.assetid: 13F877A3-7600-400F-9071-FE1B83027355
title: Attribut MFSampleExtension_VideoDSPMode (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 309d4b5b68455e78ba63074b9d8ec5e4cbde4fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534445"
---
# <a name="mfsampleextension_videodspmode-attribute"></a><span data-ttu-id="95694-103">\_Attribut MFSampleExtension VideoDSPMode</span><span class="sxs-lookup"><span data-stu-id="95694-103">MFSampleExtension\_VideoDSPMode attribute</span></span>

<span data-ttu-id="95694-104">Indique si la stabilisation vidéo a été appliquée à une image vidéo.</span><span class="sxs-lookup"><span data-stu-id="95694-104">Indicates whether video stabilization was applied to a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="95694-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="95694-105">Data type</span></span>

<span data-ttu-id="95694-106">**MFVideoDSPMode** stocké en tant que **UInt32**</span><span class="sxs-lookup"><span data-stu-id="95694-106">**MFVideoDSPMode** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="95694-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="95694-107">Get/set</span></span>

<span data-ttu-id="95694-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="95694-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="95694-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="95694-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="95694-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="95694-110">Applies to</span></span>

[<span data-ttu-id="95694-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="95694-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="95694-112">Notes</span><span class="sxs-lookup"><span data-stu-id="95694-112">Remarks</span></span>

<span data-ttu-id="95694-113">La [**stabilisation vidéo MFT**](video-stabilization-mft.md) définit cet attribut sur les exemples de sortie qu’il produit.</span><span class="sxs-lookup"><span data-stu-id="95694-113">The [**Video Stabilization MFT**](video-stabilization-mft.md) sets this attribute on the output samples that it produces.</span></span> <span data-ttu-id="95694-114">La valeur de l’attribut est une valeur d’énumération [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) .</span><span class="sxs-lookup"><span data-stu-id="95694-114">The value of the attribute is an [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) enumeration value.</span></span> <span data-ttu-id="95694-115">Si la valeur est **MFVideoDSPMode \_ stabilisation**, cela signifie que la table MFT a appliqué la stabilisation de l’image au frame.</span><span class="sxs-lookup"><span data-stu-id="95694-115">If the value is **MFVideoDSPMode\_Stabilization**, it means that the MFT applied image stabilization to the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="95694-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95694-116">Requirements</span></span>



| <span data-ttu-id="95694-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95694-117">Requirement</span></span> | <span data-ttu-id="95694-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="95694-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95694-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95694-119">Minimum supported client</span></span><br/> | <span data-ttu-id="95694-120">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95694-120">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="95694-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95694-121">Minimum supported server</span></span><br/> | <span data-ttu-id="95694-122">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95694-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="95694-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="95694-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="95694-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="95694-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95694-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95694-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95694-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="95694-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="95694-127">Exemples d’attributs</span><span class="sxs-lookup"><span data-stu-id="95694-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="95694-128">Exemples de supports</span><span class="sxs-lookup"><span data-stu-id="95694-128">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="95694-129">**Stabilisation vidéo MFT**</span><span class="sxs-lookup"><span data-stu-id="95694-129">**Video Stabilization MFT**</span></span>](video-stabilization-mft.md)
</dt> </dl>

 

 




