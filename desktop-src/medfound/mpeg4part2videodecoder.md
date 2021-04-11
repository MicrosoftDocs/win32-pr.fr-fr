---
description: Le décodeur vidéo MPEG4 2e partie décode les flux vidéo qui ont été encodés en fonction de la norme MPEG4 2e partie.
ms.assetid: 56e32d3c-9bd0-41fe-bb22-e4ff37b7cc5c
title: Décodeur vidéo MPEG-4 part 2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 777e6144684c799eb58f75afd4811ccc8871a46b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201869"
---
# <a name="mpeg-4-part-2-video-decoder"></a><span data-ttu-id="966f1-103">Décodeur vidéo MPEG-4 part 2</span><span class="sxs-lookup"><span data-stu-id="966f1-103">MPEG-4 Part 2 Video Decoder</span></span>

<span data-ttu-id="966f1-104">Le décodeur vidéo MPEG4 2e partie décode les flux vidéo qui ont été encodés en fonction de la norme MPEG4 2e partie.</span><span class="sxs-lookup"><span data-stu-id="966f1-104">The MPEG4 Part 2 Video decoder decodes video streams that were encoded according to the MPEG4 Part 2 standard.</span></span>

<span data-ttu-id="966f1-105">Vous pouvez créer une instance du décodeur vidéo MPEG4 partie 2 en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="966f1-105">You can create an instance of the MPEG4 Part 2 Video decoder by calling **CoCreateInstance**.</span></span> <span data-ttu-id="966f1-106">Pour créer une instance du décodeur qui se comporte comme un objet de média DirectX (DMO), utilisez l’identificateur de classe **CLSID \_ CMpeg4sDecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="966f1-106">To create an instance of the decoder that behaves as a DirectX Media Object (DMO), use the class identifier **CLSID\_CMpeg4sDecMediaObject**.</span></span> <span data-ttu-id="966f1-107">Pour créer un Istance du décodeur qui se comporte comme une transformation de Media Foundation (MFT), utilisez l’identificateur de classe **CLSID \_ CMpeg4sDecMFT**.</span><span class="sxs-lookup"><span data-stu-id="966f1-107">To create an istance of the decoder that behaves as a Media Foundation Transform (MFT), use the class identifier **CLSID\_CMpeg4sDecMFT**.</span></span>

## <a name="input-types"></a><span data-ttu-id="966f1-108">Types d’entrée</span><span class="sxs-lookup"><span data-stu-id="966f1-108">Input Types</span></span>

<span data-ttu-id="966f1-109">Le décodeur vidéo MPEG4 2e partie prend en charge les types de média d’entrée suivants.</span><span class="sxs-lookup"><span data-stu-id="966f1-109">The MPEG4 Part 2 Video decoder supports the following input media types.</span></span>

-   <span data-ttu-id="966f1-110">MEDIASUBTYPE \_ M4S2</span><span class="sxs-lookup"><span data-stu-id="966f1-110">MEDIASUBTYPE\_M4S2</span></span>
-   <span data-ttu-id="966f1-111">MEDIASUBTYPE \_ m4s2</span><span class="sxs-lookup"><span data-stu-id="966f1-111">MEDIASUBTYPE\_m4s2</span></span>
-   <span data-ttu-id="966f1-112">MEDIASUBTYPE \_ mp4v</span><span class="sxs-lookup"><span data-stu-id="966f1-112">MEDIASUBTYPE\_MP4V</span></span>
-   <span data-ttu-id="966f1-113">MEDIASUBTYPE \_ mp4v</span><span class="sxs-lookup"><span data-stu-id="966f1-113">MEDIASUBTYPE\_mp4v</span></span>
-   <span data-ttu-id="966f1-114">MEDIASUBTYPE \_ fichiers MP4 à (déprécié)</span><span class="sxs-lookup"><span data-stu-id="966f1-114">MEDIASUBTYPE\_MP4S (deprecated)</span></span>
-   <span data-ttu-id="966f1-115">MEDIASUBTYPE \_ fichiers MP4 à (déprécié)</span><span class="sxs-lookup"><span data-stu-id="966f1-115">MEDIASUBTYPE\_mp4s (deprecated)</span></span>

## <a name="output-types"></a><span data-ttu-id="966f1-116">Types de sortie</span><span class="sxs-lookup"><span data-stu-id="966f1-116">Output Types</span></span>

<span data-ttu-id="966f1-117">Le décodeur vidéo MPEG4 2e partie prend en charge les sous-types de médias de sortie suivants lorsqu’il joue le rôle de DMO.</span><span class="sxs-lookup"><span data-stu-id="966f1-117">The MPEG4 Part 2 Video decoder supports the following output media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="966f1-118">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="966f1-118">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="966f1-119">MEDIASUBTYPE \_ NV12</span><span class="sxs-lookup"><span data-stu-id="966f1-119">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="966f1-120">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="966f1-120">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="966f1-121">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="966f1-121">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="966f1-122">MEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="966f1-122">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="966f1-123">MEDIASUBTYPE \_ NV11</span><span class="sxs-lookup"><span data-stu-id="966f1-123">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="966f1-124">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="966f1-124">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="966f1-125">MEDIASUBTYPE \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="966f1-125">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="966f1-126">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="966f1-126">MEDIASUBTYPE\_ RGB565</span></span>
-   <span data-ttu-id="966f1-127">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="966f1-127">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="966f1-128">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="966f1-128">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="966f1-129">Le décodeur vidéo MPEG4 2e partie prend en charge les sous-types de médias de sortie suivants lorsqu’il joue le rôle de MFT.</span><span class="sxs-lookup"><span data-stu-id="966f1-129">The MPEG4 Part 2 Video decoder supports the following output media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="966f1-130">MEDIASUBTYPE \_ NV12</span><span class="sxs-lookup"><span data-stu-id="966f1-130">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="966f1-131">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="966f1-131">MEDIASUBTYPE\_YV12</span></span>

## <a name="formats"></a><span data-ttu-id="966f1-132">Formats</span><span class="sxs-lookup"><span data-stu-id="966f1-132">Formats</span></span>

<span data-ttu-id="966f1-133">Le décodeur vidéo MPEG4 2ème partie accepte les formats suivants.</span><span class="sxs-lookup"><span data-stu-id="966f1-133">The MPEG4 Part 2 Video decoder accepts the following formats.</span></span>

-   [<span data-ttu-id="966f1-134">**VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="966f1-134">**VIDEOINFOHEADER**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)
-   <span data-ttu-id="966f1-135">[**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)</span><span class="sxs-lookup"><span data-stu-id="966f1-135">[**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)</span></span>
-   [<span data-ttu-id="966f1-136">**MFVideoInfo**</span><span class="sxs-lookup"><span data-stu-id="966f1-136">**MFVideoInfo**</span></span>](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoinfo)
-   <span data-ttu-id="966f1-137">[**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (seule la partie VIH2 de l’en-tête est utilisée.)</span><span class="sxs-lookup"><span data-stu-id="966f1-137">[**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (Only the VIH2 portion of the header is used.)</span></span>

## <a name="interfaces-for-the-dmo"></a><span data-ttu-id="966f1-138">Interfaces pour DMO</span><span class="sxs-lookup"><span data-stu-id="966f1-138">Interfaces for the DMO</span></span>

<span data-ttu-id="966f1-139">Si vous créez une instance du décodeur vidéo MPEG4 2e partie 2 comme DMO, le décodeur expose les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="966f1-139">If you create an instance of the MPEG4 Part 2 Video decoder as a DMO, the decoder exposes the following interfaces.</span></span>

-   [<span data-ttu-id="966f1-140">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="966f1-140">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="966f1-141">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="966f1-141">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)

<span data-ttu-id="966f1-142">Vous pouvez obtenir une interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) en appelant **CoCreateInstance**, et vous pouvez obtenir une interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) en appelant **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="966f1-142">You can obtain an [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface by calling **CoCreateInstance**, and you can obtain an [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface by calling **QueryInterface**.</span></span>

## <a name="interfaces-for-the-mft"></a><span data-ttu-id="966f1-143">Interfaces pour la MFT</span><span class="sxs-lookup"><span data-stu-id="966f1-143">Interfaces for the MFT</span></span>

<span data-ttu-id="966f1-144">Si vous créez une instance du décodeur vidéo MPEG2 partie 2 en tant que MFT, le décodeur expose les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="966f1-144">If you create an instance of the MPEG2 Part 2 Video decoder as an MFT, the decoder exposes the following interfaces.</span></span>

-   [<span data-ttu-id="966f1-145">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="966f1-145">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="966f1-146">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="966f1-146">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="966f1-147">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="966f1-147">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="966f1-148">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="966f1-148">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="966f1-149">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="966f1-149">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="966f1-150">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="966f1-150">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)

<span data-ttu-id="966f1-151">Vous pouvez obtenir un pointeur vers l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) en appelant **CoCreateInstance**, et vous pouvez obtenir un pointeur vers l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) en appelant [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes).</span><span class="sxs-lookup"><span data-stu-id="966f1-151">You can obtain a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface by calling **CoCreateInstance**, and you can obtain a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface by calling [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes).</span></span> <span data-ttu-id="966f1-152">Vous pouvez obtenir un pointeur vers l’interface [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) ou [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) en appelant **QueryInterface** sur la table MFT.</span><span class="sxs-lookup"><span data-stu-id="966f1-152">You can obtain a pointer to the [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) or [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) interface by calling **QueryInterface** on the MFT.</span></span> <span data-ttu-id="966f1-153">Vous pouvez obtenir un pointeur vers l’interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) ou [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) en appelant [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) et en passant l’identificateur de service **MF \_ rate \_ Control \_ service**.</span><span class="sxs-lookup"><span data-stu-id="966f1-153">You can obtain a pointer to the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) or [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface by calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) and passing the service identifier **MF\_RATE\_CONTROL\_SERVICE**.</span></span>

## <a name="profiles-and-levels"></a><span data-ttu-id="966f1-154">Profils et niveaux</span><span class="sxs-lookup"><span data-stu-id="966f1-154">Profiles and Levels</span></span>

<span data-ttu-id="966f1-155">La spécification MPEG4 définit plusieurs profils, chacun d’entre eux spécifiant les outils qu’un encodeur peut utiliser pour générer un flux encodé.</span><span class="sxs-lookup"><span data-stu-id="966f1-155">The MPEG4 specification defines several profiles, each of which specifies the tools that an encoder can use to generate an encoded stream.</span></span> <span data-ttu-id="966f1-156">Le décodeur vidéo MPEG4 part2 prend en charge deux de ces profils : un profil visuel simple et un profil simple avancé.</span><span class="sxs-lookup"><span data-stu-id="966f1-156">The MPEG4 Part2 Video Decoder supports two of those profiles: Simple Visual Profile and Advanced Simple Profile.</span></span> <span data-ttu-id="966f1-157">En d’autres termes, le décodeur vidéo MPEG4 partie 2 peut décoder les flux qui ont été encodés selon le profil d’élément visuel simple ou le profil simple avancé.</span><span class="sxs-lookup"><span data-stu-id="966f1-157">In other words, the MPEG4 Part 2 Video decoder can decode streams that were encoded according to either the Simple Visual Profile or the Advanced Simple Profile.</span></span>

<span data-ttu-id="966f1-158">Le profil visuel simple prend en charge la transmission de base d’une vidéo à faible vitesse de transmission en mode progressive.</span><span class="sxs-lookup"><span data-stu-id="966f1-158">The Simple Visual Profile supports basic transmission of low bit-rate video in progressive mode.</span></span> <span data-ttu-id="966f1-159">Il prend uniquement en charge les images intra et de prédiction.</span><span class="sxs-lookup"><span data-stu-id="966f1-159">It supports only Intra and Prediction pictures.</span></span> <span data-ttu-id="966f1-160">Il prend également en charge le mode d’en-tête abrégé, qui offre une compatibilité descendante avec le profil de base H. 263.</span><span class="sxs-lookup"><span data-stu-id="966f1-160">It also supports the short header mode, which is backward compatible with the H.263 baseline profile.</span></span> <span data-ttu-id="966f1-161">À compter de Windows 10, le décodeur vidéo MPEG-4 part 2 prend également en charge H. 263v2 (H. 263 +) qui prend en charge les tailles d’images personnalisées.</span><span class="sxs-lookup"><span data-stu-id="966f1-161">Starting with Windows 10, the MPEG-4 Part 2 Video Decoder also supports H.263v2 (H.263+) which supports custom picture sizes.</span></span>

<span data-ttu-id="966f1-162">Le profil simple avancé prend en charge tous les outils du profil visuel simple et, en outre, prend en charge la vidéo entrelacée, les images B, la compensation de mouvement Quarter-PEL, les tables de quantification supplémentaires et la compensation de mouvement globale.</span><span class="sxs-lookup"><span data-stu-id="966f1-162">The Advanced Simple Profile supports all the tools of the Simple Visual Profile and, in addition, supports interlaced video, B-frames, quarter-pel motion compensation, additional quantization tables, and global motion compensation.</span></span>

<span data-ttu-id="966f1-163">La spécification MPEG4 définit également plusieurs niveaux, chacun d’entre eux spécifiant des contraintes sur le flux de sortie généré par un encodeur.</span><span class="sxs-lookup"><span data-stu-id="966f1-163">The MPEG4 specification also defines several levels, each of which specifies constraints on the output stream generated by an encoder.</span></span>

<span data-ttu-id="966f1-164">Le tableau suivant présente les profils et les niveaux, ainsi que les résolutions classiques, prises en charge par le décodeur vidéo MPEG4 2e partie 2.</span><span class="sxs-lookup"><span data-stu-id="966f1-164">The following table shows the profiles and levels, along with typical resolutions, supported by the MPEG4 Part 2 Video decoder.</span></span>



| <span data-ttu-id="966f1-165">Profil</span><span class="sxs-lookup"><span data-stu-id="966f1-165">Profile</span></span>         | <span data-ttu-id="966f1-166">Level</span><span class="sxs-lookup"><span data-stu-id="966f1-166">Level</span></span> | <span data-ttu-id="966f1-167">Résolution standard</span><span class="sxs-lookup"><span data-stu-id="966f1-167">Typical Resolution</span></span> |
|-----------------|-------|--------------------|
| <span data-ttu-id="966f1-168">Visuel simple</span><span class="sxs-lookup"><span data-stu-id="966f1-168">Simple Visual</span></span>   | <span data-ttu-id="966f1-169">0</span><span class="sxs-lookup"><span data-stu-id="966f1-169">0</span></span>     | <span data-ttu-id="966f1-170">176 x 144</span><span class="sxs-lookup"><span data-stu-id="966f1-170">176 x 144</span></span>          |
| <span data-ttu-id="966f1-171">Visuel simple</span><span class="sxs-lookup"><span data-stu-id="966f1-171">Simple Visual</span></span>   | <span data-ttu-id="966f1-172">1</span><span class="sxs-lookup"><span data-stu-id="966f1-172">1</span></span>     | <span data-ttu-id="966f1-173">176 x 144</span><span class="sxs-lookup"><span data-stu-id="966f1-173">176 x 144</span></span>          |
| <span data-ttu-id="966f1-174">Visuel simple</span><span class="sxs-lookup"><span data-stu-id="966f1-174">Simple Visual</span></span>   | <span data-ttu-id="966f1-175">2</span><span class="sxs-lookup"><span data-stu-id="966f1-175">2</span></span>     | <span data-ttu-id="966f1-176">352 x 288</span><span class="sxs-lookup"><span data-stu-id="966f1-176">352 x 288</span></span>          |
| <span data-ttu-id="966f1-177">Visuel simple</span><span class="sxs-lookup"><span data-stu-id="966f1-177">Simple Visual</span></span>   | <span data-ttu-id="966f1-178">3</span><span class="sxs-lookup"><span data-stu-id="966f1-178">3</span></span>     | <span data-ttu-id="966f1-179">352 x 288</span><span class="sxs-lookup"><span data-stu-id="966f1-179">352 x 288</span></span>          |
| <span data-ttu-id="966f1-180">SimpleVisual</span><span class="sxs-lookup"><span data-stu-id="966f1-180">SimpleVisual</span></span>    | <span data-ttu-id="966f1-181">4a</span><span class="sxs-lookup"><span data-stu-id="966f1-181">4a</span></span>    | <span data-ttu-id="966f1-182">640 x 480</span><span class="sxs-lookup"><span data-stu-id="966f1-182">640 x 480</span></span>          |
| <span data-ttu-id="966f1-183">Visuel simple</span><span class="sxs-lookup"><span data-stu-id="966f1-183">Simple Visual</span></span>   | <span data-ttu-id="966f1-184">5</span><span class="sxs-lookup"><span data-stu-id="966f1-184">5</span></span>     | <span data-ttu-id="966f1-185">720 x 576</span><span class="sxs-lookup"><span data-stu-id="966f1-185">720 x 576</span></span>          |
| <span data-ttu-id="966f1-186">Advanced simple</span><span class="sxs-lookup"><span data-stu-id="966f1-186">Advanced Simple</span></span> | <span data-ttu-id="966f1-187">0</span><span class="sxs-lookup"><span data-stu-id="966f1-187">0</span></span>     | <span data-ttu-id="966f1-188">176 x 144</span><span class="sxs-lookup"><span data-stu-id="966f1-188">176 x 144</span></span>          |
| <span data-ttu-id="966f1-189">Advanced simple</span><span class="sxs-lookup"><span data-stu-id="966f1-189">Advanced Simple</span></span> | <span data-ttu-id="966f1-190">1</span><span class="sxs-lookup"><span data-stu-id="966f1-190">1</span></span>     | <span data-ttu-id="966f1-191">176 x 144</span><span class="sxs-lookup"><span data-stu-id="966f1-191">176 x 144</span></span>          |
| <span data-ttu-id="966f1-192">Advanced simple</span><span class="sxs-lookup"><span data-stu-id="966f1-192">Advanced Simple</span></span> | <span data-ttu-id="966f1-193">2</span><span class="sxs-lookup"><span data-stu-id="966f1-193">2</span></span>     | <span data-ttu-id="966f1-194">352 x 288</span><span class="sxs-lookup"><span data-stu-id="966f1-194">352 x 288</span></span>          |
| <span data-ttu-id="966f1-195">Advanced simple</span><span class="sxs-lookup"><span data-stu-id="966f1-195">Advanced Simple</span></span> | <span data-ttu-id="966f1-196">3</span><span class="sxs-lookup"><span data-stu-id="966f1-196">3</span></span>     | <span data-ttu-id="966f1-197">352 x 288</span><span class="sxs-lookup"><span data-stu-id="966f1-197">352 x 288</span></span>          |
| <span data-ttu-id="966f1-198">Advanced simple</span><span class="sxs-lookup"><span data-stu-id="966f1-198">Advanced Simple</span></span> | <span data-ttu-id="966f1-199">3b</span><span class="sxs-lookup"><span data-stu-id="966f1-199">3b</span></span>    | <span data-ttu-id="966f1-200">352 x 288</span><span class="sxs-lookup"><span data-stu-id="966f1-200">352 x 288</span></span>          |
| <span data-ttu-id="966f1-201">Advanced simple</span><span class="sxs-lookup"><span data-stu-id="966f1-201">Advanced Simple</span></span> | <span data-ttu-id="966f1-202">4</span><span class="sxs-lookup"><span data-stu-id="966f1-202">4</span></span>     | <span data-ttu-id="966f1-203">352 x 756</span><span class="sxs-lookup"><span data-stu-id="966f1-203">352 x 756</span></span>          |
| <span data-ttu-id="966f1-204">Advanced simple</span><span class="sxs-lookup"><span data-stu-id="966f1-204">Advanced Simple</span></span> | <span data-ttu-id="966f1-205">5</span><span class="sxs-lookup"><span data-stu-id="966f1-205">5</span></span>     | <span data-ttu-id="966f1-206">720 x 576</span><span class="sxs-lookup"><span data-stu-id="966f1-206">720 x 576</span></span>          |



 

<span data-ttu-id="966f1-207">Pour plus d’informations sur les profils et les niveaux, consultez la spécification MPEG4 2ème partie 2 (ISO/IEC 14496-2) : Information Technology--Coding of Audio-Visual Objects--part 2 : Visual.</span><span class="sxs-lookup"><span data-stu-id="966f1-207">For more information about profiles and levels, see the MPEG4 Part 2 specification (ISO/IEC 14496-2): Information technology -- Coding of audio-visual objects -- Part 2: Visual.</span></span>

## <a name="decoder-properties"></a><span data-ttu-id="966f1-208">Propriétés du décodeur</span><span class="sxs-lookup"><span data-stu-id="966f1-208">Decoder Properties</span></span>

<span data-ttu-id="966f1-209">Pour définir des propriétés sur le décodeur vidéo MPEG4 2e partie 2, utilisez l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) ou l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="966f1-209">To set properties on the MPEG4 Part 2 Video decoder, use the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface or the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="966f1-210">Le décodeur vidéo MPEG4 2e partie prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="966f1-210">The MPEG4 Part 2 Video decoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="966f1-211">Propriété</span><span class="sxs-lookup"><span data-stu-id="966f1-211">Property</span></span></th>
<th><span data-ttu-id="966f1-212">Description</span><span class="sxs-lookup"><span data-stu-id="966f1-212">Description</span></span></th>
<th><span data-ttu-id="966f1-213">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="966f1-213">Default Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="966f1-214"><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></span><span class="sxs-lookup"><span data-stu-id="966f1-214"><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></span></span></td>
<td><span data-ttu-id="966f1-215">Spécifie le niveau de puissance.</span><span class="sxs-lookup"><span data-stu-id="966f1-215">Specifies the power level.</span></span><br/> <dl> <span data-ttu-id="966f1-216">Windows 7</span><span class="sxs-lookup"><span data-stu-id="966f1-216">Windows 7.</span></span><br />
<span data-ttu-id="966f1-217">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="966f1-217">Write-only.</span></span><br />
</dl></td>
<td><span data-ttu-id="966f1-218">100</span><span class="sxs-lookup"><span data-stu-id="966f1-218">100</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="966f1-219"><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="966f1-219"><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></span></span></td>
<td><span data-ttu-id="966f1-220">Spécifie le mode de génération de miniatures.</span><span class="sxs-lookup"><span data-stu-id="966f1-220">Specifies the thumbnail generation mode.</span></span><br/> <dl> <span data-ttu-id="966f1-221">Windows 7</span><span class="sxs-lookup"><span data-stu-id="966f1-221">Windows 7.</span></span><br />
<span data-ttu-id="966f1-222">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="966f1-222">Write-only.</span></span><br />
</dl></td>
<td><span data-ttu-id="966f1-223"><strong>VARIANT_FALSE</strong></span><span class="sxs-lookup"><span data-stu-id="966f1-223"><strong>VARIANT_FALSE</strong></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="966f1-224">Notes</span><span class="sxs-lookup"><span data-stu-id="966f1-224">Remarks</span></span>

<span data-ttu-id="966f1-225">Les identificateurs globaux uniques (GUID) pour les sous-types de média RVB diffèrent selon qu’un décodeur agit comme DMO ou MFT.</span><span class="sxs-lookup"><span data-stu-id="966f1-225">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="966f1-226">Les GUID pour les sous-types de média non RVB sont les mêmes, qu’un décodeur agisse comme DMO ou MFT.</span><span class="sxs-lookup"><span data-stu-id="966f1-226">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="966f1-227">Pour plus d’informations sur les GUID qui représentent des sous-types de médias, consultez [types de médias](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="966f1-227">For information about the GUIDs that represent media subtypes, see [Media Types](media-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="966f1-228">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="966f1-228">Requirements</span></span>



| <span data-ttu-id="966f1-229">Condition requise</span><span class="sxs-lookup"><span data-stu-id="966f1-229">Requirement</span></span> | <span data-ttu-id="966f1-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="966f1-230">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="966f1-231">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="966f1-231">Minimum supported client</span></span><br/> | <span data-ttu-id="966f1-232">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="966f1-232">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="966f1-233">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="966f1-233">Minimum supported server</span></span><br/> | <span data-ttu-id="966f1-234">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="966f1-234">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="966f1-235">En-tête</span><span class="sxs-lookup"><span data-stu-id="966f1-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="966f1-236"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="966f1-236"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="966f1-237">DLL</span><span class="sxs-lookup"><span data-stu-id="966f1-237">DLL</span></span><br/>                      | <dl> <span data-ttu-id="966f1-238"><dt>MP4SDecd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="966f1-238"><dt>MP4SDecd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="966f1-239">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="966f1-239">See also</span></span>

<dl> <dt>

[<span data-ttu-id="966f1-240">Objets codec</span><span class="sxs-lookup"><span data-stu-id="966f1-240">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
