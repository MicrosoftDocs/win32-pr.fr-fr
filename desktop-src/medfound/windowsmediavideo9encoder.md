---
description: L’encodeur Windows Media Video 9 encode les flux vidéo.
ms.assetid: 1d0a41bc-7f7c-4e25-860c-1108ab292951
title: Encodeur Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c36ee5823c585d60ee74e75f99e8ec9b4d91f5cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537833"
---
# <a name="windows-media-video-9-encoder"></a><span data-ttu-id="d00a8-103">Encodeur Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="d00a8-103">Windows Media Video 9 Encoder</span></span>

<span data-ttu-id="d00a8-104">L’encodeur Windows Media Video 9 encode les flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="d00a8-104">The Windows Media Video 9 encoder encodes video streams.</span></span> <span data-ttu-id="d00a8-105">L’encodeur prend en charge les quatre catégories de sortie encodées suivantes.</span><span class="sxs-lookup"><span data-stu-id="d00a8-105">The encoder supports the following four categories of encoded output.</span></span>

-   <span data-ttu-id="d00a8-106">Profil simple Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="d00a8-106">Windows Media Video 9 Simple Profile</span></span>
-   <span data-ttu-id="d00a8-107">Profil principal du Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="d00a8-107">Windows Media Video 9 Main Profile</span></span>
-   <span data-ttu-id="d00a8-108">Profil avancé Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="d00a8-108">Windows Media Video 9 Advanced Profile</span></span>
-   <span data-ttu-id="d00a8-109">Image Windows Media Video 9,1</span><span class="sxs-lookup"><span data-stu-id="d00a8-109">Windows Media Video 9.1 Image</span></span>

## <a name="class-identifier"></a><span data-ttu-id="d00a8-110">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="d00a8-110">Class Identifier</span></span>

<span data-ttu-id="d00a8-111">L’identificateur de classe (CLSID) de l’encodeur de Windows Media Video est représenté par la constante **CLSID \_ CWMV9EncMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="d00a8-111">The class identifier (CLSID) for the Windows Media Video encoder is represented by the constant **CLSID\_CWMV9EncMediaObject**.</span></span> <span data-ttu-id="d00a8-112">Vous pouvez créer une instance de l’encodeur vidéo en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="d00a8-112">You can create an instance of the video encoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="d00a8-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="d00a8-113">Interfaces</span></span>

<span data-ttu-id="d00a8-114">Un objet encodeur vidéo expose l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) afin que l’objet puisse être utilisé en tant qu’objet de média DirectX (DMO) et expose l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="d00a8-114">A video encoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="d00a8-115">Un encodeur vidéo se comporte comme un DMO ou une table MFT en fonction des interfaces que vous obtenez et de la version de Windows en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d00a8-115">A video encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="d00a8-116">Le tableau suivant présente les conditions dans lesquelles un encodeur vidéo se comporte comme un DMO ou une table MFT.</span><span class="sxs-lookup"><span data-stu-id="d00a8-116">The following table shows the conditions under which a video encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="d00a8-117">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="d00a8-117">Operating system</span></span>            | <span data-ttu-id="d00a8-118">Comportement de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="d00a8-118">Encoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d00a8-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d00a8-119">Windows XP</span></span>                  | <span data-ttu-id="d00a8-120">Un encodeur vidéo Windows Media se comporte toujours comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="d00a8-120">A Windows Media video encoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="d00a8-121">Windows Vista et Windows 7</span><span class="sxs-lookup"><span data-stu-id="d00a8-121">Windows Vista and Windows 7</span></span> | <span data-ttu-id="d00a8-122">Par défaut, un encodeur vidéo Windows Media se comporte comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="d00a8-122">By default, a Windows Media video encoder behaves as a DMO.</span></span> <span data-ttu-id="d00a8-123">Si vous obtenez une interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) sur un encodeur vidéo, elle se comporte comme une table MFT.</span><span class="sxs-lookup"><span data-stu-id="d00a8-123">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video encoder, it behaves as an MFT.</span></span> |



 

## <a name="input-formats"></a><span data-ttu-id="d00a8-124">Formats d’entrée</span><span class="sxs-lookup"><span data-stu-id="d00a8-124">Input Formats</span></span>

<span data-ttu-id="d00a8-125">L’encodeur Windows Media Video prend en charge les sous-types de médias d’entrée suivants lorsqu’il agit en tant que DMO.</span><span class="sxs-lookup"><span data-stu-id="d00a8-125">The Windows Media Video encoder supports the following input media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="d00a8-126">MEDIASUBTYPE \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="d00a8-126">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="d00a8-127">MEDIASUBTYPE \_ I420</span><span class="sxs-lookup"><span data-stu-id="d00a8-127">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="d00a8-128">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="d00a8-128">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="d00a8-129">MEDIASUBTYPE \_ NV11</span><span class="sxs-lookup"><span data-stu-id="d00a8-129">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="d00a8-130">MEDIASUBTYPE \_ NV12</span><span class="sxs-lookup"><span data-stu-id="d00a8-130">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="d00a8-131">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="d00a8-131">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="d00a8-132">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="d00a8-132">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="d00a8-133">MEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="d00a8-133">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="d00a8-134">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="d00a8-134">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="d00a8-135">MEDIASUBTYPE \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="d00a8-135">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="d00a8-136">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="d00a8-136">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="d00a8-137">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="d00a8-137">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="d00a8-138">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="d00a8-138">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="d00a8-139">photomotion MEDIASUBTYPE \_</span><span class="sxs-lookup"><span data-stu-id="d00a8-139">MEDIASUBTYPE\_PHOTOMOTION</span></span>

<span data-ttu-id="d00a8-140">L’encodeur Windows Media Video prend en charge les sous-types de médias d’entrée suivants lorsqu’il joue le rôle de MFT.</span><span class="sxs-lookup"><span data-stu-id="d00a8-140">The Windows Media Video encoder supports the following input media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="d00a8-141">MFVideoFormat \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="d00a8-141">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="d00a8-142">MFVideoFormat \_ I420</span><span class="sxs-lookup"><span data-stu-id="d00a8-142">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="d00a8-143">MFVideoFormat \_ YV12</span><span class="sxs-lookup"><span data-stu-id="d00a8-143">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="d00a8-144">MFVideoFormat \_ NV11</span><span class="sxs-lookup"><span data-stu-id="d00a8-144">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="d00a8-145">MFVideoFormat \_ NV12</span><span class="sxs-lookup"><span data-stu-id="d00a8-145">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="d00a8-146">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="d00a8-146">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="d00a8-147">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="d00a8-147">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="d00a8-148">MFVideoFormat \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="d00a8-148">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="d00a8-149">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="d00a8-149">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="d00a8-150">MFVideoFormat \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="d00a8-150">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="d00a8-151">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="d00a8-151">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="d00a8-152">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="d00a8-152">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="d00a8-153">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="d00a8-153">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="d00a8-154">photomotion MEDIASUBTYPE \_</span><span class="sxs-lookup"><span data-stu-id="d00a8-154">MEDIASUBTYPE\_PHOTOMOTION</span></span>

## <a name="output-formats"></a><span data-ttu-id="d00a8-155">Formats de sortie</span><span class="sxs-lookup"><span data-stu-id="d00a8-155">Output Formats</span></span>

<span data-ttu-id="d00a8-156">Le tableau suivant présente les codes à quatre caractères (FOURCCs) qui correspondent aux catégories de sortie encodée.</span><span class="sxs-lookup"><span data-stu-id="d00a8-156">The following table shows the four-character codes (FOURCCs) that correspond to the categories of encoded output.</span></span>



| <span data-ttu-id="d00a8-157">Category</span><span class="sxs-lookup"><span data-stu-id="d00a8-157">Category</span></span>                               | <span data-ttu-id="d00a8-158">FOURCC</span><span class="sxs-lookup"><span data-stu-id="d00a8-158">FOURCC</span></span>                                   |
|----------------------------------------|------------------------------------------|
| <span data-ttu-id="d00a8-159">Profil simple Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="d00a8-159">Windows Media Video 9 Simple Profile</span></span>   | <span data-ttu-id="d00a8-160">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="d00a8-160">"WMV3"</span></span>                                   |
| <span data-ttu-id="d00a8-161">Profil principal du Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="d00a8-161">Windows Media Video 9 Main Profile</span></span>     | <span data-ttu-id="d00a8-162">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="d00a8-162">"WMV3"</span></span>                                   |
| <span data-ttu-id="d00a8-163">Profil avancé Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="d00a8-163">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="d00a8-164">"WVC1"</span><span class="sxs-lookup"><span data-stu-id="d00a8-164">"WVC1"</span></span>                                   |
| <span data-ttu-id="d00a8-165">Image Windows Media Video 9,1</span><span class="sxs-lookup"><span data-stu-id="d00a8-165">Windows Media Video 9.1 Image</span></span>          | <span data-ttu-id="d00a8-166">« WMVP » pour 9,1, « WVP2 » pour 9,1 version 2</span><span class="sxs-lookup"><span data-stu-id="d00a8-166">"WMVP" for 9.1, "WVP2" for 9.1 version 2</span></span> |



 

<span data-ttu-id="d00a8-167">Pour faire la distinction entre profil simple et profil principal, définissez la propriété [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="d00a8-167">To distinguish between Simple Profile and Main Profile, set the [**MFPKEY\_DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) property.</span></span>

## <a name="properties"></a><span data-ttu-id="d00a8-168">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d00a8-168">Properties</span></span>

<span data-ttu-id="d00a8-169">L’encodeur Windows Media Video 9 prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d00a8-169">The Windows Media Video 9 encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d00a8-170">Propriété</span><span class="sxs-lookup"><span data-stu-id="d00a8-170">Property</span></span></th>
<th><span data-ttu-id="d00a8-171">Description</span><span class="sxs-lookup"><span data-stu-id="d00a8-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d00a8-172"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-172"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-173">Spécifie la surcharge, en octets par paquet, requise pour le conteneur utilisé pour stocker le contenu compressé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-173">Specifies the overhead, in bytes per packet, required for the container used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="d00a8-174">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-174">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-175">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="d00a8-175">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="d00a8-176">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-177"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-177"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-178">Spécifie la fréquence d’images moyenne du contenu vidéo, en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="d00a8-178">Specifies the average frame rate of video content, in frames per second.</span></span><br/> <dl> <span data-ttu-id="d00a8-179">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-179">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-180">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="d00a8-180">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="d00a8-181">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-181">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-182"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-182"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-183">Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) contraints à sa vitesse de transmission moyenne (spécifiée par <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="d00a8-183">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span></span><br/> <dl> <span data-ttu-id="d00a8-184">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-184">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-185">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-185">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-186">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d00a8-186">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-187"><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-187"><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-188">Spécifie l’augmentation Delta entre le quantificateur d’image du frame d’ancrage et le quantificateur d’image du cadre B.</span><span class="sxs-lookup"><span data-stu-id="d00a8-188">Specifies the delta increase between the picture quantizer of the anchor frame and the picture quantizer of the B-frame.</span></span><br/> <dl> <span data-ttu-id="d00a8-189">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-189">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-190">Profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-190">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-191">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-191">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-192"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-192"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-193">Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) avec restriction à sa vitesse de transmission maximale (spécifiée par <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="d00a8-193">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span></span><br/> <dl> <span data-ttu-id="d00a8-194">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-194">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-195">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="d00a8-195">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="d00a8-196">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d00a8-196">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-197"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-197"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-198">Spécifie si le flux de bits vidéo encodé contient une valeur de saturation de la mémoire tampon avec chaque image clé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-198">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="d00a8-199">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-199">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-200">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-200">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-201">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-201">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-202"><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-202"><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-203">Spécifie le modèle d’encodage à utiliser au début d’un groupe d’images.</span><span class="sxs-lookup"><span data-stu-id="d00a8-203">Specifies the encoding pattern to use at the beginning of a group of pictures.</span></span><br/> <dl> <span data-ttu-id="d00a8-204">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-204">Windows Vista and later.</span></span><br />
<span data-ttu-id="d00a8-205">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="d00a8-205">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="d00a8-206">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-206">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-207"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-207"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-208">Spécifie le nombre de trames vidéo encodées par le codec.</span><span class="sxs-lookup"><span data-stu-id="d00a8-208">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="d00a8-209">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-209">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-210">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-210">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-211">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-211">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-212"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-212"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-213">Spécifie le nombre de trames vidéo encodées par le codec qui contiennent réellement des données.</span><span class="sxs-lookup"><span data-stu-id="d00a8-213">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="d00a8-214">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-214">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-215">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-215">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-216">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-216">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-217"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-217"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-218">Cette propriété est remplacée par <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d00a8-218">This property is superseded by <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-219"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-219"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-220">Spécifie la complexité de l’algorithme d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="d00a8-220">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="d00a8-221">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-221">Windows Vista and later.</span></span><br />
<span data-ttu-id="d00a8-222">Profil simple, profil principal.</span><span class="sxs-lookup"><span data-stu-id="d00a8-222">Simple Profile, Main Profile.</span></span> <span data-ttu-id="d00a8-223">Profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-223">Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-224">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-224">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-225"><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-225"><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-226">Spécifie le type d’optimisation à utiliser pour le codec de profil avancé Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="d00a8-226">Specifies the type of optimization to use for the Windows Media Video 9 Advanced Profile codec.</span></span><br/> <dl> <span data-ttu-id="d00a8-227">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-227">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-228">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-228">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-229">Écriture.</span><span class="sxs-lookup"><span data-stu-id="d00a8-229">Write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-230"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-230"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-231">Spécifie une représentation numérique du compromis entre le lissage du mouvement et la qualité de l’image dans la sortie du codec.</span><span class="sxs-lookup"><span data-stu-id="d00a8-231">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="d00a8-232">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-232">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-233">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-233">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-234">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-234">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-235"><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-235"><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-236">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-236">Not used.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-237"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-237"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-238">Spécifie le modèle de conformité de périphérique auquel le contenu encodé est conforme.</span><span class="sxs-lookup"><span data-stu-id="d00a8-238">Specifies the device conformance template to which the encoded content conforms.</span></span><br/> <dl> <span data-ttu-id="d00a8-239">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-239">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-240">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="d00a8-240">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="d00a8-241">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-241">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-242"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-242"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-243">Spécifie le modèle de conformité de périphérique que vous souhaitez utiliser pour l’encodage vidéo.</span><span class="sxs-lookup"><span data-stu-id="d00a8-243">Specifies the device conformance template that you want to use for video encoding.</span></span><br/> <dl> <span data-ttu-id="d00a8-244">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-244">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-245">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-245">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-246">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-246">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-247"><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-247"><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-248">Spécifie la méthode utilisée pour encoder les informations de vecteur de mouvement.</span><span class="sxs-lookup"><span data-stu-id="d00a8-248">Specifies the method used to encode the motion vector information.</span></span><br/> <dl> <span data-ttu-id="d00a8-249">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-249">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-250">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-250">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-251">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-251">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-252"><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-252"><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-253">Spécifie si le codec doit utiliser le filtre de bruit lors de l’encodage.</span><span class="sxs-lookup"><span data-stu-id="d00a8-253">Specifies whether the codec will use the noise filter when encoding.</span></span><br/> <dl> <span data-ttu-id="d00a8-254">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-254">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-255">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-255">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-256">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-256">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-257"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-257"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-258">Spécifie le niveau de qualité souhaité pour l’encodage VBR (variable-bit-rate) basé sur la qualité (1 passe).</span><span class="sxs-lookup"><span data-stu-id="d00a8-258">Specifies the desired quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="d00a8-259">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-259">Windows Vista and later.</span></span><br />
<span data-ttu-id="d00a8-260">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="d00a8-260">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="d00a8-261">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-261">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-262"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-262"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-263">Spécifie le nombre de trames vidéo supprimées pendant l’encodage.</span><span class="sxs-lookup"><span data-stu-id="d00a8-263">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="d00a8-264">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-264">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-265">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-265">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-266">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-266">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-267"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-267"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-268">Spécifie la fin d’une passe d’encodage.</span><span class="sxs-lookup"><span data-stu-id="d00a8-268">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="d00a8-269">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-269">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-270">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-270">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-271">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-271">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-272"><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-272"><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-273">Spécifie une hauteur de frame intermédiaire pour la vidéo encodée.</span><span class="sxs-lookup"><span data-stu-id="d00a8-273">Specifies an intermediate frame height for encoded video.</span></span><br/> <dl> <span data-ttu-id="d00a8-274">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-274">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-275">Profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-275">Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-276">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-276">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-277"><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-277"><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-278">Spécifie une largeur de frame intermédiaire pour la vidéo encodée.</span><span class="sxs-lookup"><span data-stu-id="d00a8-278">Specifies an intermediate frame width for encoded video.</span></span><br/> <dl> <span data-ttu-id="d00a8-279">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-279">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-280">Profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-280">Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-281">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-281">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-282"><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-282"><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-283">Spécifie si le codec doit utiliser le filtrage médian pendant l’encodage.</span><span class="sxs-lookup"><span data-stu-id="d00a8-283">Specifies whether the codec should use median filtering during encoding.</span></span><br/> <dl> <span data-ttu-id="d00a8-284">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-284">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-285">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-285">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-286">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-286">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-287"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-287"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-288">Spécifie le FOURCC qui identifie l’encodeur que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="d00a8-288">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="d00a8-289">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-289">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-290">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="d00a8-290">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="d00a8-291">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-291">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-292"><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-292"><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-293">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="d00a8-293">Obsolete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-294"><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-294"><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-295">Spécifie si l’encodeur est autorisé à déposer des frames.</span><span class="sxs-lookup"><span data-stu-id="d00a8-295">Specifies whether the encoder is allowed to drop frames.</span></span><br/> <dl> <span data-ttu-id="d00a8-296">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-296">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-297">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="d00a8-297">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="d00a8-298">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-298">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-299"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-299"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-300">Spécifie si la sortie du codec sera entrelacée.</span><span class="sxs-lookup"><span data-stu-id="d00a8-300">Specifies whether the codec output will be interlaced.</span></span><br/> <dl> <span data-ttu-id="d00a8-301">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-301">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-302">Profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-302">Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-303">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-303">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-304"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-304"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-305">Spécifie la durée maximale, en millisecondes, entre les images clés de la sortie du codec.</span><span class="sxs-lookup"><span data-stu-id="d00a8-305">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="d00a8-306">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-306">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-307">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="d00a8-307">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="d00a8-308">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-308">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-309"><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-309"><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-310">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-310">Not used.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-311"><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-311"><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-312">Spécifie le nombre de frames après le frame actuel que le codec évaluera avant d’encoder le frame actuel.</span><span class="sxs-lookup"><span data-stu-id="d00a8-312">Specifies the number of frames after the current frame that the codec will evaluate before encoding the current frame.</span></span><br/> <dl> <span data-ttu-id="d00a8-313">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-313">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-314">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-314">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-315">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-315">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-316"><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-316"><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-317">Spécifie si le codec doit utiliser le filtre de déblocage en boucle lors de l’encodage.</span><span class="sxs-lookup"><span data-stu-id="d00a8-317">Specifies whether the codec should use the in-loop deblocking filter during encoding.</span></span><br/> <dl> <span data-ttu-id="d00a8-318">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-318">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-319">Profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-319">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-320">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-320">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-321"><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-321"><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-322">Spécifie la méthode de coût utilisée par le codec pour déterminer le mode bloc macro à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d00a8-322">Specifies the cost method used by the codec to determine which macroblock mode to use.</span></span><br/> <dl> <span data-ttu-id="d00a8-323">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-323">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-324">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-324">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-325">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-325">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-326"><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-326"><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-327">Spécifie la méthode à utiliser pour la correspondance de mouvement.</span><span class="sxs-lookup"><span data-stu-id="d00a8-327">Specifies the method to use for motion matching.</span></span><br/> <dl> <span data-ttu-id="d00a8-328">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-328">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-329">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-329">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-330">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-330">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-331"><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-331"><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-332">Spécifie les types d’informations vidéo utilisées dans les opérations de recherche de mouvement.</span><span class="sxs-lookup"><span data-stu-id="d00a8-332">Specifies the types of video information that are used in motion search operations.</span></span><br/> <dl> <span data-ttu-id="d00a8-333">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-333">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-334">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-334">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-335">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-335">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-336"><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-336"><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-337">Spécifie la plage utilisée dans les recherches de mouvement.</span><span class="sxs-lookup"><span data-stu-id="d00a8-337">Specifies the range used in motion searches.</span></span><br/> <dl> <span data-ttu-id="d00a8-338">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-338">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-339">Profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-339">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-340">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-340">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-341"><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-341"><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-342">Spécifie si le codec doit tenter de détecter les bords bruyants du cadre et les supprimer.</span><span class="sxs-lookup"><span data-stu-id="d00a8-342">Specifies whether the codec should attempt to detect noisy frame edges and remove them.</span></span><br/> <dl> <span data-ttu-id="d00a8-343">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-343">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-344">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-344">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-345">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-345">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-346"><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-346"><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-347">Spécifie le nombre de frames prédictifs bidirectionnels (frames B).</span><span class="sxs-lookup"><span data-stu-id="d00a8-347">Specifies the number of bidirectional predictive frames (B-frames).</span></span><br/> <dl> <span data-ttu-id="d00a8-348">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-348">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-349">Profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-349">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-350">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-350">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-351"><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-351"><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-352">Spécifie le nombre de threads que le codec doit utiliser pour l’encodage.</span><span class="sxs-lookup"><span data-stu-id="d00a8-352">Specifies the number of threads that the codec will use for encoding.</span></span><br/> <dl> <span data-ttu-id="d00a8-353">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-353">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-354">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-354">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-355">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-355">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-356"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-356"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-357">Spécifie le nombre maximal de passes prises en charge par le codec.</span><span class="sxs-lookup"><span data-stu-id="d00a8-357">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="d00a8-358">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-358">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-359">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="d00a8-359">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="d00a8-360">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-360">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-361"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-361"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-362">Spécifie le nombre de passes qui seront utilisées par le codec pour encoder le contenu.</span><span class="sxs-lookup"><span data-stu-id="d00a8-362">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="d00a8-363">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-363">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-364">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="d00a8-364">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="d00a8-365">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d00a8-365">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-366"><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-366"><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-367">Spécifie si le codec doit utiliser l’optimisation de perception conservatrice lors de l’encodage.</span><span class="sxs-lookup"><span data-stu-id="d00a8-367">Specifies whether the codec should use conservative perceptual optimization when encoding.</span></span><br/> <dl> <span data-ttu-id="d00a8-368">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-368">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-369">Profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-369">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-370">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-370">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-371"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-371"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-372">Spécifie si l’encodeur génère des entrées de frame factice dans le flux binaire pour les frames en double.</span><span class="sxs-lookup"><span data-stu-id="d00a8-372">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span><br/> <dl> <span data-ttu-id="d00a8-373">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-373">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-374">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-374">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-375">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-375">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-376"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-376"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-377">Spécifie QP.</span><span class="sxs-lookup"><span data-stu-id="d00a8-377">Specifies QP.</span></span><br/> <dl> <span data-ttu-id="d00a8-378">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-378">Windows Vista and later.</span></span><br />
<span data-ttu-id="d00a8-379">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="d00a8-379">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="d00a8-380">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-380">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-381"><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-381"><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-382">Spécifie le degré auquel le codec doit réduire la plage de couleurs effectives de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="d00a8-382">Specifies the degree to which the codec should reduce the effective color range of the video.</span></span><br/> <dl> <span data-ttu-id="d00a8-383">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-383">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-384">Profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-384">Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-385">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-385">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-386"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-386"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-387">Spécifie la vitesse de transmission moyenne, en bits par seconde, utilisée pour l’encodage VBR (variable-bit-rate) à 2 passes.</span><span class="sxs-lookup"><span data-stu-id="d00a8-387">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="d00a8-388">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-388">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-389">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-389">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-390">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d00a8-390">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-391"><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-391"><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-392">Spécifie si l’encodeur utilise la recherche de MV sous-pixel basée sur les services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="d00a8-392">Specifies whether the encoder uses RD-based sub-pixel MV search.</span></span> <br/> <dl> <span data-ttu-id="d00a8-393">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-393">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-394">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="d00a8-394">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="d00a8-395">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-395">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-396"><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-396"><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-397">Pour le ré-encodage de segment, spécifie la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d00a8-397">For segment re-encoding, specifies the buffer size.</span></span><br/> <dl> <span data-ttu-id="d00a8-398">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-398">Windows Vista and later.</span></span><br />
<span data-ttu-id="d00a8-399">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="d00a8-399">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="d00a8-400">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-400">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-401"><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-401"><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-402">Pour le ré-encodage de segment, spécifie la durée du segment à recoder.</span><span class="sxs-lookup"><span data-stu-id="d00a8-402">For segment re-encoding, specifies the duration of the segment to be re-encoded.</span></span><br/> <dl> <span data-ttu-id="d00a8-403">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-403">Windows Vista and later.</span></span><br />
<span data-ttu-id="d00a8-404">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="d00a8-404">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="d00a8-405">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-405">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-406"><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-406"><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-407">Pour le ré-encodage de segment, spécifie le quantificateur du frame avant le segment de départ.</span><span class="sxs-lookup"><span data-stu-id="d00a8-407">For segment re-encoding, specifies the quantizer of the frame prior to the starting segment.</span></span><br/> <dl> <span data-ttu-id="d00a8-408">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-408">Windows Vista and later.</span></span><br />
<span data-ttu-id="d00a8-409">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="d00a8-409">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="d00a8-410">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-410">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-411"><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-411"><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-412">Pour le ré-encodage de segment, spécifie la saturation de la mémoire tampon de départ.</span><span class="sxs-lookup"><span data-stu-id="d00a8-412">For segment re-encoding, specifies the starting buffer fullness.</span></span><br/> <dl> <span data-ttu-id="d00a8-413">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-413">Windows Vista and later.</span></span><br />
<span data-ttu-id="d00a8-414">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="d00a8-414">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="d00a8-415">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-415">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-416"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-416"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-417">Spécifie le taux de bits de pointe, en bits par seconde, utilisé pour le VBR (variable-bit-bit-rate) avec une limite de 2 passes.</span><span class="sxs-lookup"><span data-stu-id="d00a8-417">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR).</span></span><br/> <dl> <span data-ttu-id="d00a8-418">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-418">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-419">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-419">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-420">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d00a8-420">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-421"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-421"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-422">Spécifie le nombre de trames vidéo transmises à l’encodeur pendant le processus d’encodage.</span><span class="sxs-lookup"><span data-stu-id="d00a8-422">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="d00a8-423">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-423">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-424">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="d00a8-424">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="d00a8-425">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-425">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-426"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-426"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-427">Spécifie si le codec utilise l’encodage VBR (variable-bit-rate).</span><span class="sxs-lookup"><span data-stu-id="d00a8-427">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="d00a8-428">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-428">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-429">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="d00a8-429">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="d00a8-430">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d00a8-430">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-431"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-431"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-432">Spécifie le niveau de qualité réel pour l’encodage VBR (variable-bit-rate) basé sur la qualité (1 passe).</span><span class="sxs-lookup"><span data-stu-id="d00a8-432">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="d00a8-433">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-433">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-434">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-434">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-435">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-435">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-436"><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-436"><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-437">Spécifie si le codec utilise l’optimisation de la mise à l’échelle vidéo.</span><span class="sxs-lookup"><span data-stu-id="d00a8-437">Specifies whether the codec will use video scaling optimization.</span></span><br/> <dl> <span data-ttu-id="d00a8-438">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-438">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-439">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-439">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-440">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-440">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-441"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-441"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-442">Spécifie la quantité de contenu, en millisecondes, qui peut tenir dans la mémoire tampon du modèle.</span><span class="sxs-lookup"><span data-stu-id="d00a8-442">Specifies the amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="d00a8-443">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-443">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-444">Profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-444">Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-445">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-445">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-446"><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-446"><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-447">Pour le ré-encodage de segment, spécifie les données privées du codec du fichier qui est à nouveau codé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-447">For segment re-encoding, specifies the codec private data of the file that is being re-encoded.</span></span><br/> <dl> <span data-ttu-id="d00a8-448">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-448">Windows Vista and later.</span></span><br />
<span data-ttu-id="d00a8-449">Profil simple, profil principal, profil avancé, image.</span><span class="sxs-lookup"><span data-stu-id="d00a8-449">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="d00a8-450">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-450">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00a8-451"><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-451"><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-452">Spécifie le type de logique qui sera utilisé par le codec pour détecter la vidéo source entrelacée.</span><span class="sxs-lookup"><span data-stu-id="d00a8-452">Specifies the type of logic that the codec will use to detect interlaced source video.</span></span><br/> <dl> <span data-ttu-id="d00a8-453">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-453">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-454">Profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-454">Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-455">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d00a8-455">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00a8-456"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00a8-456"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="d00a8-457">Spécifie le nombre de trames vidéo qui ont été ignorées, car il s’agissait de doublons de trames précédentes.</span><span class="sxs-lookup"><span data-stu-id="d00a8-457">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="d00a8-458">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d00a8-458">Windows XP and later.</span></span><br />
<span data-ttu-id="d00a8-459">Profil simple, profil principal, profil avancé.</span><span class="sxs-lookup"><span data-stu-id="d00a8-459">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="d00a8-460">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d00a8-460">Read-only</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="d00a8-461">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d00a8-461">Requirements</span></span>



| <span data-ttu-id="d00a8-462">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d00a8-462">Requirement</span></span> | <span data-ttu-id="d00a8-463">Valeur</span><span class="sxs-lookup"><span data-stu-id="d00a8-463">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d00a8-464">Client</span><span class="sxs-lookup"><span data-stu-id="d00a8-464">Client</span></span><br/> | <span data-ttu-id="d00a8-465">Windows XP, Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="d00a8-465">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="d00a8-466">En-tête</span><span class="sxs-lookup"><span data-stu-id="d00a8-466">Header</span></span><br/> | <dl> <span data-ttu-id="d00a8-467"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d00a8-467"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="d00a8-468">DLL</span><span class="sxs-lookup"><span data-stu-id="d00a8-468">DLL</span></span><br/>    | <dl> <span data-ttu-id="d00a8-469"><dt>Wmvencod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d00a8-469"><dt>Wmvencod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d00a8-470">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d00a8-470">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d00a8-471">Objets codec</span><span class="sxs-lookup"><span data-stu-id="d00a8-471">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="d00a8-472">Implémentation du codec</span><span class="sxs-lookup"><span data-stu-id="d00a8-472">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 
