---
description: Le décodeur Windows Media Video 9 décode les flux vidéo qui ont été encodés par l’encodeur Windows Media Video.
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: Décodeur Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d89e05f82ce503016a10d5591a23bc673d0db5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539949"
---
# <a name="windows-media-video-9-decoder"></a><span data-ttu-id="e0aff-103">Décodeur Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="e0aff-103">Windows Media Video 9 Decoder</span></span>

<span data-ttu-id="e0aff-104">Le décodeur Windows Media Video 9 décode les flux vidéo qui ont été encodés par l’encodeur [**Windows Media Video**](windowsmediavideo9encoder.md).</span><span class="sxs-lookup"><span data-stu-id="e0aff-104">The Windows Media Video 9 decoder decodes video streams that were encoded by the [**Windows Media Video Encoder**](windowsmediavideo9encoder.md).</span></span> <span data-ttu-id="e0aff-105">L’encodeur et le décodeur prennent en charge les quatre catégories de vidéo encodées suivantes.</span><span class="sxs-lookup"><span data-stu-id="e0aff-105">The encoder and decoder support the following four categories of encoded video.</span></span>

-   <span data-ttu-id="e0aff-106">Profil simple Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="e0aff-106">Windows Media Video 9 Simple Profile</span></span>
-   <span data-ttu-id="e0aff-107">Profil principal du Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="e0aff-107">Windows Media Video 9 Main Profile</span></span>
-   <span data-ttu-id="e0aff-108">Profil avancé Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="e0aff-108">Windows Media Video 9 Advanced Profile</span></span>
-   <span data-ttu-id="e0aff-109">Image Windows Media Video 9,1</span><span class="sxs-lookup"><span data-stu-id="e0aff-109">Windows Media Video 9.1 Image</span></span>

## <a name="class-identifier"></a><span data-ttu-id="e0aff-110">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="e0aff-110">Class Identifier</span></span>

<span data-ttu-id="e0aff-111">L’identificateur de classe (CLSID) du décodeur de Windows Media Video est représenté par la constante **CLSID \_ CWMVDecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="e0aff-111">The class identifier (CLSID) for the Windows Media Video decoder is represented by the constant **CLSID\_CWMVDecMediaObject**.</span></span> <span data-ttu-id="e0aff-112">Vous pouvez créer une instance du décodeur vidéo en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="e0aff-112">You can create an instance of the video decoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="e0aff-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="e0aff-113">Interfaces</span></span>

<span data-ttu-id="e0aff-114">Un objet décodeur vidéo expose l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) afin que l’objet puisse être utilisé en tant qu’objet de média DirectX (DMO) et expose l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="e0aff-114">A video decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="e0aff-115">Un décodeur vidéo se comporte comme un DMO ou une table MFT en fonction des interfaces que vous obtenez et de la version de Windows en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e0aff-115">A video decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="e0aff-116">Le tableau suivant indique les conditions sous lesquelles un décodeur vidéo se comporte comme un DMO ou une table MFT.</span><span class="sxs-lookup"><span data-stu-id="e0aff-116">The following table shows the conditions under which a video decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="e0aff-117">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="e0aff-117">Operating system</span></span>            | <span data-ttu-id="e0aff-118">Comportement du décodeur</span><span class="sxs-lookup"><span data-stu-id="e0aff-118">Decoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0aff-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e0aff-119">Windows XP</span></span>                  | <span data-ttu-id="e0aff-120">Un décodeur vidéo Windows Media se comporte toujours comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="e0aff-120">A Windows Media video decoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="e0aff-121">Windows Vista et Windows 7</span><span class="sxs-lookup"><span data-stu-id="e0aff-121">Windows Vista and Windows 7</span></span> | <span data-ttu-id="e0aff-122">Par défaut, un décodeur vidéo Windows Media se comporte comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="e0aff-122">By default, a Windows Media video decoder behaves as a DMO.</span></span> <span data-ttu-id="e0aff-123">Si vous obtenez une interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) sur un décodeur vidéo, il se comporte comme une table MFT.</span><span class="sxs-lookup"><span data-stu-id="e0aff-123">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="e0aff-124">À partir de Windows 7, le décodeur Windows Media Video implémente l’interface [**IDMOQualityControl**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) .</span><span class="sxs-lookup"><span data-stu-id="e0aff-124">Beginning with Windows 7, the Windows Media Video decoder implements the [**IDMOQualityControl**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) interface.</span></span>

## <a name="input-formats"></a><span data-ttu-id="e0aff-125">Formats d’entrée</span><span class="sxs-lookup"><span data-stu-id="e0aff-125">Input Formats</span></span>

<span data-ttu-id="e0aff-126">Le tableau suivant présente les codes à quatre caractères (FOURCCs) qui correspondent aux catégories d’entrées encodées prises en charge par le décodeur Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="e0aff-126">The following table shows the four-character codes (FOURCCs) that correspond to the categories of encoded input that are supported by the Windows Media Video decoder.</span></span>



| <span data-ttu-id="e0aff-127">Category</span><span class="sxs-lookup"><span data-stu-id="e0aff-127">Category</span></span>                               | <span data-ttu-id="e0aff-128">FOURCC</span><span class="sxs-lookup"><span data-stu-id="e0aff-128">FOURCC</span></span>                                   |
|----------------------------------------|------------------------------------------|
| <span data-ttu-id="e0aff-129">Profil simple Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="e0aff-129">Windows Media Video 9 Simple Profile</span></span>   | <span data-ttu-id="e0aff-130">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="e0aff-130">"WMV3"</span></span>                                   |
| <span data-ttu-id="e0aff-131">Profil principal du Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="e0aff-131">Windows Media Video 9 Main Profile</span></span>     | <span data-ttu-id="e0aff-132">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="e0aff-132">"WMV3"</span></span>                                   |
| <span data-ttu-id="e0aff-133">Profil avancé Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="e0aff-133">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="e0aff-134">"WVC1"</span><span class="sxs-lookup"><span data-stu-id="e0aff-134">"WVC1"</span></span>                                   |
| <span data-ttu-id="e0aff-135">Image Windows Media Video 9,1</span><span class="sxs-lookup"><span data-stu-id="e0aff-135">Windows Media Video 9.1 Image</span></span>          | <span data-ttu-id="e0aff-136">« WMVP » pour 9,1, « WVP2 » pour 9,1 version 2</span><span class="sxs-lookup"><span data-stu-id="e0aff-136">"WMVP" for 9.1, "WVP2" for 9.1 version 2</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="e0aff-137">Formats de sortie</span><span class="sxs-lookup"><span data-stu-id="e0aff-137">Output Formats</span></span>

<span data-ttu-id="e0aff-138">Le décodeur Windows Media Video prend en charge les sous-types de médias de sortie suivants lorsqu’il agit en tant que DMO.</span><span class="sxs-lookup"><span data-stu-id="e0aff-138">The Windows Media Video decoder supports the following output media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="e0aff-139">MEDIASUBTYPE \_ NV12</span><span class="sxs-lookup"><span data-stu-id="e0aff-139">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="e0aff-140">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="e0aff-140">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="e0aff-141">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="e0aff-141">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="e0aff-142">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="e0aff-142">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="e0aff-143">MEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="e0aff-143">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="e0aff-144">MEDIASUBTYPE \_ NV11</span><span class="sxs-lookup"><span data-stu-id="e0aff-144">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="e0aff-145">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="e0aff-145">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="e0aff-146">MEDIASUBTYPE \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="e0aff-146">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="e0aff-147">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="e0aff-147">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="e0aff-148">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="e0aff-148">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="e0aff-149">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="e0aff-149">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="e0aff-150">Le décodeur Windows Media Video prend en charge les sous-types de médias de sortie suivants lorsqu’il joue le rôle de MFT.</span><span class="sxs-lookup"><span data-stu-id="e0aff-150">The Windows Media Video decoder supports the following output media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="e0aff-151">MFVideoFormat \_ NV12</span><span class="sxs-lookup"><span data-stu-id="e0aff-151">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="e0aff-152">MFVideoFormat \_ YV12</span><span class="sxs-lookup"><span data-stu-id="e0aff-152">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="e0aff-153">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="e0aff-153">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="e0aff-154">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="e0aff-154">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="e0aff-155">MFVideoFormat \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="e0aff-155">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="e0aff-156">MFVideoFormat \_ NV11</span><span class="sxs-lookup"><span data-stu-id="e0aff-156">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="e0aff-157">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="e0aff-157">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="e0aff-158">MFVideoFormat \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="e0aff-158">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="e0aff-159">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="e0aff-159">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="e0aff-160">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="e0aff-160">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="e0aff-161">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="e0aff-161">MFVideoFormat\_RGB8</span></span>

## <a name="properties"></a><span data-ttu-id="e0aff-162">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e0aff-162">Properties</span></span>

<span data-ttu-id="e0aff-163">Le décodeur Windows Media Video prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e0aff-163">The Windows Media Video decoder supports the following properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e0aff-164">Propriété</span><span class="sxs-lookup"><span data-stu-id="e0aff-164">Property</span></span></th>
<th><span data-ttu-id="e0aff-165">Description</span><span class="sxs-lookup"><span data-stu-id="e0aff-165">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e0aff-166"><a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a></span><span class="sxs-lookup"><span data-stu-id="e0aff-166"><a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a></span></span></td>
<td><span data-ttu-id="e0aff-167">Spécifie si le codec décode les images vidéo entrelacées du flux compressé en tant que trames progressives.</span><span class="sxs-lookup"><span data-stu-id="e0aff-167">Specifies whether the codec decodes interlaced video frames from the compressed stream as progressive frames.</span></span><br/> <dl> <span data-ttu-id="e0aff-168">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e0aff-168">Windows XP and later.</span></span><br />
<span data-ttu-id="e0aff-169">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="e0aff-169">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="e0aff-170">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e0aff-170">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0aff-171"><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></span><span class="sxs-lookup"><span data-stu-id="e0aff-171"><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></span></span></td>
<td><span data-ttu-id="e0aff-172">Spécifie si le décodeur utilise le matériel d’accélération vidéo DirectX, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="e0aff-172">Specifies whether the decoder will use DirectX video acceleration hardware, if available.</span></span><br/> <dl> <span data-ttu-id="e0aff-173">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e0aff-173">Windows XP and later.</span></span><br />
<span data-ttu-id="e0aff-174">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="e0aff-174">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="e0aff-175">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="e0aff-175">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0aff-176"><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></span><span class="sxs-lookup"><span data-stu-id="e0aff-176"><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></span></span></td>
<td><span data-ttu-id="e0aff-177">Spécifie le niveau de puissance pour le décodeur.</span><span class="sxs-lookup"><span data-stu-id="e0aff-177">Specifies the power level for the decoder.</span></span><br/> <dl> <span data-ttu-id="e0aff-178">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e0aff-178">Windows 7.</span></span><br />
<span data-ttu-id="e0aff-179">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="e0aff-179">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="e0aff-180">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e0aff-180">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0aff-181"><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></span><span class="sxs-lookup"><span data-stu-id="e0aff-181"><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></span></span></td>
<td><span data-ttu-id="e0aff-182">Spécifie si le décodeur doit utiliser l’interpolation de frame.</span><span class="sxs-lookup"><span data-stu-id="e0aff-182">Specifies whether the decoder should use frame interpolation.</span></span><br/> <dl> <span data-ttu-id="e0aff-183">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e0aff-183">Windows XP and later.</span></span><br />
<span data-ttu-id="e0aff-184">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="e0aff-184">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="e0aff-185">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="e0aff-185">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0aff-186"><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></span><span class="sxs-lookup"><span data-stu-id="e0aff-186"><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></span></span></td>
<td><span data-ttu-id="e0aff-187">Spécifie si le décodeur prend en charge l’interpolation de frame.</span><span class="sxs-lookup"><span data-stu-id="e0aff-187">Specifies whether the decoder supports frame interpolation.</span></span><br/> <dl> <span data-ttu-id="e0aff-188">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e0aff-188">Windows XP and later.</span></span><br />
<span data-ttu-id="e0aff-189">Profil simple, profil principal, profil avancé, image</span><span class="sxs-lookup"><span data-stu-id="e0aff-189">Simple Profile, Main Profile, Advanced Profile, Image</span></span><br />
<span data-ttu-id="e0aff-190">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e0aff-190">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0aff-191"><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></span><span class="sxs-lookup"><span data-stu-id="e0aff-191"><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></span></span></td>
<td><span data-ttu-id="e0aff-192">Spécifie le nombre de threads que le décodeur utilisera.</span><span class="sxs-lookup"><span data-stu-id="e0aff-192">Specifies the number of threads that the decoder will use.</span></span><br/> <dl> <span data-ttu-id="e0aff-193">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e0aff-193">Windows Vista and later.</span></span><br />
<span data-ttu-id="e0aff-194">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="e0aff-194">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="e0aff-195">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e0aff-195">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0aff-196"><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></span><span class="sxs-lookup"><span data-stu-id="e0aff-196"><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></span></span></td>
<td><span data-ttu-id="e0aff-197">Spécifie le mode de traitement de la publication pour le décodeur.</span><span class="sxs-lookup"><span data-stu-id="e0aff-197">Specifies the post processing mode for the decoder.</span></span><br/> <dl> <span data-ttu-id="e0aff-198">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e0aff-198">Windows Vista and later.</span></span><br />
<span data-ttu-id="e0aff-199">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="e0aff-199">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="e0aff-200">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="e0aff-200">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0aff-201"><strong>g_wszWMVCNeedsDrain</strong></span><span class="sxs-lookup"><span data-stu-id="e0aff-201"><strong>g_wszWMVCNeedsDrain</strong></span></span></td>
<td><span data-ttu-id="e0aff-202">Spécifie si le décodeur doit être vidé.</span><span class="sxs-lookup"><span data-stu-id="e0aff-202">Specifies whether the decoder should be drained.</span></span><br/> <dl> <span data-ttu-id="e0aff-203">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e0aff-203">Windows 8</span></span><br />
<span data-ttu-id="e0aff-204">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e0aff-204">Read-only.</span></span><br />
</dl> <span data-ttu-id="e0aff-205">Cette propriété est utilisée par l’exécution du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e0aff-205">This property is used by the Windows Media Format runtime.</span></span> <span data-ttu-id="e0aff-206">Le type de propriété est <strong>VARIANT_BOOL</strong>.</span><span class="sxs-lookup"><span data-stu-id="e0aff-206">The property type is <strong>VARIANT_BOOL</strong>.</span></span> <span data-ttu-id="e0aff-207">Si la valeur est <strong>VARIANT_TRUE</strong>, le décodeur doit être vidé après une discontinuation.</span><span class="sxs-lookup"><span data-stu-id="e0aff-207">If the value is <strong>VARIANT_TRUE</strong>, the decoder should be drained after a discontinuity.</span></span> <span data-ttu-id="e0aff-208">Pour plus d’informations sur la vidange d’une table MFT, consultez <a href="basic-mft-processing-model.md">modèle de traitement MFT de base</a>.</span><span class="sxs-lookup"><span data-stu-id="e0aff-208">For more information about draining an MFT, see <a href="basic-mft-processing-model.md">Basic MFT Processing Model</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e0aff-209">Pour interroger cette propriété, utilisez l’interface <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e0aff-209">To query this property, use the <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> interface.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="e0aff-210">Notes</span><span class="sxs-lookup"><span data-stu-id="e0aff-210">Remarks</span></span>

<span data-ttu-id="e0aff-211">La résolution maximale autorisée par le décodeur Windows Media Video 9 est 4096x4096.</span><span class="sxs-lookup"><span data-stu-id="e0aff-211">The maximum resolution allowed by the Windows Media Video 9 decoder is 4096x4096.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0aff-212">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0aff-212">Requirements</span></span>



| <span data-ttu-id="e0aff-213">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0aff-213">Requirement</span></span> | <span data-ttu-id="e0aff-214">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0aff-214">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0aff-215">Client</span><span class="sxs-lookup"><span data-stu-id="e0aff-215">Client</span></span><br/> | <span data-ttu-id="e0aff-216">Windows XP, Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="e0aff-216">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="e0aff-217">En-tête</span><span class="sxs-lookup"><span data-stu-id="e0aff-217">Header</span></span><br/> | <dl> <span data-ttu-id="e0aff-218"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0aff-218"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="e0aff-219">DLL</span><span class="sxs-lookup"><span data-stu-id="e0aff-219">DLL</span></span><br/>    | <dl> <span data-ttu-id="e0aff-220"><dt>Wmvdecod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0aff-220"><dt>Wmvdecod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0aff-221">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0aff-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0aff-222">Objets codec</span><span class="sxs-lookup"><span data-stu-id="e0aff-222">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="e0aff-223">Implémentation du codec</span><span class="sxs-lookup"><span data-stu-id="e0aff-223">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 
