---
description: Pour un type de média qui décrit un flux de programme (PS) MPEG-2 ou un flux de transport (TS), spécifie la norme utilisée pour multiplexer le flux.
ms.assetid: 3D4C1A81-A9BA-427F-93DB-F522A0616EAB
title: Attribut MF_MT_MPEG2_STANDARD (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0650a68975f449ea938b41872005e11d79922393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518202"
---
# <a name="mf_mt_mpeg2_standard-attribute"></a><span data-ttu-id="e1e0c-103">\_ \_ Attribut standard MF MT MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="e1e0c-103">MF\_MT\_MPEG2\_STANDARD attribute</span></span>

<span data-ttu-id="e1e0c-104">Pour un type de média qui décrit un flux de programme (PS) MPEG-2 ou un flux de transport (TS), spécifie la norme utilisée pour multiplexer le flux.</span><span class="sxs-lookup"><span data-stu-id="e1e0c-104">For a media type that describes an MPEG-2 program stream (PS) or transport stream (TS), specifies the standard that is used to multiplex the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="e1e0c-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="e1e0c-105">Data type</span></span>

<span data-ttu-id="e1e0c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e1e0c-106">**UINT32**</span></span>



| <span data-ttu-id="e1e0c-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1e0c-107">Value</span></span>                                                                                                | <span data-ttu-id="e1e0c-108">Signification</span><span class="sxs-lookup"><span data-stu-id="e1e0c-108">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="e1e0c-109"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0c-109"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="e1e0c-110">Standard MPEG-2 PS ou TS.</span><span class="sxs-lookup"><span data-stu-id="e1e0c-110">Standard MPEG-2 PS or TS.</span></span><br/>                                       |
| <span id="1"></span><dl> <span data-ttu-id="e1e0c-111"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0c-111"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="e1e0c-112">Norme ATSC (Advanced TV Systems Committee).</span><span class="sxs-lookup"><span data-stu-id="e1e0c-112">Advanced Television Systems Committee (ATSC) standard.</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="e1e0c-113"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0c-113"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="e1e0c-114">Norme de diffusion vidéo numérique (DVB).</span><span class="sxs-lookup"><span data-stu-id="e1e0c-114">Digital Video Broadcasting (DVB) standard.</span></span><br/>                      |
| <span id="3"></span><dl> <span data-ttu-id="e1e0c-115"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0c-115"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="e1e0c-116">Association de la norme ARIB (Radio Industries and Business).</span><span class="sxs-lookup"><span data-stu-id="e1e0c-116">Association of Radio Industries and Businesses (ARIB) standard.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e1e0c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1e0c-117">Requirements</span></span>



| <span data-ttu-id="e1e0c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1e0c-118">Requirement</span></span> | <span data-ttu-id="e1e0c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1e0c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e1e0c-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1e0c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e1e0c-121">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e1e0c-121">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="e1e0c-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1e0c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e1e0c-123">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="e1e0c-123">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e1e0c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1e0c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1e0c-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0c-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1e0c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1e0c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1e0c-127">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e1e0c-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




