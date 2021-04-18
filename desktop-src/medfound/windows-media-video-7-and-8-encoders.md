---
description: L’encodeur Windows Media Video 7/8 implémente les versions précédentes de l’encodeur Windows Media Video.
ms.assetid: c4165614-b9ec-4216-b36c-f57bc05e3a8e
title: Windows Media Video encodeur 7/8 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5467d02681ef319a508f6f6581e1f3c0191950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543332"
---
# <a name="windows-media-video-78-encoder"></a><span data-ttu-id="24e67-103">Windows Media Video encodeur 7/8</span><span class="sxs-lookup"><span data-stu-id="24e67-103">Windows Media Video 7/8 Encoder</span></span>

<span data-ttu-id="24e67-104">L’encodeur Windows Media Video 7/8 implémente les versions précédentes de l’encodeur Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="24e67-104">The Windows Media Video 7/8 encoder implements previous versions of the Windows Media Video encoder.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="24e67-105">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="24e67-105">Class Identifier</span></span>

<span data-ttu-id="24e67-106">L’identificateur de classe (CLSID) de l’encodeur Windows Media Video 7/8 est **CLSID \_ CWMVXEncMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="24e67-106">The class identifier (CLSID) for the Windows Media Video 7/8 encoder is **CLSID\_CWMVXEncMediaObject**.</span></span> <span data-ttu-id="24e67-107">Vous pouvez créer une instance de l’encodeur en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="24e67-107">You can create an instance of the encoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="24e67-108">Interfaces</span><span class="sxs-lookup"><span data-stu-id="24e67-108">Interfaces</span></span>

<span data-ttu-id="24e67-109">Un objet encodeur vidéo expose l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) afin que l’objet puisse être utilisé en tant qu’objet de média DirectX (DMO) et expose l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="24e67-109">A video encoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="24e67-110">Un encodeur vidéo se comporte comme un DMO ou une table MFT en fonction des interfaces que vous obtenez et de la version de Windows en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="24e67-110">A video encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="24e67-111">Le tableau suivant présente les conditions dans lesquelles un encodeur vidéo se comporte comme un DMO ou une table MFT.</span><span class="sxs-lookup"><span data-stu-id="24e67-111">The following table shows the conditions under which a video encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="24e67-112">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="24e67-112">Operating system</span></span>            | <span data-ttu-id="24e67-113">Comportement de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="24e67-113">Encoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24e67-114">Windows XP</span><span class="sxs-lookup"><span data-stu-id="24e67-114">Windows XP</span></span>                  | <span data-ttu-id="24e67-115">Un encodeur vidéo Windows Media se comporte toujours comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="24e67-115">A Windows Media video encoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="24e67-116">Windows Vista et Windows 7</span><span class="sxs-lookup"><span data-stu-id="24e67-116">Windows Vista and Windows 7</span></span> | <span data-ttu-id="24e67-117">Par défaut, un encodeur vidéo Windows Media se comporte comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="24e67-117">By default, a Windows Media video encoder behaves as a DMO.</span></span> <span data-ttu-id="24e67-118">Si vous obtenez une interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) sur un encodeur vidéo, elle se comporte comme une table MFT.</span><span class="sxs-lookup"><span data-stu-id="24e67-118">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video encoder, it behaves as an MFT.</span></span> |



 

## <a name="input-formats"></a><span data-ttu-id="24e67-119">Formats d’entrée</span><span class="sxs-lookup"><span data-stu-id="24e67-119">Input Formats</span></span>

<span data-ttu-id="24e67-120">L’encodeur Windows Media Video prend en charge les sous-types de médias d’entrée suivants lorsqu’il agit en tant que DMO.</span><span class="sxs-lookup"><span data-stu-id="24e67-120">The Windows Media Video encoder supports the following input media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="24e67-121">MEDIASUBTYPE \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="24e67-121">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="24e67-122">MEDIASUBTYPE \_ I420</span><span class="sxs-lookup"><span data-stu-id="24e67-122">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="24e67-123">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="24e67-123">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="24e67-124">MEDIASUBTYPE \_ NV11</span><span class="sxs-lookup"><span data-stu-id="24e67-124">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="24e67-125">MEDIASUBTYPE \_ NV12</span><span class="sxs-lookup"><span data-stu-id="24e67-125">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="24e67-126">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="24e67-126">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="24e67-127">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="24e67-127">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="24e67-128">MEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="24e67-128">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="24e67-129">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="24e67-129">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="24e67-130">MEDIASUBTYPE \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="24e67-130">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="24e67-131">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="24e67-131">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="24e67-132">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="24e67-132">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="24e67-133">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="24e67-133">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="24e67-134">photomotion MEDIASUBTYPE \_</span><span class="sxs-lookup"><span data-stu-id="24e67-134">MEDIASUBTYPE\_PHOTOMOTION</span></span>

<span data-ttu-id="24e67-135">L’encodeur Windows Media Video prend en charge les sous-types de médias d’entrée suivants lorsqu’il joue le rôle de MFT.</span><span class="sxs-lookup"><span data-stu-id="24e67-135">The Windows Media Video encoder supports the following input media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="24e67-136">MFVideoFormat \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="24e67-136">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="24e67-137">MFVideoFormat \_ I420</span><span class="sxs-lookup"><span data-stu-id="24e67-137">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="24e67-138">MFVideoFormat \_ YV12</span><span class="sxs-lookup"><span data-stu-id="24e67-138">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="24e67-139">MFVideoFormat \_ NV11</span><span class="sxs-lookup"><span data-stu-id="24e67-139">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="24e67-140">MFVideoFormat \_ NV12</span><span class="sxs-lookup"><span data-stu-id="24e67-140">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="24e67-141">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="24e67-141">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="24e67-142">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="24e67-142">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="24e67-143">MFVideoFormat \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="24e67-143">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="24e67-144">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="24e67-144">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="24e67-145">MFVideoFormat \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="24e67-145">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="24e67-146">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="24e67-146">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="24e67-147">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="24e67-147">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="24e67-148">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="24e67-148">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="24e67-149">photomotion MEDIASUBTYPE \_</span><span class="sxs-lookup"><span data-stu-id="24e67-149">MEDIASUBTYPE\_PHOTOMOTION</span></span>

## <a name="output-formats"></a><span data-ttu-id="24e67-150">Formats de sortie</span><span class="sxs-lookup"><span data-stu-id="24e67-150">Output Formats</span></span>

<span data-ttu-id="24e67-151">Le tableau suivant présente les codes à quatre caractères (FOURCCs) pour les types de sortie pris en charge par l’encodeur Windows Media Video 7/8.</span><span class="sxs-lookup"><span data-stu-id="24e67-151">The following table shows the four-character codes (FOURCCs) for the output types supported by the Windows Media Video 7/8 encoder.</span></span>



| <span data-ttu-id="24e67-152">Category</span><span class="sxs-lookup"><span data-stu-id="24e67-152">Category</span></span>              | <span data-ttu-id="24e67-153">FOURCC</span><span class="sxs-lookup"><span data-stu-id="24e67-153">FOURCC</span></span> |
|-----------------------|--------|
| <span data-ttu-id="24e67-154">Windows Media Video 7</span><span class="sxs-lookup"><span data-stu-id="24e67-154">Windows Media Video 7</span></span> | <span data-ttu-id="24e67-155">"WMV1"</span><span class="sxs-lookup"><span data-stu-id="24e67-155">"WMV1"</span></span> |
| <span data-ttu-id="24e67-156">Windows Media Video 8</span><span class="sxs-lookup"><span data-stu-id="24e67-156">Windows Media Video 8</span></span> | <span data-ttu-id="24e67-157">"WMV2"</span><span class="sxs-lookup"><span data-stu-id="24e67-157">"WMV2"</span></span> |



 

## <a name="properties"></a><span data-ttu-id="24e67-158">Propriétés</span><span class="sxs-lookup"><span data-stu-id="24e67-158">Properties</span></span>

<span data-ttu-id="24e67-159">L’encodeur Windows Media Video 7/8 prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="24e67-159">The Windows Media Video 7/8 encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="24e67-160">Propriété</span><span class="sxs-lookup"><span data-stu-id="24e67-160">Property</span></span></th>
<th><span data-ttu-id="24e67-161">Description</span><span class="sxs-lookup"><span data-stu-id="24e67-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="24e67-162"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-162"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="24e67-163">Spécifie la surcharge, en octets par paquet, requise pour le conteneur utilisé pour stocker le contenu compressé.</span><span class="sxs-lookup"><span data-stu-id="24e67-163">Specifies the overhead, in bytes per packet, required for the container used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="24e67-164">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-164">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-165">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="24e67-165">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24e67-166"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-166"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="24e67-167">Spécifie la fréquence d’images moyenne du contenu vidéo, en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="24e67-167">Specifies the average frame rate of video content, in frames per second.</span></span><br/> <dl> <span data-ttu-id="24e67-168">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-168">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-169">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="24e67-169">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24e67-170"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-170"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="24e67-171">Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) contraints à sa vitesse de transmission moyenne (spécifiée par <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="24e67-171">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span></span><br/> <dl> <span data-ttu-id="24e67-172">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-172">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-173">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="24e67-173">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24e67-174"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-174"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="24e67-175">Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) avec restriction à sa vitesse de transmission maximale (spécifiée par <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="24e67-175">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span></span><br/> <dl> <span data-ttu-id="24e67-176">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-176">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-177">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="24e67-177">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24e67-178"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-178"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span></span></td>
<td><span data-ttu-id="24e67-179">Spécifie si le flux de bits vidéo encodé contient une valeur de saturation de la mémoire tampon avec chaque image clé.</span><span class="sxs-lookup"><span data-stu-id="24e67-179">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="24e67-180">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-180">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-181">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="24e67-181">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24e67-182"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-182"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="24e67-183">Spécifie le nombre de trames vidéo encodées par le codec.</span><span class="sxs-lookup"><span data-stu-id="24e67-183">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="24e67-184">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-184">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-185">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="24e67-185">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24e67-186"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-186"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="24e67-187">Spécifie le nombre de trames vidéo encodées par le codec qui contiennent réellement des données.</span><span class="sxs-lookup"><span data-stu-id="24e67-187">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="24e67-188">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-188">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-189">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="24e67-189">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24e67-190"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-190"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="24e67-191">Cette propriété est remplacée par <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="24e67-191">This property is superseded by <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24e67-192"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-192"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span></span></td>
<td><span data-ttu-id="24e67-193">Spécifie la complexité de l’algorithme d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="24e67-193">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="24e67-194">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-194">Windows Vista and later.</span></span><br />
<span data-ttu-id="24e67-195">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="24e67-195">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24e67-196"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-196"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span></span></td>
<td><span data-ttu-id="24e67-197">Spécifie une représentation numérique du compromis entre le lissage du mouvement et la qualité de l’image dans la sortie du codec.</span><span class="sxs-lookup"><span data-stu-id="24e67-197">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="24e67-198">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-198">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-199">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="24e67-199">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24e67-200"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-200"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="24e67-201">Spécifie le modèle de conformité de périphérique auquel le contenu encodé est conforme.</span><span class="sxs-lookup"><span data-stu-id="24e67-201">Specifies the device conformance template to which the encoded content conforms.</span></span><br/> <dl> <span data-ttu-id="24e67-202">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-202">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-203">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="24e67-203">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24e67-204"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-204"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span></span></td>
<td><span data-ttu-id="24e67-205">Spécifie le modèle de conformité de périphérique que vous souhaitez utiliser pour l’encodage vidéo.</span><span class="sxs-lookup"><span data-stu-id="24e67-205">Specifies the device conformance template that you want to use for video encoding.</span></span><br/> <dl> <span data-ttu-id="24e67-206">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-206">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-207">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="24e67-207">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24e67-208"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-208"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="24e67-209">Spécifie le nombre de trames vidéo supprimées pendant l’encodage.</span><span class="sxs-lookup"><span data-stu-id="24e67-209">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="24e67-210">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-210">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-211">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="24e67-211">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24e67-212"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-212"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="24e67-213">Spécifie la fin d’une passe d’encodage.</span><span class="sxs-lookup"><span data-stu-id="24e67-213">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="24e67-214">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-214">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-215">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="24e67-215">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24e67-216"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-216"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span></span></td>
<td><span data-ttu-id="24e67-217">Spécifie le FOURCC qui identifie l’encodeur que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="24e67-217">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="24e67-218">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-218">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-219">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="24e67-219">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24e67-220"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-220"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span></span></td>
<td><span data-ttu-id="24e67-221">Spécifie si la sortie du codec sera entrelacée.</span><span class="sxs-lookup"><span data-stu-id="24e67-221">Specifies whether the codec output will be interlaced.</span></span><br/> <dl> <span data-ttu-id="24e67-222">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-222">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-223">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="24e67-223">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24e67-224"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-224"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span></span></td>
<td><span data-ttu-id="24e67-225">Spécifie la durée maximale, en millisecondes, entre les images clés de la sortie du codec.</span><span class="sxs-lookup"><span data-stu-id="24e67-225">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="24e67-226">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-226">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-227">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="24e67-227">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24e67-228"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-228"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="24e67-229">Spécifie le nombre maximal de passes prises en charge par le codec.</span><span class="sxs-lookup"><span data-stu-id="24e67-229">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="24e67-230">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-230">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-231">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="24e67-231">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24e67-232"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-232"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="24e67-233">Spécifie le nombre de passes qui seront utilisées par le codec pour encoder le contenu.</span><span class="sxs-lookup"><span data-stu-id="24e67-233">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="24e67-234">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-234">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-235">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="24e67-235">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24e67-236"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-236"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="24e67-237">Spécifie si l’encodeur génère des entrées de frame factice dans le flux binaire pour les frames en double.</span><span class="sxs-lookup"><span data-stu-id="24e67-237">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span><br/> <dl> <span data-ttu-id="24e67-238">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-238">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-239">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="24e67-239">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24e67-240"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-240"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="24e67-241">Spécifie QP.</span><span class="sxs-lookup"><span data-stu-id="24e67-241">Specifies QP.</span></span><br/> <dl> <span data-ttu-id="24e67-242">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-242">Windows Vista and later.</span></span><br />
<span data-ttu-id="24e67-243">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="24e67-243">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24e67-244"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-244"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="24e67-245">Spécifie la vitesse de transmission moyenne, en bits par seconde, utilisée pour l’encodage VBR (variable-bit-rate) à 2 passes.</span><span class="sxs-lookup"><span data-stu-id="24e67-245">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="24e67-246">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-246">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-247">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="24e67-247">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24e67-248"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-248"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="24e67-249">Spécifie le taux de bits de pointe, en bits par seconde, utilisé pour le VBR (variable-bit-bit-rate) avec une limite de 2 passes.</span><span class="sxs-lookup"><span data-stu-id="24e67-249">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR).</span></span><br/> <dl> <span data-ttu-id="24e67-250">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-250">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-251">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="24e67-251">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24e67-252"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-252"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="24e67-253">Spécifie le nombre de trames vidéo transmises à l’encodeur pendant le processus d’encodage.</span><span class="sxs-lookup"><span data-stu-id="24e67-253">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="24e67-254">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-254">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-255">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="24e67-255">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24e67-256"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-256"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="24e67-257">Spécifie si le codec utilise l’encodage VBR (variable-bit-rate).</span><span class="sxs-lookup"><span data-stu-id="24e67-257">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="24e67-258">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-258">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-259">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="24e67-259">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24e67-260"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-260"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="24e67-261">Spécifie le niveau de qualité réel pour l’encodage VBR (variable-bit-rate) basé sur la qualité (1 passe).</span><span class="sxs-lookup"><span data-stu-id="24e67-261">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="24e67-262">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-262">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-263">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="24e67-263">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24e67-264"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-264"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span></span></td>
<td><span data-ttu-id="24e67-265">Spécifie la quantité de contenu, en millisecondes, qui peut tenir dans la mémoire tampon du modèle.</span><span class="sxs-lookup"><span data-stu-id="24e67-265">Specifies the amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="24e67-266">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-266">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-267">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="24e67-267">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24e67-268"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e67-268"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="24e67-269">Spécifie le nombre de trames vidéo qui ont été ignorées, car il s’agissait de doublons de trames précédentes.</span><span class="sxs-lookup"><span data-stu-id="24e67-269">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="24e67-270">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24e67-270">Windows XP and later.</span></span><br />
<span data-ttu-id="24e67-271">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="24e67-271">Read-only</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="24e67-272">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24e67-272">Requirements</span></span>



| <span data-ttu-id="24e67-273">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24e67-273">Requirement</span></span> | <span data-ttu-id="24e67-274">Valeur</span><span class="sxs-lookup"><span data-stu-id="24e67-274">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24e67-275">Client</span><span class="sxs-lookup"><span data-stu-id="24e67-275">Client</span></span><br/> | <span data-ttu-id="24e67-276">Windows XP, Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="24e67-276">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="24e67-277">En-tête</span><span class="sxs-lookup"><span data-stu-id="24e67-277">Header</span></span><br/> | <dl> <span data-ttu-id="24e67-278"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="24e67-278"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="24e67-279">DLL</span><span class="sxs-lookup"><span data-stu-id="24e67-279">DLL</span></span><br/>    | <dl> <span data-ttu-id="24e67-280"><dt>Wmvxencd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24e67-280"><dt>Wmvxencd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24e67-281">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24e67-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24e67-282">Objets codec</span><span class="sxs-lookup"><span data-stu-id="24e67-282">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="24e67-283">Implémentation du codec</span><span class="sxs-lookup"><span data-stu-id="24e67-283">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="24e67-284">GUID de sous-type de vidéo</span><span class="sxs-lookup"><span data-stu-id="24e67-284">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 
