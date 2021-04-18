---
description: Pour plusieurs GUID de type de média MPEG-2, le DDK Windows définit des noms qui diffèrent de ceux utilisés dans DirectShow. Le tableau suivant présente les noms DirectShow (définis dans Ksuuids. h) et les noms en mode noyau correspondants (définis dans Ksmedia. h).
ms.assetid: ecf94552-5a0f-464c-9f9b-4861faa38d05
title: Types de média de noyau MPEG-2 (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b03e6d3cbc32c987110ceac98e6aeef6617d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528914"
---
# <a name="mpeg-2-kernel-media-types"></a><span data-ttu-id="e7502-104">Types de média de noyau MPEG-2</span><span class="sxs-lookup"><span data-stu-id="e7502-104">MPEG-2 Kernel Media Types</span></span>

<span data-ttu-id="e7502-105">Pour plusieurs GUID de type de média MPEG-2, le DDK Windows définit des noms qui diffèrent de ceux utilisés dans DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e7502-105">For several MPEG-2 media type GUIDs, the Windows DDK defines names that differ from the names used in DirectShow.</span></span> <span data-ttu-id="e7502-106">Le tableau suivant présente les noms DirectShow (définis dans Ksuuids. h) et les noms en mode noyau correspondants (définis dans Ksmedia. h).</span><span class="sxs-lookup"><span data-stu-id="e7502-106">The following table shows the DirectShow names (defined in Ksuuids.h) and the corresponding kernel-mode names (defined in Ksmedia.h).</span></span>



| <span data-ttu-id="e7502-107">Nom dans Ksuuids. h</span><span class="sxs-lookup"><span data-stu-id="e7502-107">Name in Ksuuids.h</span></span>              | <span data-ttu-id="e7502-108">Nom dans Ksmedia. h</span><span class="sxs-lookup"><span data-stu-id="e7502-108">Name in Ksmedia.h</span></span>                          |
|--------------------------------|--------------------------------------------|
| <span data-ttu-id="e7502-109">FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="e7502-109">FORMAT\_WaveFormatEx</span></span>           | <span data-ttu-id="e7502-110">\_spécificateur KSDATAFORMAT \_ WAVEFORMATEX</span><span class="sxs-lookup"><span data-stu-id="e7502-110">KSDATAFORMAT\_SPECIFIER\_WAVEFORMATEX</span></span>      |
| <span data-ttu-id="e7502-111">FORMAT \_ mpeg2video</span><span class="sxs-lookup"><span data-stu-id="e7502-111">FORMAT\_MPEG2Video</span></span>             | <span data-ttu-id="e7502-112">Vidéo sur le \_ spécificateur KSDATAFORMAT \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="e7502-112">KSDATAFORMAT\_SPECIFIER\_MPEG2\_VIDEO</span></span>      |
| <span data-ttu-id="e7502-113">MEDIASUBTYPE \_ ATSC \_ si</span><span class="sxs-lookup"><span data-stu-id="e7502-113">MEDIASUBTYPE\_ATSC\_SI</span></span>         | <span data-ttu-id="e7502-114">KSDATAFORMAT \_ sous-type \_ ATSC \_ si</span><span class="sxs-lookup"><span data-stu-id="e7502-114">KSDATAFORMAT\_SUBTYPE\_ATSC\_SI</span></span>            |
| <span data-ttu-id="e7502-115">MEDIASUBTYPE \_ Dolby \_ AC3</span><span class="sxs-lookup"><span data-stu-id="e7502-115">MEDIASUBTYPE\_DOLBY\_AC3</span></span>       | <span data-ttu-id="e7502-116">KSDATAFORMAT \_ sous-type \_ AC3 \_ audio</span><span class="sxs-lookup"><span data-stu-id="e7502-116">KSDATAFORMAT\_SUBTYPE\_AC3\_AUDIO</span></span>          |
| <span data-ttu-id="e7502-117">MEDIASUBTYPE \_ DVB \_ si</span><span class="sxs-lookup"><span data-stu-id="e7502-117">MEDIASUBTYPE\_DVB\_SI</span></span>          | <span data-ttu-id="e7502-118">KSDATAFORMAT \_ sous-type \_ DVB \_ si</span><span class="sxs-lookup"><span data-stu-id="e7502-118">KSDATAFORMAT\_SUBTYPE\_DVB\_SI</span></span>             |
| <span data-ttu-id="e7502-119">MEDIASUBTYPE \_ DVD \_ LPCM \_ audio</span><span class="sxs-lookup"><span data-stu-id="e7502-119">MEDIASUBTYPE\_DVD\_LPCM\_AUDIO</span></span> | <span data-ttu-id="e7502-120">KSDATAFORMAT \_ sous-type \_ LPCM \_ audio</span><span class="sxs-lookup"><span data-stu-id="e7502-120">KSDATAFORMAT\_SUBTYPE\_LPCM\_AUDIO</span></span>         |
| <span data-ttu-id="e7502-121">MEDIASUBTYPE \_ MPEG2 \_ audio</span><span class="sxs-lookup"><span data-stu-id="e7502-121">MEDIASUBTYPE\_MPEG2\_AUDIO</span></span>     | <span data-ttu-id="e7502-122">KSDATAFORMAT \_ sous-type \_ MPEG2 \_ audio</span><span class="sxs-lookup"><span data-stu-id="e7502-122">KSDATAFORMAT\_SUBTYPE\_MPEG2\_AUDIO</span></span>        |
| <span data-ttu-id="e7502-123">\_Programme MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="e7502-123">MEDIASUBTYPE\_MPEG2\_PROGRAM</span></span>   | <span data-ttu-id="e7502-124">\_ \_ Programme MPEG2 de type KSDATAFORMAT \_ statique \_</span><span class="sxs-lookup"><span data-stu-id="e7502-124">STATIC\_KSDATAFORMAT\_TYPE\_MPEG2\_PROGRAM</span></span> |
| <span data-ttu-id="e7502-125">\_Transport MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="e7502-125">MEDIASUBTYPE\_MPEG2\_TRANSPORT</span></span> | <span data-ttu-id="e7502-126">\_ \_ Transport MPEG2 de type KSDATAFORMAT \_</span><span class="sxs-lookup"><span data-stu-id="e7502-126">KSDATAFORMAT\_TYPE\_MPEG2\_TRANSPORT</span></span>       |
| <span data-ttu-id="e7502-127">\_Vidéo MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="e7502-127">MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>     | <span data-ttu-id="e7502-128">\_Vidéo MPEG2 de sous-type KSDATAFORMAT \_ \_</span><span class="sxs-lookup"><span data-stu-id="e7502-128">KSDATAFORMAT\_SUBTYPE\_MPEG2\_VIDEO</span></span>        |
| <span data-ttu-id="e7502-129">SECTIONS de MEDIATYPE \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="e7502-129">MEDIATYPE\_MPEG2\_SECTIONS</span></span>     | <span data-ttu-id="e7502-130">KSDATAFORMAT, \_ type, \_ \_ sections MPEG2</span><span class="sxs-lookup"><span data-stu-id="e7502-130">KSDATAFORMAT\_TYPE\_MPEG2\_SECTIONS</span></span>        |
| <span data-ttu-id="e7502-131">Audio de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="e7502-131">MEDIATYPE\_Audio</span></span>               | <span data-ttu-id="e7502-132">KSDATAFORMAT \_ type \_ audio</span><span class="sxs-lookup"><span data-stu-id="e7502-132">KSDATAFORMAT\_TYPE\_AUDIO</span></span>                  |
| <span data-ttu-id="e7502-133">\_PES MPEG2 de MediaType \_</span><span class="sxs-lookup"><span data-stu-id="e7502-133">MEDIATYPE\_MPEG2\_PES</span></span>          | <span data-ttu-id="e7502-134">KSDATAFORMAT \_ type \_ MPEG2 \_ PES</span><span class="sxs-lookup"><span data-stu-id="e7502-134">KSDATAFORMAT\_TYPE\_MPEG2\_PES</span></span>             |
| <span data-ttu-id="e7502-135">Vidéo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="e7502-135">MEDIATYPE\_Video</span></span>               | <span data-ttu-id="e7502-136">\_vidéo de type KSDATAFORMAT \_</span><span class="sxs-lookup"><span data-stu-id="e7502-136">KSDATAFORMAT\_TYPE\_VIDEO</span></span>                  |



 

## <a name="requirements"></a><span data-ttu-id="e7502-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7502-137">Requirements</span></span>



| <span data-ttu-id="e7502-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7502-138">Requirement</span></span> | <span data-ttu-id="e7502-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7502-139">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e7502-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7502-140">Header</span></span><br/> | <dl> <span data-ttu-id="e7502-141"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7502-141"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7502-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7502-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7502-143">Types de média MPEG-2</span><span class="sxs-lookup"><span data-stu-id="e7502-143">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 




