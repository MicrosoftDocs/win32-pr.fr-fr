---
description: Spécifie la manière dont une image vidéo 3D est stockée dans un échantillon de média.
ms.assetid: 1B996B22-C76B-47E5-8937-1E5E672E32EC
title: Attribut MFSampleExtension_3DVideo_SampleFormat (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14829c879c151149edc48bf1635b3a5591ddeac5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115011"
---
# <a name="mfsampleextension_3dvideo_sampleformat-attribute"></a><span data-ttu-id="5b3b1-103">MFSampleExtension \_ 3DVideo \_ SampleFormat, attribut</span><span class="sxs-lookup"><span data-stu-id="5b3b1-103">MFSampleExtension\_3DVideo\_SampleFormat attribute</span></span>

<span data-ttu-id="5b3b1-104">Spécifie la manière dont une image vidéo 3D est stockée dans un échantillon de média.</span><span class="sxs-lookup"><span data-stu-id="5b3b1-104">Specifies how a 3D video frame is stored in a media sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="5b3b1-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5b3b1-105">Data type</span></span>

<span data-ttu-id="5b3b1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5b3b1-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="5b3b1-107">Notes</span><span class="sxs-lookup"><span data-stu-id="5b3b1-107">Remarks</span></span>

<span data-ttu-id="5b3b1-108">La valeur de cet attribut est un membre de l’énumération [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) .</span><span class="sxs-lookup"><span data-stu-id="5b3b1-108">The value of this attribute is a member of the [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) enumeration.</span></span>

<span data-ttu-id="5b3b1-109">Un composant qui génère des images vidéo 3D doit affecter la **valeur true** à cet attribut sur chaque échantillon de média qui contient un frame 3D.</span><span class="sxs-lookup"><span data-stu-id="5b3b1-109">A component that generates 3D video frames should set this attribute to **TRUE** on every media sample that contains a 3D frame.</span></span> <span data-ttu-id="5b3b1-110">L’attribut est ignoré si l’attribut [MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md) a la **valeur false** ou n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="5b3b1-110">The attribute is ignored if the [MFSampleExtension\_3DVideo](mfsampleextension-3dvideo.md) attribute is **FALSE** or not set.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b3b1-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b3b1-111">Requirements</span></span>



| <span data-ttu-id="5b3b1-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b3b1-112">Requirement</span></span> | <span data-ttu-id="5b3b1-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b3b1-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5b3b1-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b3b1-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5b3b1-115">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5b3b1-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="5b3b1-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b3b1-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5b3b1-117">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="5b3b1-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5b3b1-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b3b1-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b3b1-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b3b1-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b3b1-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b3b1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b3b1-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5b3b1-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5b3b1-122">MFSampleExtension \_ 3DVideo</span><span class="sxs-lookup"><span data-stu-id="5b3b1-122">MFSampleExtension\_3DVideo</span></span>](mfsampleextension-3dvideo.md)
</dt> </dl>

 

 




