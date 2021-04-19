---
description: Les GUID suivants sont utilisés pour le suivi d’événements dans DirectShow.
ms.assetid: 438938fe-37e7-45d6-b49a-d96698307f25
title: GUID de trace (PerfStruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AUDIOBREAK
- GUID_DSHOW_CTL
- GUID_STREAMTRACE
- GUID_VIDEOREND
api_type:
- HeaderDef
api_location:
- PerfStruct.h
ms.openlocfilehash: 4b2f2a6a678c029d01d9bf55481837d81d48557e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534828"
---
# <a name="trace-guids"></a><span data-ttu-id="c7209-103">GUID de trace</span><span class="sxs-lookup"><span data-stu-id="c7209-103">Trace GUIDs</span></span>

<span data-ttu-id="c7209-104">Les GUID suivants sont utilisés pour le suivi d’événements dans DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c7209-104">The following GUIDs are used for event tracing in DirectShow.</span></span>



| <span data-ttu-id="c7209-105">GUID</span><span class="sxs-lookup"><span data-stu-id="c7209-105">GUID</span></span>                                                                                                                                                                   | <span data-ttu-id="c7209-106">Description</span><span class="sxs-lookup"><span data-stu-id="c7209-106">Description</span></span>                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AUDIOBREAK"></span><span id="guid_audiobreak"></span><dl> <span data-ttu-id="c7209-107"><dt>**GUID \_ AUDIOBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="c7209-107"><dt>**GUID\_AUDIOBREAK**</dt></span></span> </dl>    | <span data-ttu-id="c7209-108">Événement d’arrêt audio.</span><span class="sxs-lookup"><span data-stu-id="c7209-108">Audio break event.</span></span> <span data-ttu-id="c7209-109">Les événements de ce type utilisent la structure [**PERFINFO \_ DShow \_ AUDIOBREAK**](perfinfo-dshow-audiobreak.md) pour les données d’événement.</span><span class="sxs-lookup"><span data-stu-id="c7209-109">Events of this type use the [**PERFINFO\_DSHOW\_AUDIOBREAK**](perfinfo-dshow-audiobreak.md) structure for event data.</span></span><br/>         |
| <span id="GUID_DSHOW_CTL"></span><span id="guid_dshow_ctl"></span><dl> <span data-ttu-id="c7209-110"><dt>**GUID de la \_ \_ liste CTL DShow**</dt></span><span class="sxs-lookup"><span data-stu-id="c7209-110"><dt>**GUID\_DSHOW\_CTL**</dt></span></span> </dl>      | <span data-ttu-id="c7209-111">Fournisseur d’événements DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c7209-111">DirectShow event provider.</span></span><br/>                                                                                                                        |
| <span id="GUID_STREAMTRACE"></span><span id="guid_streamtrace"></span><dl> <span data-ttu-id="c7209-112"><dt>**GUID \_ STREAMTRACE**</dt></span><span class="sxs-lookup"><span data-stu-id="c7209-112"><dt>**GUID\_STREAMTRACE**</dt></span></span> </dl> | <span data-ttu-id="c7209-113">Événement de diffusion générale.</span><span class="sxs-lookup"><span data-stu-id="c7209-113">General streaming event.</span></span> <span data-ttu-id="c7209-114">Les événements de ce type utilisent la structure [**PERFINFO \_ DShow \_ STREAMTRACE**](perfinfo-dshow-streamtrace.md) pour les données d’événement.</span><span class="sxs-lookup"><span data-stu-id="c7209-114">Events of this type use the [**PERFINFO\_DSHOW\_STREAMTRACE**](perfinfo-dshow-streamtrace.md) structure for event data.</span></span><br/> |
| <span id="GUID_VIDEOREND"></span><span id="guid_videorend"></span><dl> <span data-ttu-id="c7209-115"><dt>**GUID \_ VIDEOREND**</dt></span><span class="sxs-lookup"><span data-stu-id="c7209-115"><dt>**GUID\_VIDEOREND**</dt></span></span> </dl>       | <span data-ttu-id="c7209-116">Événement de rendu vidéo.</span><span class="sxs-lookup"><span data-stu-id="c7209-116">Video rendering event.</span></span> <span data-ttu-id="c7209-117">Les événements de ce type utilisent la structure [**PERFINFO \_ DShow \_ AVREND**](perfinfo-dshow-avrend.md) pour les données d’événement.</span><span class="sxs-lookup"><span data-stu-id="c7209-117">Events of this type use the [**PERFINFO\_DSHOW\_AVREND**](perfinfo-dshow-avrend.md) structure for event data.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="c7209-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7209-118">Requirements</span></span>



| <span data-ttu-id="c7209-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7209-119">Requirement</span></span> | <span data-ttu-id="c7209-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7209-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7209-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7209-121">Header</span></span><br/> | <dl> <span data-ttu-id="c7209-122"><dt>PerfStruct. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7209-122"><dt>PerfStruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7209-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7209-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7209-124">Suivi d’événements dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="c7209-124">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> </dl>

 

 




