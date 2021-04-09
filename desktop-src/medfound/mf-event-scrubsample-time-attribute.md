---
description: Durée de présentation d’un échantillon rendu lors du nettoyage.
ms.assetid: 6ce52cf5-014b-49a2-abf7-2c9cc5340a42
title: Attribut MF_EVENT_SCRUBSAMPLE_TIME (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7c4fb1a8015367fa3d48edb066cdb135983926
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951540"
---
# <a name="mf_event_scrubsample_time-attribute"></a><span data-ttu-id="db3d7-103">\_Attribut de \_ \_ durée SCRUBSAMPLE de l’événement MF</span><span class="sxs-lookup"><span data-stu-id="db3d7-103">MF\_EVENT\_SCRUBSAMPLE\_TIME attribute</span></span>

<span data-ttu-id="db3d7-104">Durée de présentation d’un échantillon rendu lors du nettoyage.</span><span class="sxs-lookup"><span data-stu-id="db3d7-104">Presentation time for a sample that was rendered while scrubbing.</span></span>

## <a name="data-type"></a><span data-ttu-id="db3d7-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="db3d7-105">Data type</span></span>

<span data-ttu-id="db3d7-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="db3d7-106">**UINT64**</span></span>

<span data-ttu-id="db3d7-107">Traiter en tant que valeur **LongLong** .</span><span class="sxs-lookup"><span data-stu-id="db3d7-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="db3d7-108">Notes</span><span class="sxs-lookup"><span data-stu-id="db3d7-108">Remarks</span></span>

<span data-ttu-id="db3d7-109">Cet attribut est utilisé avec l’événement [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="db3d7-109">This attribute is used with the [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md) event.</span></span>

<span data-ttu-id="db3d7-110">Cet attribut est une valeur signée, bien qu’il soit stocké en tant que **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="db3d7-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="db3d7-111">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="db3d7-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="db3d7-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db3d7-112">Requirements</span></span>



| <span data-ttu-id="db3d7-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db3d7-113">Requirement</span></span> | <span data-ttu-id="db3d7-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="db3d7-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="db3d7-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db3d7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="db3d7-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db3d7-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="db3d7-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db3d7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="db3d7-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db3d7-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="db3d7-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="db3d7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="db3d7-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="db3d7-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db3d7-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db3d7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db3d7-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="db3d7-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="db3d7-123">Attributs d'événement</span><span class="sxs-lookup"><span data-stu-id="db3d7-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="db3d7-124">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="db3d7-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="db3d7-125">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="db3d7-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




