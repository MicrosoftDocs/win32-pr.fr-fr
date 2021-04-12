---
description: Pour un type de média qui décrit un flux de transport MPEG-2 (TS), spécifie que les paquets de transport contiennent un code d’heure de 4 octets.
ms.assetid: B172E7A8-5757-49B7-A784-FAFC7E904A4C
title: Attribut MF_MT_MPEG2_TIMECODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc9db5d7b3c6e94f7845bec2bd98c569d1b1f9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203721"
---
# <a name="mf_mt_mpeg2_timecode-attribute"></a><span data-ttu-id="59215-103">\_ \_ \_ Attribut code temporel MPEG2 MT</span><span class="sxs-lookup"><span data-stu-id="59215-103">MF\_MT\_MPEG2\_TIMECODE attribute</span></span>

<span data-ttu-id="59215-104">Pour un type de média qui décrit un flux de transport MPEG-2 (TS), spécifie que les paquets de transport contiennent un code d’heure de 4 octets.</span><span class="sxs-lookup"><span data-stu-id="59215-104">For a media type that describes an MPEG-2 transport stream (TS), specifies the transport packets contain a 4-byte time code.</span></span>

## <a name="data-type"></a><span data-ttu-id="59215-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="59215-105">Data type</span></span>

<span data-ttu-id="59215-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="59215-106">**UINT32**</span></span>



| <span data-ttu-id="59215-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="59215-107">Value</span></span>                                                                                                | <span data-ttu-id="59215-108">Signification</span><span class="sxs-lookup"><span data-stu-id="59215-108">Meaning</span></span>                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="59215-109"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="59215-109"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="59215-110">Aucun code d’heure n’est ajouté.</span><span class="sxs-lookup"><span data-stu-id="59215-110">No time code is added.</span></span><br/>                                                                                                              |
| <span id="1"></span><dl> <span data-ttu-id="59215-111"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="59215-111"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="59215-112">Un code d’heure de 4 octets est ajouté au début de chaque paquet de transport.</span><span class="sxs-lookup"><span data-stu-id="59215-112">A 4-byte time code is added at the start of each transport packet.</span></span> <span data-ttu-id="59215-113">Ce code de temps est requis par certaines normes de télévision numérique.</span><span class="sxs-lookup"><span data-stu-id="59215-113">This time code is required by some digital television standards.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="59215-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59215-114">Requirements</span></span>



| <span data-ttu-id="59215-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59215-115">Requirement</span></span> | <span data-ttu-id="59215-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="59215-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="59215-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59215-117">Minimum supported client</span></span><br/> | <span data-ttu-id="59215-118">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="59215-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="59215-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59215-119">Minimum supported server</span></span><br/> | <span data-ttu-id="59215-120">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="59215-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="59215-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="59215-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="59215-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="59215-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59215-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59215-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59215-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59215-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




