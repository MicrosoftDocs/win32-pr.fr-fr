---
description: Spécifie le mode d’utilisation d’un encodeur H. 264 UVC.
ms.assetid: 05158F47-CE01-4C99-8FFA-6BBD4F829B59
title: Attribut MF_MT_H264_USAGE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad5239c81e490f5069b8a6f95d4a91c1f150f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113435"
---
# <a name="mf_mt_h264_usage-attribute"></a><span data-ttu-id="6db27-103">\_Attribut d' \_ utilisation de H264 – MF MT \_</span><span class="sxs-lookup"><span data-stu-id="6db27-103">MF\_MT\_H264\_USAGE attribute</span></span>

<span data-ttu-id="6db27-104">Spécifie le mode d’utilisation d’un encodeur H. 264 UVC.</span><span class="sxs-lookup"><span data-stu-id="6db27-104">Specifies the usage mode for a UVC H.264 encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="6db27-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="6db27-105">Data type</span></span>

<span data-ttu-id="6db27-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6db27-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="6db27-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="6db27-107">Get/set</span></span>

<span data-ttu-id="6db27-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="6db27-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="6db27-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="6db27-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="6db27-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="6db27-110">Applies to</span></span>

[<span data-ttu-id="6db27-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6db27-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="6db27-112">Notes</span><span class="sxs-lookup"><span data-stu-id="6db27-112">Remarks</span></span>

<span data-ttu-id="6db27-113">Cet attribut s’applique aux types de média pour les flux H. 264 transmis sur USB.</span><span class="sxs-lookup"><span data-stu-id="6db27-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="6db27-114">La valeur correspond au champ **bUsage** dans le contrôle de sonde/validation UVC 1,2 H. 264.</span><span class="sxs-lookup"><span data-stu-id="6db27-114">The value corresponds to the **bUsage** field in the UVC 1.2 H.264 probe/commit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="6db27-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6db27-115">Requirements</span></span>



| <span data-ttu-id="6db27-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6db27-116">Requirement</span></span> | <span data-ttu-id="6db27-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6db27-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6db27-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6db27-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6db27-119">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6db27-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="6db27-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6db27-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6db27-121">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="6db27-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6db27-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="6db27-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6db27-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6db27-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6db27-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6db27-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6db27-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6db27-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6db27-126">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="6db27-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




