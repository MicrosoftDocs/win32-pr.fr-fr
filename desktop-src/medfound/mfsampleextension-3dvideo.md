---
description: Spécifie si un exemple de média contient une image vidéo 3D.
ms.assetid: 1B0B9DBD-80EB-4876-B2F2-BE419AC84265
title: Attribut MFSampleExtension_3DVideo (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e30ea247f6f12f05414df0ae4305ecaaa6e3e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524093"
---
# <a name="mfsampleextension_3dvideo-attribute"></a><span data-ttu-id="7e838-103">\_Attribut MFSampleExtension 3DVideo</span><span class="sxs-lookup"><span data-stu-id="7e838-103">MFSampleExtension\_3DVideo attribute</span></span>

<span data-ttu-id="7e838-104">Spécifie si un exemple de média contient une image vidéo 3D.</span><span class="sxs-lookup"><span data-stu-id="7e838-104">Specifies whether a media sample contains a 3D video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="7e838-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="7e838-105">Data type</span></span>

<span data-ttu-id="7e838-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e838-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7e838-107">Notes</span><span class="sxs-lookup"><span data-stu-id="7e838-107">Remarks</span></span>

<span data-ttu-id="7e838-108">Si cet attribut a la **valeur true**, l’exemple de média contient une image vidéo qui comporte deux vues stéréoscopiques ou plus.</span><span class="sxs-lookup"><span data-stu-id="7e838-108">If this attribute is **TRUE**, the media sample contains a video frame that has two or more stereoscopic views.</span></span> <span data-ttu-id="7e838-109">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="7e838-109">The default value is **FALSE**.</span></span>

<span data-ttu-id="7e838-110">Un composant qui génère des images vidéo 3D doit affecter la **valeur true** à cet attribut sur chaque échantillon de média qui contient un frame 3D.</span><span class="sxs-lookup"><span data-stu-id="7e838-110">A component that generates 3D video frames should set this attribute to **TRUE** on every media sample that contains a 3D frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e838-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e838-111">Requirements</span></span>



| <span data-ttu-id="7e838-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e838-112">Requirement</span></span> | <span data-ttu-id="7e838-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e838-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7e838-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e838-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7e838-115">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7e838-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="7e838-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e838-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7e838-117">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="7e838-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="7e838-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e838-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e838-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e838-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e838-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e838-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e838-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7e838-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7e838-122">MFSampleExtension \_ 3DVideo \_ SampleFormat</span><span class="sxs-lookup"><span data-stu-id="7e838-122">MFSampleExtension\_3DVideo\_SampleFormat</span></span>](mfsampleextension-3dvideo-sampleformat.md)
</dt> </dl>

 

 




