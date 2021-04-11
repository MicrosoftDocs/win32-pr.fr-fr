---
description: Vidéo FOURCCs
ms.assetid: bea4835d-fd7f-4ac3-8466-7f4e0d799a12
title: Vidéo FOURCCs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b804962308d0ecc5bf32fcddf5176905d0e17fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318917"
---
# <a name="video-fourccs"></a><span data-ttu-id="a0d61-103">Vidéo FOURCCs</span><span class="sxs-lookup"><span data-stu-id="a0d61-103">Video FOURCCs</span></span>

<span data-ttu-id="a0d61-104">De nombreux formats vidéo ont des Codes FOURCC qui leur sont affectés.</span><span class="sxs-lookup"><span data-stu-id="a0d61-104">Many video formats have FOURCC codes assigned to them.</span></span> <span data-ttu-id="a0d61-105">Un code FOURCC est un entier non signé 32 bits créé par la concaténation de quatre caractères ASCII.</span><span class="sxs-lookup"><span data-stu-id="a0d61-105">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span> <span data-ttu-id="a0d61-106">Par exemple, le code FOURCC pour la vidéo YUY2 est « YUY2 ».</span><span class="sxs-lookup"><span data-stu-id="a0d61-106">For example, the FOURCC code for YUY2 video is 'YUY2'.</span></span>

<span data-ttu-id="a0d61-107">Différentes macros C/C++ sont définies pour déclarer des valeurs FOURCC dans le code source.</span><span class="sxs-lookup"><span data-stu-id="a0d61-107">Various C/C++ macros are defined for declaring FOURCC values in source code.</span></span> <span data-ttu-id="a0d61-108">La macro **MAKEFOURCC** est définie dans Mmsystem. h, et la macro **FCC** est définie dans Aviriff. h et dans divers autres fichiers d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="a0d61-108">The **MAKEFOURCC** macro is defined in Mmsystem.h, and the **FCC** macro is defined in Aviriff.h and various other header files.</span></span> <span data-ttu-id="a0d61-109">Vous pouvez également déclarer directement un code FOURCC en tant que littéral de chaîne en inversant l’ordre des caractères.</span><span class="sxs-lookup"><span data-stu-id="a0d61-109">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="a0d61-110">Par conséquent, les instructions suivantes sont équivalentes :</span><span class="sxs-lookup"><span data-stu-id="a0d61-110">Thus, the following statements are equivalent:</span></span>

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```

<span data-ttu-id="a0d61-111">(Dans le dernier exemple, l’inversion de l’ordre des octets est nécessaire car Windows utilise une architecture Little endian.</span><span class="sxs-lookup"><span data-stu-id="a0d61-111">(In the last example, reversing the byte order is necessary because Windows uses a little-endian architecture.</span></span> <span data-ttu-id="a0d61-112">'Y' = 0x59, 'U' = 0x55, et' 2 ' = 0x32, donc' 2YUY’est 0x32595559.)</span><span class="sxs-lookup"><span data-stu-id="a0d61-112">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.)</span></span>

<span data-ttu-id="a0d61-113">Certaines API [DirectX Video Acceleration 2,0](directx-video-acceleration-2-0.md) utilisent une valeur **D3DFORMAT** pour décrire un format vidéo.</span><span class="sxs-lookup"><span data-stu-id="a0d61-113">Some of the [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md) APIs use a **D3DFORMAT** value to describe a video format.</span></span> <span data-ttu-id="a0d61-114">Un code FOURCC peut également être utilisé dans ce contexte :</span><span class="sxs-lookup"><span data-stu-id="a0d61-114">A FOURCC code can be used in this context as well:</span></span>

``` syntax
D3DFORMAT fmt = (D3DFORMAT)MAKEFOURCC('Y','U','Y','2');
D3DFORMAT fmt = (D3DFORMAT)FCC('YUY2');
D3DFORMAT fmt = D3DFORMAT('2YUY'); // Coerce to D3DFORMAT type.
```

### <a name="fourcc-constants"></a><span data-ttu-id="a0d61-115">Constantes FOURCC</span><span class="sxs-lookup"><span data-stu-id="a0d61-115">FOURCC Constants</span></span>

<span data-ttu-id="a0d61-116">Le tableau suivant répertorie certains codes FOURCC courants.</span><span class="sxs-lookup"><span data-stu-id="a0d61-116">The following table lists some common FOURCC codes.</span></span>



| <span data-ttu-id="a0d61-117">Valeur FOURCC</span><span class="sxs-lookup"><span data-stu-id="a0d61-117">FOURCC value</span></span> | <span data-ttu-id="a0d61-118">Description</span><span class="sxs-lookup"><span data-stu-id="a0d61-118">Description</span></span>                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0d61-119">H264 –</span><span class="sxs-lookup"><span data-stu-id="a0d61-119">'H264'</span></span>       | <span data-ttu-id="a0d61-120">Vidéo H. 264.</span><span class="sxs-lookup"><span data-stu-id="a0d61-120">H.264 video.</span></span>                                                                                                          |
| <span data-ttu-id="a0d61-121">'I420'</span><span class="sxs-lookup"><span data-stu-id="a0d61-121">'I420'</span></span>       | <span data-ttu-id="a0d61-122">Vidéo YUV stockée au format 4:2:0 planaire.</span><span class="sxs-lookup"><span data-stu-id="a0d61-122">YUV video stored in planar 4:2:0 format.</span></span>                                                                              |
| <span data-ttu-id="a0d61-123">'IYUV'</span><span class="sxs-lookup"><span data-stu-id="a0d61-123">'IYUV'</span></span>       | <span data-ttu-id="a0d61-124">Vidéo YUV stockée au format 4:2:0 planaire.</span><span class="sxs-lookup"><span data-stu-id="a0d61-124">YUV video stored in planar 4:2:0 format.</span></span>                                                                              |
| <span data-ttu-id="a0d61-125">4S2 ' '</span><span class="sxs-lookup"><span data-stu-id="a0d61-125">'M4S2'</span></span>       | <span data-ttu-id="a0d61-126">Vidéo MPEG-4 part 2.</span><span class="sxs-lookup"><span data-stu-id="a0d61-126">MPEG-4 part 2 video.</span></span>                                                                                                  |
| <span data-ttu-id="a0d61-127">FICHIERS MP4 À</span><span class="sxs-lookup"><span data-stu-id="a0d61-127">'MP4S'</span></span>       | <span data-ttu-id="a0d61-128">Codec Microsoft MPEG 4 version 3.</span><span class="sxs-lookup"><span data-stu-id="a0d61-128">Microsoft MPEG 4 codec version 3.</span></span> <span data-ttu-id="a0d61-129">Ce codec n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a0d61-129">This codec is no longer supported.</span></span>                                                  |
| <span data-ttu-id="a0d61-130">Mp4v</span><span class="sxs-lookup"><span data-stu-id="a0d61-130">'MP4V'</span></span>       | <span data-ttu-id="a0d61-131">Vidéo MPEG-4 part 2.</span><span class="sxs-lookup"><span data-stu-id="a0d61-131">MPEG-4 part 2 video.</span></span>                                                                                                  |
| <span data-ttu-id="a0d61-132">'MPG1'</span><span class="sxs-lookup"><span data-stu-id="a0d61-132">'MPG1'</span></span>       | <span data-ttu-id="a0d61-133">Vidéo MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="a0d61-133">MPEG-1 video.</span></span>                                                                                                         |
| <span data-ttu-id="a0d61-134">'MSS1'</span><span class="sxs-lookup"><span data-stu-id="a0d61-134">'MSS1'</span></span>       | <span data-ttu-id="a0d61-135">Contenu encodé avec le codec d’écran Windows Media Video 7.</span><span class="sxs-lookup"><span data-stu-id="a0d61-135">Content encoded with the Windows Media Video 7 screen codec.</span></span>                                                          |
| <span data-ttu-id="a0d61-136">'MSS2'</span><span class="sxs-lookup"><span data-stu-id="a0d61-136">'MSS2'</span></span>       | <span data-ttu-id="a0d61-137">Contenu encodé avec le codec d’écran Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="a0d61-137">Content encoded with the Windows Media Video 9 screen codec.</span></span>                                                          |
| <span data-ttu-id="a0d61-138">UYVY</span><span class="sxs-lookup"><span data-stu-id="a0d61-138">'UYVY'</span></span>       | <span data-ttu-id="a0d61-139">Vidéo YUV stockée au format 4:2:2 compressé.</span><span class="sxs-lookup"><span data-stu-id="a0d61-139">YUV video stored in packed 4:2:2 format.</span></span> <span data-ttu-id="a0d61-140">Semblable à YUY2 mais avec un classement des données différent.</span><span class="sxs-lookup"><span data-stu-id="a0d61-140">Similar to YUY2 but with different ordering of data.</span></span>                         |
| <span data-ttu-id="a0d61-141">'WMV1'</span><span class="sxs-lookup"><span data-stu-id="a0d61-141">'WMV1'</span></span>       | <span data-ttu-id="a0d61-142">Contenu encodé avec le codec Windows Media Video 7.</span><span class="sxs-lookup"><span data-stu-id="a0d61-142">Content encoded with the Windows Media Video 7 codec.</span></span>                                                                 |
| <span data-ttu-id="a0d61-143">'WMV2'</span><span class="sxs-lookup"><span data-stu-id="a0d61-143">'WMV2'</span></span>       | <span data-ttu-id="a0d61-144">Contenu encodé avec le codec Windows Media Video 8.</span><span class="sxs-lookup"><span data-stu-id="a0d61-144">Content encoded with the Windows Media Video 8 codec.</span></span>                                                                 |
| <span data-ttu-id="a0d61-145">'WMV3'</span><span class="sxs-lookup"><span data-stu-id="a0d61-145">'WMV3'</span></span>       | <span data-ttu-id="a0d61-146">Contenu encodé avec le codec Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="a0d61-146">Content encoded with the Windows Media Video 9 codec.</span></span>                                                                 |
| <span data-ttu-id="a0d61-147">'WMVA'</span><span class="sxs-lookup"><span data-stu-id="a0d61-147">'WMVA'</span></span>       | <span data-ttu-id="a0d61-148">Contenu encodé avec la version obsolète la plus ancienne du codec de profil avancé Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="a0d61-148">Content encoded with the older, obsolete version of the Windows Media Video 9 Advanced Profile codec.</span></span>                 |
| <span data-ttu-id="a0d61-149">'WMVP'</span><span class="sxs-lookup"><span data-stu-id="a0d61-149">'WMVP'</span></span>       | <span data-ttu-id="a0d61-150">Contenu encodé avec le codec d’image Windows Media Video 9,1.</span><span class="sxs-lookup"><span data-stu-id="a0d61-150">Content encoded with the Windows Media Video 9.1 Image codec.</span></span>                                                         |
| <span data-ttu-id="a0d61-151">'WVC1'</span><span class="sxs-lookup"><span data-stu-id="a0d61-151">'WVC1'</span></span>       | <span data-ttu-id="a0d61-152">SMPTE 421M (« VC-1 »).</span><span class="sxs-lookup"><span data-stu-id="a0d61-152">SMPTE 421M ("VC-1").</span></span> <span data-ttu-id="a0d61-153">Contenu encodé avec le profil avancé Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="a0d61-153">Content encoded with Windows Media Video 9 Advanced Profile.</span></span>                                     |
| <span data-ttu-id="a0d61-154">'WVP2'</span><span class="sxs-lookup"><span data-stu-id="a0d61-154">'WVP2'</span></span>       | <span data-ttu-id="a0d61-155">Contenu encodé avec le codec Windows Media Video 9,1 image v2.</span><span class="sxs-lookup"><span data-stu-id="a0d61-155">Content encoded with the Windows Media Video 9.1 Image v2 codec.</span></span>                                                      |
| <span data-ttu-id="a0d61-156">YUY2</span><span class="sxs-lookup"><span data-stu-id="a0d61-156">'YUY2'</span></span>       | <span data-ttu-id="a0d61-157">Vidéo YUV stockée au format 4:2:2 compressé.</span><span class="sxs-lookup"><span data-stu-id="a0d61-157">YUV video stored in packed 4:2:2 format.</span></span>                                                                              |
| <span data-ttu-id="a0d61-158">'YV12'</span><span class="sxs-lookup"><span data-stu-id="a0d61-158">'YV12'</span></span>       | <span data-ttu-id="a0d61-159">Vidéo YUV stockée au format 4:2:0 ou 4:1:1 planaire.</span><span class="sxs-lookup"><span data-stu-id="a0d61-159">YUV video stored in planar 4:2:0 or 4:1:1 format.</span></span> <span data-ttu-id="a0d61-160">Identique à I420/IYUV, sauf que les plans vous et V sont basculés.</span><span class="sxs-lookup"><span data-stu-id="a0d61-160">Identical to I420/IYUV except that the U and V planes are switched.</span></span> |
| <span data-ttu-id="a0d61-161">YVU9</span><span class="sxs-lookup"><span data-stu-id="a0d61-161">'YVU9'</span></span>       | <span data-ttu-id="a0d61-162">Vidéo YUV stockée au format 16:1:1 planaire.</span><span class="sxs-lookup"><span data-stu-id="a0d61-162">YUV video stored in planar 16:1:1 format.</span></span>                                                                             |
| <span data-ttu-id="a0d61-163">YVYU</span><span class="sxs-lookup"><span data-stu-id="a0d61-163">'YVYU'</span></span>       | <span data-ttu-id="a0d61-164">Vidéo YUV stockée au format 4:2:2 compressé.</span><span class="sxs-lookup"><span data-stu-id="a0d61-164">YUV video stored in packed 4:2:2 format.</span></span> <span data-ttu-id="a0d61-165">Semblable à YUY2 mais avec un classement des données différent.</span><span class="sxs-lookup"><span data-stu-id="a0d61-165">Similar to YUY2 but with different ordering of data.</span></span>                         |



 

## <a name="related-topics"></a><span data-ttu-id="a0d61-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0d61-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0d61-167">Types de média vidéo</span><span class="sxs-lookup"><span data-stu-id="a0d61-167">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="a0d61-168">GUID de sous-type de vidéo</span><span class="sxs-lookup"><span data-stu-id="a0d61-168">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 



