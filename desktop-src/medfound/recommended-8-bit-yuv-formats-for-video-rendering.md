---
description: Formats YUV 8 bits recommandés pour le rendu vidéo
ms.assetid: 675d4c60-4c58-4f15-9bae-ffb0c389c608
title: Formats YUV 8 bits recommandés pour le rendu vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4505eb17f833040e0148ac98912f16af860b55b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753892"
---
# <a name="recommended-8-bit-yuv-formats-for-video-rendering"></a><span data-ttu-id="d3e65-103">Formats YUV 8 bits recommandés pour le rendu vidéo</span><span class="sxs-lookup"><span data-stu-id="d3e65-103">Recommended 8-Bit YUV Formats for Video Rendering</span></span>

<span data-ttu-id="d3e65-104">Gary Sullivan et Stephen Estrop</span><span class="sxs-lookup"><span data-stu-id="d3e65-104">Gary Sullivan and Stephen Estrop</span></span>

<span data-ttu-id="d3e65-105">Microsoft Corporation</span><span class="sxs-lookup"><span data-stu-id="d3e65-105">Microsoft Corporation</span></span>

<span data-ttu-id="d3e65-106">2002 avril, mis à jour le 2008 novembre</span><span class="sxs-lookup"><span data-stu-id="d3e65-106">April 2002, updated November 2008</span></span>

<span data-ttu-id="d3e65-107">Cette rubrique décrit les formats de couleurs YUV 8 bits recommandés pour le rendu vidéo dans le système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="d3e65-107">This topic describes the 8-bit YUV color formats that are recommended for video rendering in the Windows operating system.</span></span> <span data-ttu-id="d3e65-108">Cet article présente les techniques de conversion entre les formats YUV et RVB, et fournit également des techniques pour l’échantillonnage des formats YUV.</span><span class="sxs-lookup"><span data-stu-id="d3e65-108">This article presents techniques for converting between YUV and RGB formats, and also provides techniques for upsampling YUV formats.</span></span> <span data-ttu-id="d3e65-109">Cet article est destiné aux personnes qui travaillent avec le décodage vidéo YUV ou le rendu dans Windows.</span><span class="sxs-lookup"><span data-stu-id="d3e65-109">This article is intended for anyone working with YUV video decoding or rendering in Windows.</span></span>

## <a name="introduction"></a><span data-ttu-id="d3e65-110">Introduction</span><span class="sxs-lookup"><span data-stu-id="d3e65-110">Introduction</span></span>

<span data-ttu-id="d3e65-111">De nombreux formats YUV sont définis dans l’ensemble du secteur de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="d3e65-111">Numerous YUV formats are defined throughout the video industry.</span></span> <span data-ttu-id="d3e65-112">Cet article identifie les formats YUV 8 bits recommandés pour le rendu vidéo dans Windows.</span><span class="sxs-lookup"><span data-stu-id="d3e65-112">This article identifies the 8-bit YUV formats that are recommended for video rendering in Windows.</span></span> <span data-ttu-id="d3e65-113">Les fournisseurs de décodeurs et les fournisseurs d’affichage sont encouragés à prendre en charge les formats décrits dans cet article.</span><span class="sxs-lookup"><span data-stu-id="d3e65-113">Decoder vendors and display vendors are encouraged to support the formats described in this article.</span></span> <span data-ttu-id="d3e65-114">Cet article ne traite pas d’autres utilisations de la couleur YUV, telles que la photographie continue.</span><span class="sxs-lookup"><span data-stu-id="d3e65-114">This article does not address other uses of YUV color, such as still photography.</span></span>

<span data-ttu-id="d3e65-115">Les formats décrits dans cet article utilisent tous 8 bits par emplacement de pixel pour encoder le canal Y (également appelé canal de luminance) et utilisent 8 bits par échantillon pour encoder chaque échantillon de chrominance U ou V.</span><span class="sxs-lookup"><span data-stu-id="d3e65-115">The formats described in this article all use 8 bits per pixel location to encode the Y channel (also called the luma channel), and use 8 bits per sample to encode each U or V chroma sample.</span></span> <span data-ttu-id="d3e65-116">Toutefois, la plupart des formats YUV utilisent moins de 24 bits par pixel en moyenne, car ils contiennent moins d’échantillons de vous et de V que de Y. Cet article ne couvre pas les formats YUV avec des canaux Y 10 bits ou plus.</span><span class="sxs-lookup"><span data-stu-id="d3e65-116">However, most YUV formats use fewer than 24 bits per pixel on average, because they contain fewer samples of U and V than of Y. This article does not cover YUV formats with 10-bit or higher Y channels.</span></span>

> [!Note]  
> <span data-ttu-id="d3e65-117">Dans le cadre de cet article, le terme U est équivalent à CB et le terme V équivaut à CR.</span><span class="sxs-lookup"><span data-stu-id="d3e65-117">For the purposes of this article, the term U is equivalent to Cb, and the term V is equivalent to Cr.</span></span>

 

<span data-ttu-id="d3e65-118">Cet article aborde les thèmes suivants :</span><span class="sxs-lookup"><span data-stu-id="d3e65-118">This article covers the following topics:</span></span>

-   <span data-ttu-id="d3e65-119">[Échantillonnage YUV](#yuv-sampling).</span><span class="sxs-lookup"><span data-stu-id="d3e65-119">[YUV Sampling](#yuv-sampling).</span></span> <span data-ttu-id="d3e65-120">Décrit les techniques d’échantillonnage YUV les plus courantes.</span><span class="sxs-lookup"><span data-stu-id="d3e65-120">Describes the most common YUV sampling techniques.</span></span>
-   <span data-ttu-id="d3e65-121">[Définitions de surface](#surface-definitions).</span><span class="sxs-lookup"><span data-stu-id="d3e65-121">[Surface Definitions](#surface-definitions).</span></span> <span data-ttu-id="d3e65-122">Décrit les formats YUV recommandés.</span><span class="sxs-lookup"><span data-stu-id="d3e65-122">Describes the recommended YUV formats.</span></span>
-   <span data-ttu-id="d3e65-123">[Conversions de l’espace colorimétrique et du taux d’échantillonnage Chroma](#color-space-and-chroma-sampling-rate-conversions).</span><span class="sxs-lookup"><span data-stu-id="d3e65-123">[Color Space and Chroma Sampling Rate Conversions](#color-space-and-chroma-sampling-rate-conversions).</span></span> <span data-ttu-id="d3e65-124">Fournit des instructions pour la conversion entre des formats YUV et RGB et pour la conversion entre différents formats YUV.</span><span class="sxs-lookup"><span data-stu-id="d3e65-124">Provides some guidelines for converting between YUV and RGB formats and for converting between different YUV formats.</span></span>
-   <span data-ttu-id="d3e65-125">[Identification des formats YUV dans Media Foundation](#identifying-yuv-formats-in-media-foundation).</span><span class="sxs-lookup"><span data-stu-id="d3e65-125">[Identifying YUV Formats in Media Foundation](#identifying-yuv-formats-in-media-foundation).</span></span> <span data-ttu-id="d3e65-126">Explique comment décrire les types de format YUV dans Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d3e65-126">Explains how to describe YUV format types in Media Foundation.</span></span>

## <a name="yuv-sampling"></a><span data-ttu-id="d3e65-127">Échantillonnage YUV</span><span class="sxs-lookup"><span data-stu-id="d3e65-127">YUV Sampling</span></span>

<span data-ttu-id="d3e65-128">Les canaux Chroma peuvent avoir un taux d’échantillonnage inférieur à celui du canal de luminance, sans aucune perte spectaculaire de qualité de perception.</span><span class="sxs-lookup"><span data-stu-id="d3e65-128">Chroma channels can have a lower sampling rate than the luma channel, without any dramatic loss of perceptual quality.</span></span> <span data-ttu-id="d3e65-129">Une notation appelée « A :B: C » est utilisée pour décrire la fréquence à laquelle vous et le V sont échantillonnés par rapport à Y :</span><span class="sxs-lookup"><span data-stu-id="d3e65-129">A notation called the "A:B:C" notation is used to describe how often U and V are sampled relative to Y:</span></span>

-   <span data-ttu-id="d3e65-130">4:4:4 signifie aucun sous-échantillonnage des canaux Chroma.</span><span class="sxs-lookup"><span data-stu-id="d3e65-130">4:4:4 means no downsampling of the chroma channels.</span></span>
-   <span data-ttu-id="d3e65-131">4:2:2 signifie un sous-échantillonnage horizontal de 2:1, sans sous-échantillonnage vertical.</span><span class="sxs-lookup"><span data-stu-id="d3e65-131">4:2:2 means 2:1 horizontal downsampling, with no vertical downsampling.</span></span> <span data-ttu-id="d3e65-132">Chaque ligne de numérisation contient quatre échantillons Y pour chacun des deux échantillons U ou V.</span><span class="sxs-lookup"><span data-stu-id="d3e65-132">Every scan line contains four Y samples for every two U or V samples.</span></span>
-   <span data-ttu-id="d3e65-133">4:2:0 signifie le sous-échantillonnage horizontal 2:1 de 2:1, avec un sous-échantillonnage vertical.</span><span class="sxs-lookup"><span data-stu-id="d3e65-133">4:2:0 means 2:1 horizontal downsampling, with 2:1 vertical downsampling.</span></span>
-   <span data-ttu-id="d3e65-134">4:1:1 signifie un sous-échantillonnage horizontal de 4:1, sans sous-échantillonnage vertical.</span><span class="sxs-lookup"><span data-stu-id="d3e65-134">4:1:1 means 4:1 horizontal downsampling, with no vertical downsampling.</span></span> <span data-ttu-id="d3e65-135">Chaque ligne de numérisation contient quatre échantillons Y pour chaque exemple V et V.</span><span class="sxs-lookup"><span data-stu-id="d3e65-135">Every scan line contains four Y samples for each U and V sample.</span></span> <span data-ttu-id="d3e65-136">4:1:1 l’échantillonnage est moins courant que les autres formats, et n’est pas abordé en détail dans cet article.</span><span class="sxs-lookup"><span data-stu-id="d3e65-136">4:1:1 sampling is less common than other formats, and is not discussed in detail in this article.</span></span>

<span data-ttu-id="d3e65-137">Les diagrammes suivants montrent comment Chroma est échantillonné pour chaque fréquence de sous-échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="d3e65-137">The following diagrams shows how chroma is sampled for each of the downsampling rates.</span></span> <span data-ttu-id="d3e65-138">Les échantillons de luminance sont représentés par une croix, et les échantillons de chrominance sont représentés par un cercle.</span><span class="sxs-lookup"><span data-stu-id="d3e65-138">Luma samples are represented by a cross, and chroma samples are represented by a circle.</span></span>

![Figure 1.](images/yuv-sampling-grids.png)

<span data-ttu-id="d3e65-141">La forme dominante de l’échantillonnage 4:2:2 est définie dans la recommandation ITU-R BT. 601.</span><span class="sxs-lookup"><span data-stu-id="d3e65-141">The dominant form of 4:2:2 sampling is defined in ITU-R Recommendation BT.601.</span></span> <span data-ttu-id="d3e65-142">Il existe deux variantes courantes de l’échantillonnage 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="d3e65-142">There are two common variants of 4:2:0 sampling.</span></span> <span data-ttu-id="d3e65-143">L’une d’elles est utilisée dans MPEG-2 Video, tandis que l’autre est utilisée dans MPEG-1 et dans les recommandations de l’ITU-T et de l’h. 261.</span><span class="sxs-lookup"><span data-stu-id="d3e65-143">One of these is used in MPEG-2 video, and the other is used in MPEG-1 and in ITU-T Recommendations H.261 and H.263.</span></span>

<span data-ttu-id="d3e65-144">Comparé au schéma MPEG-1, il est plus simple de procéder à une conversion entre le schéma MPEG-2 et les grilles d’échantillonnage définies pour les formats 4:2:2 et 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="d3e65-144">Compared with the MPEG-1 scheme, it is simpler to convert between the MPEG-2 scheme and the sampling grids defined for 4:2:2 and 4:4:4 formats.</span></span> <span data-ttu-id="d3e65-145">Pour cette raison, le schéma MPEG-2 est préféré dans Windows et doit être considéré comme l’interprétation par défaut des formats 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="d3e65-145">For this reason, the MPEG-2 scheme is preferred in Windows, and should be considered the default interpretation of 4:2:0 formats.</span></span>

## <a name="surface-definitions"></a><span data-ttu-id="d3e65-146">Définitions de surface</span><span class="sxs-lookup"><span data-stu-id="d3e65-146">Surface Definitions</span></span>

<span data-ttu-id="d3e65-147">Cette section décrit les formats YUV 8 bits recommandés pour le rendu vidéo.</span><span class="sxs-lookup"><span data-stu-id="d3e65-147">This section describes the 8-bit YUV formats that are recommended for video rendering.</span></span> <span data-ttu-id="d3e65-148">Celles-ci appartiennent à plusieurs catégories :</span><span class="sxs-lookup"><span data-stu-id="d3e65-148">These fall into several categories:</span></span>

-   [<span data-ttu-id="d3e65-149">4:4:4 formats, 32 bits par pixel</span><span class="sxs-lookup"><span data-stu-id="d3e65-149">4:4:4 Formats, 32 Bits per Pixel</span></span>](#444-formats-32-bits-per-pixel)
-   [<span data-ttu-id="d3e65-150">4:2:2 formats, 16 bits par pixel</span><span class="sxs-lookup"><span data-stu-id="d3e65-150">4:2:2 Formats, 16 Bits per Pixel</span></span>](#422-formats-16-bits-per-pixel)
-   [<span data-ttu-id="d3e65-151">4:2:0 formats, 16 bits par pixel</span><span class="sxs-lookup"><span data-stu-id="d3e65-151">4:2:0 Formats, 16 Bits per Pixel</span></span>](#420-formats-16-bits-per-pixel)
-   [<span data-ttu-id="d3e65-152">4:2:0 formats, 12 bits par pixel</span><span class="sxs-lookup"><span data-stu-id="d3e65-152">4:2:0 Formats, 12 Bits per Pixel</span></span>](#420-formats-12-bits-per-pixel)

<span data-ttu-id="d3e65-153">Tout d’abord, vous devez connaître les concepts suivants pour comprendre ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="d3e65-153">First, you should be aware of the following concepts in order to understand what follows:</span></span>

-   <span data-ttu-id="d3e65-154">*Origine* de la surface.</span><span class="sxs-lookup"><span data-stu-id="d3e65-154">*Surface origin*.</span></span> <span data-ttu-id="d3e65-155">Pour les formats YUV décrits dans cet article, l’origine (0,0) est toujours l’angle supérieur gauche de l’aire.</span><span class="sxs-lookup"><span data-stu-id="d3e65-155">For the YUV formats described in this article, the origin (0,0) is always the top left corner of the surface.</span></span>
-   <span data-ttu-id="d3e65-156">*Stride*.</span><span class="sxs-lookup"><span data-stu-id="d3e65-156">*Stride*.</span></span> <span data-ttu-id="d3e65-157">La largeur d’une surface, parfois appelée « tangage », est la largeur de la surface en octets.</span><span class="sxs-lookup"><span data-stu-id="d3e65-157">The stride of a surface, sometimes called the pitch, is the width of the surface in bytes.</span></span> <span data-ttu-id="d3e65-158">À partir de l’origine d’une surface dans le coin supérieur gauche, le Stride est toujours positif.</span><span class="sxs-lookup"><span data-stu-id="d3e65-158">Given a surface origin at the top left corner, the stride is always positive.</span></span>
-   <span data-ttu-id="d3e65-159">*Alignement*.</span><span class="sxs-lookup"><span data-stu-id="d3e65-159">*Alignment*.</span></span> <span data-ttu-id="d3e65-160">L’alignement d’une surface est à la discrétion du pilote d’affichage graphique.</span><span class="sxs-lookup"><span data-stu-id="d3e65-160">The alignment of a surface is at the discretion of the graphics display driver.</span></span> <span data-ttu-id="d3e65-161">La surface doit toujours être alignée sur la valeur DWORD. autrement dit, il est garanti que les lignes individuelles de la surface proviennent d’une limite de 32 bits (DWORD).</span><span class="sxs-lookup"><span data-stu-id="d3e65-161">The surface must always be DWORD aligned; that is, individual lines within the surface are guaranteed to originate on a 32-bit (DWORD) boundary.</span></span> <span data-ttu-id="d3e65-162">Toutefois, l’alignement peut être supérieur à 32 bits, en fonction des besoins du matériel.</span><span class="sxs-lookup"><span data-stu-id="d3e65-162">The alignment can be larger than 32 bits, however, depending on the needs of the hardware.</span></span>
-   <span data-ttu-id="d3e65-163">Format condensé et format Planar.</span><span class="sxs-lookup"><span data-stu-id="d3e65-163">Packed format versus planar format.</span></span> <span data-ttu-id="d3e65-164">Les formats YUV sont divisés en formats *compactés* et en formats *planaires* .</span><span class="sxs-lookup"><span data-stu-id="d3e65-164">YUV formats are divided into *packed* formats and *planar* formats.</span></span> <span data-ttu-id="d3e65-165">Dans un format compressé, les composants Y, U et V sont stockés dans un tableau unique.</span><span class="sxs-lookup"><span data-stu-id="d3e65-165">In a packed format, the Y, U, and V components are stored in a single array.</span></span> <span data-ttu-id="d3e65-166">Les pixels sont organisés en groupes de macropixels, dont la disposition dépend du format.</span><span class="sxs-lookup"><span data-stu-id="d3e65-166">Pixels are organized into groups of macropixels, whose layout depends on the format.</span></span> <span data-ttu-id="d3e65-167">Dans un format Planar, les composants Y, U et V sont stockés sous la forme de trois plans distincts.</span><span class="sxs-lookup"><span data-stu-id="d3e65-167">In a planar format, the Y, U, and V components are stored as three separate planes.</span></span>

<span data-ttu-id="d3e65-168">Chaque format YUV décrit dans cet article est associé à un code FOURCC.</span><span class="sxs-lookup"><span data-stu-id="d3e65-168">Each of the YUV formats described in this article has an assigned FOURCC code.</span></span> <span data-ttu-id="d3e65-169">Un code FOURCC est un entier non signé 32 bits créé par la concaténation de quatre caractères ASCII.</span><span class="sxs-lookup"><span data-stu-id="d3e65-169">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span>

-   <span data-ttu-id="d3e65-170">4:4:4 (32 BPP)</span><span class="sxs-lookup"><span data-stu-id="d3e65-170">4:4:4 (32 bpp)</span></span>
    -   [<span data-ttu-id="d3e65-171">AYUV</span><span class="sxs-lookup"><span data-stu-id="d3e65-171">AYUV</span></span>](#ayuv)
-   <span data-ttu-id="d3e65-172">4:2:2 (16 bpp)</span><span class="sxs-lookup"><span data-stu-id="d3e65-172">4:2:2 (16 bpp)</span></span>
    -   [<span data-ttu-id="d3e65-173">YUY2</span><span class="sxs-lookup"><span data-stu-id="d3e65-173">YUY2</span></span>](#yuy2)
    -   [<span data-ttu-id="d3e65-174">UYVY</span><span class="sxs-lookup"><span data-stu-id="d3e65-174">UYVY</span></span>](#uyvy)
-   <span data-ttu-id="d3e65-175">4:2:0 (16 bpp)</span><span class="sxs-lookup"><span data-stu-id="d3e65-175">4:2:0 (16 bpp)</span></span>
    -   [<span data-ttu-id="d3e65-176">IMC1</span><span class="sxs-lookup"><span data-stu-id="d3e65-176">IMC1</span></span>](#imc1)
    -   [<span data-ttu-id="d3e65-177">IMC3</span><span class="sxs-lookup"><span data-stu-id="d3e65-177">IMC3</span></span>](#imc3)
-   <span data-ttu-id="d3e65-178">4:2:0 (12 BPP)</span><span class="sxs-lookup"><span data-stu-id="d3e65-178">4:2:0 (12 bpp)</span></span>
    -   [<span data-ttu-id="d3e65-179">IMC2</span><span class="sxs-lookup"><span data-stu-id="d3e65-179">IMC2</span></span>](#imc2)
    -   [<span data-ttu-id="d3e65-180">IMC4</span><span class="sxs-lookup"><span data-stu-id="d3e65-180">IMC4</span></span>](#imc4)
    -   [<span data-ttu-id="d3e65-181">YV12</span><span class="sxs-lookup"><span data-stu-id="d3e65-181">YV12</span></span>](#yv12)
    -   [<span data-ttu-id="d3e65-182">NV12</span><span class="sxs-lookup"><span data-stu-id="d3e65-182">NV12</span></span>](#nv12)

## <a name="444-formats-32-bits-per-pixel"></a><span data-ttu-id="d3e65-183">4:4:4 formats, 32 bits par pixel</span><span class="sxs-lookup"><span data-stu-id="d3e65-183">4:4:4 Formats, 32 Bits per Pixel</span></span>

### <a name="ayuv"></a><span data-ttu-id="d3e65-184">AYUV</span><span class="sxs-lookup"><span data-stu-id="d3e65-184">AYUV</span></span>

<span data-ttu-id="d3e65-185">Un format 4:4:4 unique est recommandé, avec le code FOURCC AYUV.</span><span class="sxs-lookup"><span data-stu-id="d3e65-185">A single 4:4:4 format is recommended, with the FOURCC code AYUV.</span></span> <span data-ttu-id="d3e65-186">Il s’agit d’un format compressé, où chaque pixel est encodé sous la forme de quatre octets consécutifs, organisés dans l’ordre indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d3e65-186">This is a packed format, where each pixel is encoded as four consecutive bytes, arranged in the sequence shown in the following illustration.</span></span>

![Figure 2.](images/yuvformats01.gif)

<span data-ttu-id="d3e65-189">Les octets marqués un contiennent des valeurs pour alpha.</span><span class="sxs-lookup"><span data-stu-id="d3e65-189">The bytes marked A contain values for alpha.</span></span>

## <a name="422-formats-16-bits-per-pixel"></a><span data-ttu-id="d3e65-190">4:2:2 formats, 16 bits par pixel</span><span class="sxs-lookup"><span data-stu-id="d3e65-190">4:2:2 Formats, 16 Bits per Pixel</span></span>

<span data-ttu-id="d3e65-191">Deux formats 4:2:2 sont recommandés, avec les Codes FOURCC suivants :</span><span class="sxs-lookup"><span data-stu-id="d3e65-191">Two 4:2:2 formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="d3e65-192">YUY2</span><span class="sxs-lookup"><span data-stu-id="d3e65-192">YUY2</span></span>
-   <span data-ttu-id="d3e65-193">UYVY</span><span class="sxs-lookup"><span data-stu-id="d3e65-193">UYVY</span></span>

<span data-ttu-id="d3e65-194">Les deux sont des formats compactés, où chaque macropixel est codé sur deux pixels, sous la forme de quatre octets consécutifs.</span><span class="sxs-lookup"><span data-stu-id="d3e65-194">Both are packed formats, where each macropixel is two pixels encoded as four consecutive bytes.</span></span> <span data-ttu-id="d3e65-195">Cela entraîne un sous-échantillonnage horizontal du Chroma par un facteur de deux.</span><span class="sxs-lookup"><span data-stu-id="d3e65-195">This results in horizontal downsampling of the chroma by a factor of two.</span></span>

### <a name="yuy2"></a><span data-ttu-id="d3e65-196">YUY2</span><span class="sxs-lookup"><span data-stu-id="d3e65-196">YUY2</span></span>

<span data-ttu-id="d3e65-197">Dans le format YUY2, les données peuvent être traitées sous la forme d’un tableau de valeurs **char** non signées, où le premier octet contient le premier échantillon y, le deuxième octet contient le premier exemple U (CB), le troisième octet le deuxième y, et le quatrième octet le premier exemple V (CR), comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="d3e65-197">In YUY2 format, the data can be treated as an array of unsigned **char** values, where the first byte contains the first Y sample, the second byte contains the first U (Cb) sample, the third byte contains the second Y sample, and the fourth byte contains the first V (Cr) sample, as shown in the following diagram.</span></span>

![Figure 3.](images/yuvformats02.gif)

<span data-ttu-id="d3e65-200">Si l’image est traitée comme un tableau de valeurs de **mot** Little-endian, le premier **mot** contient le premier échantillon Y dans les bits les moins significatifs (LSBs) et le premier exemple U (CB) dans les bits les plus significatifs (MSBS).</span><span class="sxs-lookup"><span data-stu-id="d3e65-200">If the image is addressed as an array of little-endian **WORD** values, the first **WORD** contains the first Y sample in the least significant bits (LSBs) and the first U (Cb) sample in the most significant bits (MSBs).</span></span> <span data-ttu-id="d3e65-201">Le deuxième **mot** contient le deuxième échantillon Y dans le LSBs et le premier exemple V (CR) dans le MSBS.</span><span class="sxs-lookup"><span data-stu-id="d3e65-201">The second **WORD** contains the second Y sample in the LSBs and the first V (Cr) sample in the MSBs.</span></span>

<span data-ttu-id="d3e65-202">YUY2 est le format de pixel par défaut de 4:2:2 pour Microsoft DirectX Video Acceleration (DirectX VA).</span><span class="sxs-lookup"><span data-stu-id="d3e65-202">YUY2 is the preferred 4:2:2 pixel format for Microsoft DirectX Video Acceleration (DirectX VA).</span></span> <span data-ttu-id="d3e65-203">Il doit s’agir d’une exigence de terme intermédiaire pour les accélérateurs DirectX VA prenant en charge 4:2:2 vidéo.</span><span class="sxs-lookup"><span data-stu-id="d3e65-203">It is expected to be an intermediate-term requirement for DirectX VA accelerators supporting 4:2:2 video.</span></span>

### <a name="uyvy"></a><span data-ttu-id="d3e65-204">UYVY</span><span class="sxs-lookup"><span data-stu-id="d3e65-204">UYVY</span></span>

<span data-ttu-id="d3e65-205">Ce format est le même que le format YUY2, sauf que l’ordre d’octet est inversé, c’est-à-dire que les octets chrominance et luminance sont retournés (figure 4).</span><span class="sxs-lookup"><span data-stu-id="d3e65-205">This format is the same as the YUY2 format except the byte order is reversed—that is, the chroma and luma bytes are flipped (Figure 4).</span></span> <span data-ttu-id="d3e65-206">Si l’image est traitée comme un tableau de deux valeurs de **mot** Little-endian, le premier **mot** contient U dans LSBs et Y0 dans le MSBS, et le deuxième **mot** contient V dans LSBs et Y1 dans le MSBS.</span><span class="sxs-lookup"><span data-stu-id="d3e65-206">If the image is addressed as an array of two little-endian **WORD** values, the first **WORD** contains U in the LSBs and Y0 in the MSBs, and the second **WORD** contains V in the LSBs and Y1 in the MSBs.</span></span>

![Figure 4.](images/yuvformats03.gif)

## <a name="420-formats-16-bits-per-pixel"></a><span data-ttu-id="d3e65-209">4:2:0 formats, 16 bits par pixel</span><span class="sxs-lookup"><span data-stu-id="d3e65-209">4:2:0 Formats, 16 Bits per Pixel</span></span>

<span data-ttu-id="d3e65-210">Deux formats de 4:2:0 16 bits par pixel (BPP) sont recommandés, avec les Codes FOURCC suivants :</span><span class="sxs-lookup"><span data-stu-id="d3e65-210">Two 4:2:0 16-bits per pixel (bpp) formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="d3e65-211">IMC1</span><span class="sxs-lookup"><span data-stu-id="d3e65-211">IMC1</span></span>
-   <span data-ttu-id="d3e65-212">IMC3</span><span class="sxs-lookup"><span data-stu-id="d3e65-212">IMC3</span></span>

<span data-ttu-id="d3e65-213">Ces deux formats YUV sont des formats planaires.</span><span class="sxs-lookup"><span data-stu-id="d3e65-213">Both of these YUV formats are planar formats.</span></span> <span data-ttu-id="d3e65-214">Les canaux Chroma sont sous-échantillonnés par un facteur de deux dans les dimensions horizontales et verticales.</span><span class="sxs-lookup"><span data-stu-id="d3e65-214">The chroma channels are subsampled by a factor of two in both the horizontal and vertical dimensions.</span></span>

### <a name="imc1"></a><span data-ttu-id="d3e65-215">IMC1</span><span class="sxs-lookup"><span data-stu-id="d3e65-215">IMC1</span></span>

<span data-ttu-id="d3e65-216">Tous les échantillons Y apparaissent en premier dans la mémoire sous la forme d’un tableau de valeurs **char** non signées.</span><span class="sxs-lookup"><span data-stu-id="d3e65-216">All of the Y samples appear first in memory as an array of unsigned **char** values.</span></span> <span data-ttu-id="d3e65-217">Cela est suivi de tous les exemples V (CR), puis de tous les exemples U (CB).</span><span class="sxs-lookup"><span data-stu-id="d3e65-217">This is followed by all of the V (Cr) samples, and then all of the U (Cb) samples.</span></span> <span data-ttu-id="d3e65-218">Les plans V et U ont le même Stride que le plan Y, ce qui génère des zones de mémoire inutilisées, comme illustré à la figure 5.</span><span class="sxs-lookup"><span data-stu-id="d3e65-218">The V and U planes have the same stride as the Y plane, resulting in unused areas of memory, as shown in Figure 5.</span></span> <span data-ttu-id="d3e65-219">Les plans vous et V doivent commencer sur les limites de la mémoire qui sont un multiple de 16 lignes.</span><span class="sxs-lookup"><span data-stu-id="d3e65-219">The U and V planes must start on memory boundaries that are a multiple of 16 lines.</span></span> <span data-ttu-id="d3e65-220">La figure 5 illustre l’origine de vous et V pour une image vidéo 352 x 240.</span><span class="sxs-lookup"><span data-stu-id="d3e65-220">Figure 5 shows the origin of U and V for a 352 x 240 video frame.</span></span> <span data-ttu-id="d3e65-221">L’adresse de départ des plans vous et V est calculée comme suit :</span><span class="sxs-lookup"><span data-stu-id="d3e65-221">The starting address of the U and V planes are calculated as follows:</span></span>

``` syntax
BYTE* pV = pY + (((Height + 15) & ~15) * Stride);
BYTE* pU = pY + (((((Height * 3) / 2) + 15) & ~15) * Stride);
```

<span data-ttu-id="d3e65-222">où *py* est un pointeur d’octet vers le début du tableau de mémoire, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="d3e65-222">where *pY* is a byte pointer to the start of the memory array, as shown in the following diagram.</span></span>

![Figure 5.](images/yuvformats04.gif)

### <a name="imc3"></a><span data-ttu-id="d3e65-225">IMC3</span><span class="sxs-lookup"><span data-stu-id="d3e65-225">IMC3</span></span>

<span data-ttu-id="d3e65-226">Ce format est identique à IMC1, sauf que les plans vous et V sont permutés, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="d3e65-226">This format is identical to IMC1, except the U and V planes are swapped, as shown in the following diagram.</span></span>

![Figure 6.](images/yuvformats05.gif)

## <a name="420-formats-12-bits-per-pixel"></a><span data-ttu-id="d3e65-229">4:2:0 formats, 12 bits par pixel</span><span class="sxs-lookup"><span data-stu-id="d3e65-229">4:2:0 Formats, 12 Bits per Pixel</span></span>

<span data-ttu-id="d3e65-230">Quatre formats 4:2:0 12-BPP sont recommandés, avec les Codes FOURCC suivants :</span><span class="sxs-lookup"><span data-stu-id="d3e65-230">Four 4:2:0 12-bpp formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="d3e65-231">IMC2</span><span class="sxs-lookup"><span data-stu-id="d3e65-231">IMC2</span></span>
-   <span data-ttu-id="d3e65-232">IMC4</span><span class="sxs-lookup"><span data-stu-id="d3e65-232">IMC4</span></span>
-   <span data-ttu-id="d3e65-233">YV12</span><span class="sxs-lookup"><span data-stu-id="d3e65-233">YV12</span></span>
-   <span data-ttu-id="d3e65-234">NV12</span><span class="sxs-lookup"><span data-stu-id="d3e65-234">NV12</span></span>

<span data-ttu-id="d3e65-235">Dans tous ces formats, les canaux Chroma sont sous-échantillonnés par un facteur de deux dans les dimensions horizontales et verticales.</span><span class="sxs-lookup"><span data-stu-id="d3e65-235">In all of these formats, the chroma channels are subsampled by a factor of two in both the horizontal and vertical dimensions.</span></span>

### <a name="imc2"></a><span data-ttu-id="d3e65-236">IMC2</span><span class="sxs-lookup"><span data-stu-id="d3e65-236">IMC2</span></span>

<span data-ttu-id="d3e65-237">Ce format est le même que IMC1, à l’exception de la différence suivante : les lignes V (CR) et U (CB) sont entrelacées à des limites de demi-Stride.</span><span class="sxs-lookup"><span data-stu-id="d3e65-237">This format is the same as IMC1 except for the following difference: The V (Cr) and U (Cb) lines are interleaved at half-stride boundaries.</span></span> <span data-ttu-id="d3e65-238">En d’autres termes, chaque ligne complète de la zone Chroma commence par une ligne d’échantillons de V, suivie d’une ligne d’échantillons de U qui commence à la limite demi-Stride suivante (figure 7).</span><span class="sxs-lookup"><span data-stu-id="d3e65-238">In other words, each full-stride line in the chroma area starts with a line of V samples, followed by a line of U samples that begins at the next half-stride boundary (Figure 7).</span></span> <span data-ttu-id="d3e65-239">Cette disposition permet une utilisation plus efficace de l’espace d’adressage que IMC1.</span><span class="sxs-lookup"><span data-stu-id="d3e65-239">This layout makes more efficient use of address space than IMC1.</span></span> <span data-ttu-id="d3e65-240">Il coupe l’espace d’adressage chroma en moitié et, par conséquent, l’espace d’adressage total de 25%.</span><span class="sxs-lookup"><span data-stu-id="d3e65-240">It cuts the chroma address space in half, and thus the total address space by 25 percent.</span></span> <span data-ttu-id="d3e65-241">Parmi les formats 4:2:0, IMC2 est le second format préféré, après NV12.</span><span class="sxs-lookup"><span data-stu-id="d3e65-241">Among 4:2:0 formats, IMC2 is the second-most preferred format, after NV12.</span></span> <span data-ttu-id="d3e65-242">L’illustration suivante montre ce processus.</span><span class="sxs-lookup"><span data-stu-id="d3e65-242">The following image illustrates this process.</span></span>

![Figure 7.](images/yuvformats07.gif)

### <a name="imc4"></a><span data-ttu-id="d3e65-245">IMC4</span><span class="sxs-lookup"><span data-stu-id="d3e65-245">IMC4</span></span>

<span data-ttu-id="d3e65-246">Ce format est identique à IMC2, sauf que les lignes U (CB) et V (CR) sont échangées, comme le montre l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d3e65-246">This format is identical to IMC2, except the U (Cb) and V (Cr) lines are swapped, as shown in the following illustration.</span></span>

![Figure 8.](images/yuvformats06.gif)

### <a name="yv12"></a><span data-ttu-id="d3e65-249">YV12</span><span class="sxs-lookup"><span data-stu-id="d3e65-249">YV12</span></span>

<span data-ttu-id="d3e65-250">Tous les échantillons Y apparaissent en premier dans la mémoire sous la forme d’un tableau de valeurs **char** non signées.</span><span class="sxs-lookup"><span data-stu-id="d3e65-250">All of the Y samples appear first in memory as an array of unsigned **char** values.</span></span> <span data-ttu-id="d3e65-251">Ce tableau est immédiatement suivi par tous les exemples V (CR).</span><span class="sxs-lookup"><span data-stu-id="d3e65-251">This array is followed immediately by all of the V (Cr) samples.</span></span> <span data-ttu-id="d3e65-252">Le Stride du plan V est la moitié du plan Y. et le plan V contient deux fois plus de lignes que le plan Y.</span><span class="sxs-lookup"><span data-stu-id="d3e65-252">The stride of the V plane is half the stride of the Y plane; and the V plane contains half as many lines as the Y plane.</span></span> <span data-ttu-id="d3e65-253">Le plan V est immédiatement suivi par tous les exemples U (CB), avec les mêmes Stride et nombre de lignes que le plan V, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d3e65-253">The V plane is followed immediately by all of the U (Cb) samples, with the same stride and number of lines as the V plane, as shown in the following illustration.</span></span>

![Figure 9.](images/yuvformats08.gif)

### <a name="nv12"></a><span data-ttu-id="d3e65-256">NV12</span><span class="sxs-lookup"><span data-stu-id="d3e65-256">NV12</span></span>

<span data-ttu-id="d3e65-257">Tous les échantillons Y apparaissent en premier dans la mémoire sous la forme d’un tableau de valeurs **char** non signées avec un nombre pair de lignes.</span><span class="sxs-lookup"><span data-stu-id="d3e65-257">All of the Y samples appear first in memory as an array of unsigned **char** values with an even number of lines.</span></span> <span data-ttu-id="d3e65-258">Le plan Y est immédiatement suivi d’un tableau de valeurs **char** non signées qui contient des exemples empaquetés U (CB) et V (CR).</span><span class="sxs-lookup"><span data-stu-id="d3e65-258">The Y plane is followed immediately by an array of unsigned **char** values that contains packed U (Cb) and V (Cr) samples.</span></span> <span data-ttu-id="d3e65-259">Quand le tableau U-V combiné est adressé sous la forme d’un tableau de valeurs de **mot** Little-endian, LSBs contient les valeurs U et MSBS contient les valeurs V.</span><span class="sxs-lookup"><span data-stu-id="d3e65-259">When the combined U-V array is addressed as an array of little-endian **WORD** values, the LSBs contain the U values, and the MSBs contain the V values.</span></span> <span data-ttu-id="d3e65-260">NV12 est le format de pixel par défaut de 4:2:0 pour DirectX VA.</span><span class="sxs-lookup"><span data-stu-id="d3e65-260">NV12 is the preferred 4:2:0 pixel format for DirectX VA.</span></span> <span data-ttu-id="d3e65-261">Il doit s’agir d’une exigence de terme intermédiaire pour les accélérateurs DirectX VA prenant en charge 4:2:0 vidéo.</span><span class="sxs-lookup"><span data-stu-id="d3e65-261">It is expected to be an intermediate-term requirement for DirectX VA accelerators supporting 4:2:0 video.</span></span> <span data-ttu-id="d3e65-262">L’illustration suivante montre le plan Y et le tableau contenant les exemples empaquetés et V.</span><span class="sxs-lookup"><span data-stu-id="d3e65-262">The following illustration shows the Y plane and the array that contains packed U and V samples.</span></span>

![Figure 10.](images/yuvformats09.gif)

## <a name="color-space-and-chroma-sampling-rate-conversions"></a><span data-ttu-id="d3e65-265">Conversions de l’espace colorimétrique et du taux d’échantillonnage Chroma</span><span class="sxs-lookup"><span data-stu-id="d3e65-265">Color Space and Chroma Sampling Rate Conversions</span></span>

<span data-ttu-id="d3e65-266">Cette section fournit des instructions pour la conversion entre YUV et RVB, et pour la conversion entre différents formats YUV.</span><span class="sxs-lookup"><span data-stu-id="d3e65-266">This section provides guidelines for converting between YUV and RGB, and for converting between some different YUV formats.</span></span> <span data-ttu-id="d3e65-267">Nous considérons deux schémas d’encodage RVB dans cette section : RVB d' *ordinateur 8 bits*, également connu sous le nom de RVB ou « RGB à l’échelle complète », et *vidéo de Studio Video RGB*, ou « RVB avec la salle de tête et la salle de remontée ».</span><span class="sxs-lookup"><span data-stu-id="d3e65-267">We consider two RGB encoding schemes in this section: *8-bit computer RGB*, also known as sRGB or "full-scale" RGB, and *studio video RGB*, or "RGB with head-room and toe-room."</span></span> <span data-ttu-id="d3e65-268">Ceux-ci sont définis comme suit :</span><span class="sxs-lookup"><span data-stu-id="d3e65-268">These are defined as follows:</span></span>

-   <span data-ttu-id="d3e65-269">L’ordinateur RGB utilise 8 bits pour chaque échantillon de rouge, vert et bleu.</span><span class="sxs-lookup"><span data-stu-id="d3e65-269">Computer RGB uses 8 bits for each sample of red, green, and blue.</span></span> <span data-ttu-id="d3e65-270">Le noir est représenté par R = G = B = 0 et le blanc est représenté par R = G = B = 255.</span><span class="sxs-lookup"><span data-stu-id="d3e65-270">Black is represented by R = G = B = 0, and white is represented by R = G = B = 255.</span></span>
-   <span data-ttu-id="d3e65-271">Studio Video RGB utilise un nombre de bits N pour chaque échantillon de rouge, vert et bleu, où N est supérieur ou supérieur à 8.</span><span class="sxs-lookup"><span data-stu-id="d3e65-271">Studio video RGB uses some number of bits N for each sample of red, green, and blue, where N is 8 or more.</span></span> <span data-ttu-id="d3e65-272">Studio Video RGB utilise un facteur d’échelle différent de celui de l’ordinateur RGB et un décalage.</span><span class="sxs-lookup"><span data-stu-id="d3e65-272">Studio video RGB uses a different scaling factor than computer RGB, and it has an offset.</span></span> <span data-ttu-id="d3e65-273">Le noir est représenté par R = G = B = 16 \* 2 ^ (N-8) et le blanc est représenté par R = G = B = 235 \* 2 ^ (n-8).</span><span class="sxs-lookup"><span data-stu-id="d3e65-273">Black is represented by R = G = B = 16\*2^(N-8), and white is represented by R = G = B = 235\*2^(N-8).</span></span> <span data-ttu-id="d3e65-274">Toutefois, les valeurs réelles peuvent ne pas être comprises dans cette plage.</span><span class="sxs-lookup"><span data-stu-id="d3e65-274">However, actual values may fall outside this range.</span></span>

<span data-ttu-id="d3e65-275">Studio Video RGB est la définition RVB préférée pour la vidéo dans Windows, tandis que l’ordinateur RGB est la définition RVB préférée pour les applications non vidéo.</span><span class="sxs-lookup"><span data-stu-id="d3e65-275">Studio video RGB is the preferred RGB definition for video in Windows, while computer RGB is the preferred RGB definition for non-video applications.</span></span> <span data-ttu-id="d3e65-276">Quelle que soit la forme RVB, les coordonnées chromatiques sont spécifiées dans ITU-R BT. 709 pour la définition des couleurs primaires RVB.</span><span class="sxs-lookup"><span data-stu-id="d3e65-276">In either form of RGB, the chromaticity coordinates are as specified in ITU-R BT.709 for the definition of the RGB color primaries.</span></span> <span data-ttu-id="d3e65-277">Les coordonnées (x, y) de R, G et B sont (0,64, 0,33), (0,30, 0,60) et (0,15, 0,06), respectivement.</span><span class="sxs-lookup"><span data-stu-id="d3e65-277">The (x,y) coordinates of R, G, and B are (0.64, 0.33), (0.30, 0.60), and (0.15, 0.06), respectively.</span></span> <span data-ttu-id="d3e65-278">Le blanc de référence est D65 avec les coordonnées (0,3127, 0,3290).</span><span class="sxs-lookup"><span data-stu-id="d3e65-278">Reference white is D65 with coordinates (0.3127, 0.3290).</span></span> <span data-ttu-id="d3e65-279">La gamma nominal est de 1/0.45 (environ 2,2), avec un gamma précis défini en détail dans ITU-R BT. 709.</span><span class="sxs-lookup"><span data-stu-id="d3e65-279">Nominal gamma is 1/0.45 (approximately 2.2), with precise gamma defined in detail in ITU-R BT.709.</span></span>

<span data-ttu-id="d3e65-280">**Conversion entre RGB et 4:4:4 YUV**</span><span class="sxs-lookup"><span data-stu-id="d3e65-280">**Conversion between RGB and 4:4:4 YUV**</span></span>

<span data-ttu-id="d3e65-281">Nous commençons par décrire la conversion entre RVB et 4:4:4 YUV.</span><span class="sxs-lookup"><span data-stu-id="d3e65-281">We first describe conversion between RGB and 4:4:4 YUV.</span></span> <span data-ttu-id="d3e65-282">Pour convertir 4:2:0 ou 4:2:2 YUV en RGB, nous vous recommandons de convertir les données YUV en 4:4:4 YUV, puis de convertir de 4:4:4 YUV en RVB.</span><span class="sxs-lookup"><span data-stu-id="d3e65-282">To convert 4:2:0 or 4:2:2 YUV to RGB, we recommend converting the YUV data to 4:4:4 YUV, and then converting from 4:4:4 YUV to RGB.</span></span> <span data-ttu-id="d3e65-283">Le format AYUV, qui est un format 4:4:4, utilise 8 bits chacun pour les exemples Y, U et V.</span><span class="sxs-lookup"><span data-stu-id="d3e65-283">The AYUV format, which is a 4:4:4 format, uses 8 bits each for the Y, U, and V samples.</span></span> <span data-ttu-id="d3e65-284">Les YUV peuvent également être définis à l’aide de plus de 8 bits par échantillon pour certaines applications.</span><span class="sxs-lookup"><span data-stu-id="d3e65-284">YUV can also be defined using more than 8 bits per sample for some applications.</span></span>

<span data-ttu-id="d3e65-285">Deux conversions YUV dominantes de RGB ont été définies pour la vidéo numérique.</span><span class="sxs-lookup"><span data-stu-id="d3e65-285">Two dominant YUV conversions from RGB have been defined for digital video.</span></span> <span data-ttu-id="d3e65-286">Les deux reposent sur la spécification connue sous le nom de recommandation ITU-R BT. 709.</span><span class="sxs-lookup"><span data-stu-id="d3e65-286">Both are based on the specification known as ITU-R Recommendation BT.709.</span></span> <span data-ttu-id="d3e65-287">La première conversion est l’ancienne forme YUV définie pour une utilisation de 50 Hz dans BT. 709.</span><span class="sxs-lookup"><span data-stu-id="d3e65-287">The first conversion is the older YUV form defined for 50-Hz use in BT.709.</span></span> <span data-ttu-id="d3e65-288">Il est identique à la relation spécifiée dans la recommandation ITU-R BT. 601, également connue par son ancien nom, CCIR 601.</span><span class="sxs-lookup"><span data-stu-id="d3e65-288">It is the same as the relation specified in ITU-R Recommendation BT.601, also known by its older name, CCIR 601.</span></span> <span data-ttu-id="d3e65-289">Il doit être considéré comme le format YUV préféré pour la résolution TV de définition standard (720 x 576) et la vidéo de faible résolution.</span><span class="sxs-lookup"><span data-stu-id="d3e65-289">It should be considered the preferred YUV format for standard-definition TV resolution (720 x 576) and lower-resolution video.</span></span> <span data-ttu-id="d3e65-290">Il est caractérisé par les valeurs de deux constantes *KR* et *KB*:</span><span class="sxs-lookup"><span data-stu-id="d3e65-290">It is characterized by the values of two constants *Kr* and *Kb*:</span></span>

``` syntax
Kr = 0.299
Kb = 0.114
```

<span data-ttu-id="d3e65-291">La deuxième conversion est le formulaire YUV plus récent défini pour une utilisation de 60 Hz dans BT. 709 et doit être considéré comme le format préféré pour les résolutions vidéo au-dessus de SDTV.</span><span class="sxs-lookup"><span data-stu-id="d3e65-291">The second conversion is the newer YUV form defined for 60-Hz use in BT.709, and should be considered the preferred format for video resolutions above SDTV.</span></span> <span data-ttu-id="d3e65-292">Elle est caractérisée par différentes valeurs pour ces deux constantes :</span><span class="sxs-lookup"><span data-stu-id="d3e65-292">It is characterized by different values for these two constants:</span></span>

``` syntax
Kr = 0.2126
Kb = 0.0722
```

<span data-ttu-id="d3e65-293">La conversion de RVB en YUV est définie à partir de ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="d3e65-293">Conversion from RGB to YUV is defined by starting with the following:</span></span>

``` syntax
L = Kr * R + Kb * B + (1 - Kr - Kb) * G
```

<span data-ttu-id="d3e65-294">Les valeurs YUV sont ensuite obtenues comme suit :</span><span class="sxs-lookup"><span data-stu-id="d3e65-294">The YUV values are then obtained as follows:</span></span>

``` syntax
Y =                   floor(2^(M-8) * (219*(L-Z)/S + 16) + 0.5)
U = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(B-L) / ((1-Kb)*S) + 128) + 0.5))
V = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(R-L) / ((1-Kr)*S) + 128) + 0.5))
```

<span data-ttu-id="d3e65-295">where</span><span class="sxs-lookup"><span data-stu-id="d3e65-295">where</span></span>

-   <span data-ttu-id="d3e65-296">M est le nombre de bits par échantillon YUV (M >= 8).</span><span class="sxs-lookup"><span data-stu-id="d3e65-296">M is the number of bits per YUV sample (M >= 8).</span></span>
-   <span data-ttu-id="d3e65-297">Z est la variable de niveau noir.</span><span class="sxs-lookup"><span data-stu-id="d3e65-297">Z is the black-level variable.</span></span> <span data-ttu-id="d3e65-298">Pour l’ordinateur RGB, Z est égal à 0.</span><span class="sxs-lookup"><span data-stu-id="d3e65-298">For computer RGB, Z equals 0.</span></span> <span data-ttu-id="d3e65-299">Pour Studio Video RGB, Z est égal à 16 \* 2 ^ (n-8), où N est le nombre de bits par échantillon RVB (n >= 8).</span><span class="sxs-lookup"><span data-stu-id="d3e65-299">For studio video RGB, Z equals 16\*2^(N-8), where N is the number of bits per RGB sample (N >= 8).</span></span>
-   <span data-ttu-id="d3e65-300">S est la variable de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="d3e65-300">S is the scaling variable.</span></span> <span data-ttu-id="d3e65-301">Pour l’ordinateur RGB, S est égal à 255.</span><span class="sxs-lookup"><span data-stu-id="d3e65-301">For computer RGB, S equals 255.</span></span> <span data-ttu-id="d3e65-302">Pour Studio Video Video RGB, S est égal à 219 \* 2 ^ (N-8).</span><span class="sxs-lookup"><span data-stu-id="d3e65-302">For studio video RGB, S equals 219\*2^(N-8).</span></span>

<span data-ttu-id="d3e65-303">La fonction Floor (x) retourne le plus grand entier inférieur ou égal à x.</span><span class="sxs-lookup"><span data-stu-id="d3e65-303">The function floor(x) returns the largest integer less than or equal to x.</span></span> <span data-ttu-id="d3e65-304">La fonction Clip3 (x, y, z) est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="d3e65-304">The function clip3(x, y, z) is defined as follows:</span></span>

``` syntax
clip3(x, y, z) = ((z < x) ? x : ((z > y) ? y : z))
```

> [!Note]  
> <span data-ttu-id="d3e65-305">Clip3 doit être implémenté en tant que fonction plutôt qu’en tant que macro de préprocesseur ; dans le cas contraire, plusieurs évaluations des arguments se produisent.</span><span class="sxs-lookup"><span data-stu-id="d3e65-305">clip3 should be implemented as a function rather than a preprocessor macro; otherwise multiple evaluations of the arguments will occur.</span></span>

 

<span data-ttu-id="d3e65-306">L’échantillon Y représente la luminosité et les exemples vous et V représentent les écarts de couleur par rapport au bleu et au rouge, respectivement.</span><span class="sxs-lookup"><span data-stu-id="d3e65-306">The Y sample represents brightness, and the U and V samples represent the color deviations toward blue and red, respectively.</span></span> <span data-ttu-id="d3e65-307">La plage nominale pour Y est 16 \* 2 ^ (m-8) à 235 \* 2 ^ (m-8).</span><span class="sxs-lookup"><span data-stu-id="d3e65-307">The nominal range for Y is 16\*2^(M-8) to 235\*2^(M-8).</span></span> <span data-ttu-id="d3e65-308">Le noir est représenté sous la forme 16 \* 2 ^ (m-8) et le blanc est représenté sous la forme 235 \* 2 ^ (m-8).</span><span class="sxs-lookup"><span data-stu-id="d3e65-308">Black is represented as 16\*2^(M-8), and white is represented as 235\*2^(M-8).</span></span> <span data-ttu-id="d3e65-309">La plage nominale pour vous et V est comprise entre 16 \* 2 ^ (m-8) et 240 \* 2 ^ (m-8), avec la valeur 128 \* 2 ^ (m-8) représentant le Chroma neutre.</span><span class="sxs-lookup"><span data-stu-id="d3e65-309">The nominal range for U and V are 16\*2^(M-8) to 240\*2^(M-8), with the value 128\*2^(M-8) representing neutral chroma.</span></span> <span data-ttu-id="d3e65-310">Toutefois, les valeurs réelles peuvent être en dehors de ces plages.</span><span class="sxs-lookup"><span data-stu-id="d3e65-310">However, actual values may fall outside these ranges.</span></span>

<span data-ttu-id="d3e65-311">Pour les données d’entrée sous la forme Studio Video RGB, l’opération clip est nécessaire pour conserver les valeurs vous et V dans la plage 0 à (2 ^ M)-1.</span><span class="sxs-lookup"><span data-stu-id="d3e65-311">For input data in the form of studio video RGB, the clip operation is necessary to keep the U and V values within the range 0 to (2^M)-1.</span></span> <span data-ttu-id="d3e65-312">Si l’entrée est Computer RGB, l’opération de découpage n’est pas nécessaire, car la formule de conversion ne peut pas produire de valeurs en dehors de cette plage.</span><span class="sxs-lookup"><span data-stu-id="d3e65-312">If the input is computer RGB, the clip operation is not required, because the conversion formula cannot produce values outside of this range.</span></span>

<span data-ttu-id="d3e65-313">Il s’agit des formules exactes sans approximation.</span><span class="sxs-lookup"><span data-stu-id="d3e65-313">These are the exact formulas without approximation.</span></span> <span data-ttu-id="d3e65-314">Tout ce qui suit dans ce document est dérivé de ces formules.</span><span class="sxs-lookup"><span data-stu-id="d3e65-314">Everything that follows in this document is derived from these formulas.</span></span> <span data-ttu-id="d3e65-315">Cette section décrit les conversions suivantes :</span><span class="sxs-lookup"><span data-stu-id="d3e65-315">This section describes the following conversions:</span></span>

-   [<span data-ttu-id="d3e65-316">Conversion de RGB888 en YUV 4:4:4</span><span class="sxs-lookup"><span data-stu-id="d3e65-316">Converting RGB888 to YUV 4:4:4</span></span>](#converting-rgb888-to-yuv-444)
-   [<span data-ttu-id="d3e65-317">Conversion de YUV de 8 bits en RGB888</span><span class="sxs-lookup"><span data-stu-id="d3e65-317">Converting 8-bit YUV to RGB888</span></span>](#converting-8-bit-yuv-to-rgb888)
-   [<span data-ttu-id="d3e65-318">Conversion de 4:2:0 YUV en 4:2:2 YUV</span><span class="sxs-lookup"><span data-stu-id="d3e65-318">Converting 4:2:0 YUV to 4:2:2 YUV</span></span>](#converting-420-yuv-to-422-yuv)
-   [<span data-ttu-id="d3e65-319">Conversion de 4:2:2 YUV en 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="d3e65-319">Converting 4:2:2 YUV to 4:4:4 YUV</span></span>](#converting-422-yuv-to-444-yuv)
-   [<span data-ttu-id="d3e65-320">Conversion de 4:2:0 YUV en 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="d3e65-320">Converting 4:2:0 YUV to 4:4:4 YUV</span></span>](#converting-420-yuv-to-444-yuv)

## <a name="converting-rgb888-to-yuv-444"></a><span data-ttu-id="d3e65-321">Conversion de RGB888 en YUV 4:4:4</span><span class="sxs-lookup"><span data-stu-id="d3e65-321">Converting RGB888 to YUV 4:4:4</span></span>

<span data-ttu-id="d3e65-322">Dans le cas d’une entrée d’ordinateur RVB et de la sortie BT. 601 à 8 bits, nous pensons que les formules fournies dans la section précédente peuvent être raisonnablement approximatives par les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d3e65-322">In the case of computer RGB input and 8-bit BT.601 YUV output, we believe that the formulas given in the previous section can be reasonably approximated by the following:</span></span>

``` syntax
Y = ( (  66 * R + 129 * G +  25 * B + 128) >> 8) +  16
U = ( ( -38 * R -  74 * G + 112 * B + 128) >> 8) + 128
V = ( ( 112 * R -  94 * G -  18 * B + 128) >> 8) + 128
```

<span data-ttu-id="d3e65-323">Ces formules produisent des résultats 8 bits utilisant des coefficients qui ne nécessitent pas plus de 8 bits de précision (non signée).</span><span class="sxs-lookup"><span data-stu-id="d3e65-323">These formulas produce 8-bit results using coefficients that require no more than 8 bits of (unsigned) precision.</span></span> <span data-ttu-id="d3e65-324">Les résultats intermédiaires requièrent jusqu’à 16 bits de précision.</span><span class="sxs-lookup"><span data-stu-id="d3e65-324">Intermediate results will require up to 16 bits of precision.</span></span>

## <a name="converting-8-bit-yuv-to-rgb888"></a><span data-ttu-id="d3e65-325">Conversion de YUV de 8 bits en RGB888</span><span class="sxs-lookup"><span data-stu-id="d3e65-325">Converting 8-bit YUV to RGB888</span></span>

<span data-ttu-id="d3e65-326">À partir des formules RVB-à-YUV d’origine, il est possible de dériver les relations suivantes pour BT. 601.</span><span class="sxs-lookup"><span data-stu-id="d3e65-326">From the original RGB-to-YUV formulas, one can derive the following relationships for BT.601.</span></span>

``` syntax
Y = round( 0.256788 * R + 0.504129 * G + 0.097906 * B) +  16 
U = round(-0.148223 * R - 0.290993 * G + 0.439216 * B) + 128
V = round( 0.439216 * R - 0.367788 * G - 0.071427 * B) + 128
```

<span data-ttu-id="d3e65-327">Par conséquent, étant donné :</span><span class="sxs-lookup"><span data-stu-id="d3e65-327">Therefore, given:</span></span>

``` syntax
C = Y - 16
D = U - 128
E = V - 128
```

<span data-ttu-id="d3e65-328">les formules permettant de convertir YUV en RGB peuvent être dérivées comme suit :</span><span class="sxs-lookup"><span data-stu-id="d3e65-328">the formulas to convert YUV to RGB can be derived as follows:</span></span>

``` syntax
R = clip( round( 1.164383 * C                   + 1.596027 * E  ) )
G = clip( round( 1.164383 * C - (0.391762 * D) - (0.812968 * E) ) )
B = clip( round( 1.164383 * C +  2.017232 * D                   ) )
```

<span data-ttu-id="d3e65-329">où `clip()` dénote le découpage dans une plage de \[ 0.. 255 \] .</span><span class="sxs-lookup"><span data-stu-id="d3e65-329">where `clip()` denotes clipping to a range of \[0..255\].</span></span> <span data-ttu-id="d3e65-330">Nous pensons que ces formules peuvent être raisonnablement approximatives par les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d3e65-330">We believe these formulas can be reasonably approximated by the following:</span></span>

``` syntax
R = clip(( 298 * C           + 409 * E + 128) >> 8)
G = clip(( 298 * C - 100 * D - 208 * E + 128) >> 8)
B = clip(( 298 * C + 516 * D           + 128) >> 8)
```

<span data-ttu-id="d3e65-331">Ces formules utilisent des coefficients qui requièrent plus de 8 bits de précision pour produire chaque résultat de 8 bits, et les résultats intermédiaires nécessitent plus de 16 bits de précision.</span><span class="sxs-lookup"><span data-stu-id="d3e65-331">These formulas use some coefficients that require more than 8 bits of precision to produce each 8-bit result, and intermediate results will require more than 16 bits of precision.</span></span>

<span data-ttu-id="d3e65-332">Pour convertir 4:2:0 ou 4:2:2 YUV en RGB, nous vous recommandons de convertir les données YUV en 4:4:4 YUV, puis de convertir de 4:4:4 YUV en RVB.</span><span class="sxs-lookup"><span data-stu-id="d3e65-332">To convert 4:2:0 or 4:2:2 YUV to RGB, we recommend converting the YUV data to 4:4:4 YUV, and then converting from 4:4:4 YUV to RGB.</span></span> <span data-ttu-id="d3e65-333">Les sections qui suivent présentent certaines méthodes pour convertir les formats 4:2:0 et 4:2:2 à 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="d3e65-333">The sections that follow present some methods for converting 4:2:0 and 4:2:2 formats to 4:4:4.</span></span>

## <a name="converting-420-yuv-to-422-yuv"></a><span data-ttu-id="d3e65-334">Conversion de 4:2:0 YUV en 4:2:2 YUV</span><span class="sxs-lookup"><span data-stu-id="d3e65-334">Converting 4:2:0 YUV to 4:2:2 YUV</span></span>

<span data-ttu-id="d3e65-335">La conversion de 4:2:0 YUV en 4:2:2 YUV requiert une conversion verticale par un facteur de deux.</span><span class="sxs-lookup"><span data-stu-id="d3e65-335">Converting 4:2:0 YUV to 4:2:2 YUV requires vertical upconversion by a factor of two.</span></span> <span data-ttu-id="d3e65-336">Cette section décrit un exemple de méthode pour effectuer la conversion.</span><span class="sxs-lookup"><span data-stu-id="d3e65-336">This section describes an example method for performing the upconversion.</span></span> <span data-ttu-id="d3e65-337">La méthode suppose que les images vidéo sont une analyse progressive.</span><span class="sxs-lookup"><span data-stu-id="d3e65-337">The method assumes that the video pictures are progressive scan.</span></span>

> [!Note]  
> <span data-ttu-id="d3e65-338">Le processus de conversion d’analyse entrelacée de 4:2:0 à 4:2:2 présente des problèmes atypiques et est difficile à implémenter.</span><span class="sxs-lookup"><span data-stu-id="d3e65-338">The 4:2:0 to 4:2:2 interlaced scan conversion process presents atypical problems and is difficult to implement.</span></span> <span data-ttu-id="d3e65-339">Cet article ne traite pas du problème de conversion de l’analyse entrelacée de 4:2:0 à 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="d3e65-339">This article does not address the issue of converting interlaced scan from 4:2:0 to 4:2:2.</span></span>

 

<span data-ttu-id="d3e65-340">Laissez chaque ligne verticale d’échantillons de chrominance d’entrée être un tableau qui est compris `Cin[]` entre 0 et N-1.</span><span class="sxs-lookup"><span data-stu-id="d3e65-340">Let each vertical line of input chroma samples be an array `Cin[]` that ranges from 0 to N - 1.</span></span> <span data-ttu-id="d3e65-341">La ligne verticale correspondante sur l’image de sortie est un tableau `Cout[]` qui est compris entre 0 et 2n-1.</span><span class="sxs-lookup"><span data-stu-id="d3e65-341">The corresponding vertical line on the output image will be an array `Cout[]` that ranges from 0 to 2N - 1.</span></span> <span data-ttu-id="d3e65-342">Pour convertir chaque ligne verticale, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="d3e65-342">To convert each vertical line, perform the following process:</span></span>

``` syntax
Cout[0]     = Cin[0];
Cout[1]     = clip((9 * (Cin[0] + Cin[1]) - (Cin[0] + Cin[2]) + 8) >> 4);
Cout[2]     = Cin[1];
Cout[3]     = clip((9 * (Cin[1] + Cin[2]) - (Cin[0] + Cin[3]) + 8) >> 4);
Cout[4]     = Cin[2]
Cout[5]     = clip((9 * (Cin[2] + Cin[3]) - (Cin[1] + Cin[4]) + 8) >> 4);
...
Cout[2*i]   = Cin[i]
Cout[2*i+1] = clip((9 * (Cin[i] + Cin[i+1]) - (Cin[i-1] + Cin[i+2]) + 8) >> 4);
...
Cout[2*N-3] = clip((9 * (Cin[N-2] + Cin[N-1]) - (Cin[N-3] + Cin[N-1]) + 8) >> 4);
Cout[2*N-2] = Cin[N-1];
Cout[2*N-1] = clip((9 * (Cin[N-1] + Cin[N-1]) - (Cin[N-2] + Cin[N-1]) + 8) >> 4);
```

<span data-ttu-id="d3e65-343">où clip () désigne le découpage dans une plage de \[ 0.. 255 \] .</span><span class="sxs-lookup"><span data-stu-id="d3e65-343">where clip() denotes clipping to a range of \[0..255\].</span></span>

> [!Note]  
> <span data-ttu-id="d3e65-344">Les équations permettant de gérer les bords peuvent être simplifiées de façon mathématique.</span><span class="sxs-lookup"><span data-stu-id="d3e65-344">The equations for handling the edges can be mathematically simplified.</span></span> <span data-ttu-id="d3e65-345">Ils sont présentés dans ce formulaire pour illustrer l’effet de verrouillage aux bords de l’image.</span><span class="sxs-lookup"><span data-stu-id="d3e65-345">They are shown in this form to illustrate the clamping effect at the edges of the picture.</span></span>

 

<span data-ttu-id="d3e65-346">En effet, cette méthode calcule chaque valeur manquante en interpolant la courbe sur les quatre pixels adjacents, pondérée vers les valeurs des deux pixels les plus proches (figure 11).</span><span class="sxs-lookup"><span data-stu-id="d3e65-346">In effect, this method calculates each missing value by interpolating the curve over the four adjacent pixels, weighted toward the values of the two nearest pixels (Figure 11).</span></span> <span data-ttu-id="d3e65-347">La méthode d’interpolation spécifique utilisée dans cet exemple génère des échantillons manquants à des positions semi-entières à l’aide d’une méthode connue appelée Catmull-Rom interpolation, également appelée interpolation de convolution cubique.</span><span class="sxs-lookup"><span data-stu-id="d3e65-347">The specific interpolation method used in this example generates missing samples at half-integer positions using a well-known method called Catmull-Rom interpolation, also known as cubic convolution interpolation.</span></span>

![Figure 11.](images/yuvformats14.gif)

<span data-ttu-id="d3e65-350">Dans les termes du traitement des signaux, la conversion verticale doit idéalement inclure une compensation de décalage de phase pour tenir compte du décalage vertical de demi-pixel (par rapport à la grille d’échantillonnage 4:2:2 de sortie) entre les emplacements des exemples de lignes 4:2:0 et l’emplacement de chaque autre ligne d’exemple 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="d3e65-350">In signal processing terms, the vertical upconversion should ideally include a phase shift compensation to account for the half-pixel vertical offset (relative to the output 4:2:2 sampling grid) between the locations of the 4:2:0 sample lines and the location of every other 4:2:2 sample line.</span></span> <span data-ttu-id="d3e65-351">Toutefois, l’introduction de ce décalage augmenterait la quantité de traitement nécessaire pour générer les exemples, et rendra impossible la reconstruction des exemples 4:2:0 originaux à partir de l’image 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="d3e65-351">However, introducing this offset would increase the amount of processing required to generate the samples, and make it impossible to reconstruct the original 4:2:0 samples from the upsampled 4:2:2 image.</span></span> <span data-ttu-id="d3e65-352">Il serait également impossible de décoder la vidéo directement en surfaces 4:2:2, puis d’utiliser ces surfaces comme images de référence pour décoder les images suivantes dans le flux.</span><span class="sxs-lookup"><span data-stu-id="d3e65-352">It would also make it impossible to decode video directly into 4:2:2 surfaces and then use those surfaces as reference pictures for decoding subsequent pictures in the stream.</span></span> <span data-ttu-id="d3e65-353">Par conséquent, la méthode fournie ici ne prend pas en compte l’alignement vertical précis des exemples.</span><span class="sxs-lookup"><span data-stu-id="d3e65-353">Therefore, the method provided here does not take into account the precise vertical alignment of the samples.</span></span> <span data-ttu-id="d3e65-354">Cela n’est probablement pas nuisible visuellement à des résolutions d’image relativement élevées.</span><span class="sxs-lookup"><span data-stu-id="d3e65-354">Doing so is probably not visually harmful at reasonably high picture resolutions.</span></span>

<span data-ttu-id="d3e65-355">Si vous commencez avec la vidéo 4:2:0 qui utilise la grille d’échantillonnage définie dans H. 261, H. 263 ou MPEG-1 Video, la phase de l’échantillon de couleur 4:2:2 de sortie est également décalée d’un décalage horizontal 4:2:2 de demi-pixel par rapport à l’espacement sur la grille d’échantillonnage de luminance</span><span class="sxs-lookup"><span data-stu-id="d3e65-355">If you start with 4:2:0 video that uses the sampling grid defined in H.261, H.263, or MPEG-1 video, the phase of the output 4:2:2 chroma samples will also be shifted by a half-pixel horizontal offset relative to the spacing on the luma sampling grid (a quarter-pixel offset relative to the spacing of the 4:2:2 chroma sampling grid).</span></span> <span data-ttu-id="d3e65-356">Toutefois, la forme MPEG-2 de 4:2:0 vidéo est probablement plus couramment utilisée sur les PC et ne subit pas de problème.</span><span class="sxs-lookup"><span data-stu-id="d3e65-356">However, the MPEG-2 form of 4:2:0 video is probably more commonly used on PCs and does not suffer from this problem.</span></span> <span data-ttu-id="d3e65-357">En outre, la distinction n’est probablement pas dangereuse visuellement à des résolutions d’image relativement élevées.</span><span class="sxs-lookup"><span data-stu-id="d3e65-357">Moreover, the distinction is probably not visually harmful at reasonably high picture resolutions.</span></span> <span data-ttu-id="d3e65-358">Si vous tentez de corriger ce problème, vous créerez le même type de problème que celui traité pour le décalage vertical de la phase.</span><span class="sxs-lookup"><span data-stu-id="d3e65-358">Trying to correct for this problem would create the same sort of problems discussed for the vertical phase offset.</span></span>

## <a name="converting-422-yuv-to-444-yuv"></a><span data-ttu-id="d3e65-359">Conversion de 4:2:2 YUV en 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="d3e65-359">Converting 4:2:2 YUV to 4:4:4 YUV</span></span>

<span data-ttu-id="d3e65-360">La conversion de 4:2:2 YUV en 4:4:4 YUV requiert une conversion horizontale d’un facteur de deux.</span><span class="sxs-lookup"><span data-stu-id="d3e65-360">Converting 4:2:2 YUV to 4:4:4 YUV requires horizontal upconversion by a factor of two.</span></span> <span data-ttu-id="d3e65-361">La méthode décrite précédemment pour la conversion verticale peut également être appliquée à la conversion horizontale.</span><span class="sxs-lookup"><span data-stu-id="d3e65-361">The method described previously for vertical upconversion can also be applied to horizontal upconversion.</span></span> <span data-ttu-id="d3e65-362">Pour les vidéos MPEG-2 et ITU-R BT. 601, cette méthode produira des exemples avec l’alignement de phase approprié.</span><span class="sxs-lookup"><span data-stu-id="d3e65-362">For MPEG-2 and ITU-R BT.601 video, this method will produce samples with the correct phase alignment.</span></span>

## <a name="converting-420-yuv-to-444-yuv"></a><span data-ttu-id="d3e65-363">Conversion de 4:2:0 YUV en 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="d3e65-363">Converting 4:2:0 YUV to 4:4:4 YUV</span></span>

<span data-ttu-id="d3e65-364">Pour convertir 4:2:0 YUV en 4:4:4 YUV, vous pouvez simplement suivre les deux méthodes décrites précédemment.</span><span class="sxs-lookup"><span data-stu-id="d3e65-364">To convert 4:2:0 YUV to 4:4:4 YUV, you can simply follow the two methods described previously.</span></span> <span data-ttu-id="d3e65-365">Convertissez l’image 4:2:0 en 4:2:2, puis convertissez l’image 4:2:2 en 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="d3e65-365">Convert the 4:2:0 image to 4:2:2, and then convert the 4:2:2 image to 4:4:4.</span></span> <span data-ttu-id="d3e65-366">Vous pouvez également basculer l’ordre des deux processus de conversion, car l’ordre des opérations n’a pas vraiment d’importance sur la qualité visuelle du résultat.</span><span class="sxs-lookup"><span data-stu-id="d3e65-366">You can also switch the order of the two upconversion processes, as the order of operation does not really matter to the visual quality of the result.</span></span>

## <a name="other-yuv-formats"></a><span data-ttu-id="d3e65-367">Autres formats YUV</span><span class="sxs-lookup"><span data-stu-id="d3e65-367">Other YUV Formats</span></span>

<span data-ttu-id="d3e65-368">D’autres formats YUV les moins courants sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="d3e65-368">Some other, less common YUV formats include the following:</span></span>

-   <span data-ttu-id="d3e65-369">AI44 est un format en palette YUV avec 8 bits par échantillon.</span><span class="sxs-lookup"><span data-stu-id="d3e65-369">AI44 is a palettized YUV format with 8 bits per sample.</span></span> <span data-ttu-id="d3e65-370">Chaque échantillon contient un index dans les 4 bits les plus significatifs (MSBs) et une valeur alpha dans les 4 bits les plus significatifs (LSBs).</span><span class="sxs-lookup"><span data-stu-id="d3e65-370">Each sample contains an index in the 4 most significant bits (MSBs) and an alpha value in the 4 least significant bits (LSBs).</span></span> <span data-ttu-id="d3e65-371">L’index fait référence à un tableau d’entrées de palette YUV, qui doit être défini dans le type de média pour le format.</span><span class="sxs-lookup"><span data-stu-id="d3e65-371">The index refers to an array of YUV palette entries, which must be defined in the media type for the format.</span></span> <span data-ttu-id="d3e65-372">Ce format est principalement utilisé pour les images de sous-image.</span><span class="sxs-lookup"><span data-stu-id="d3e65-372">This format is primarily used for subpicture images.</span></span>
-   <span data-ttu-id="d3e65-373">NV11 est un format Planar 4:1:1 avec 12 bits par pixel.</span><span class="sxs-lookup"><span data-stu-id="d3e65-373">NV11 is a 4:1:1 planar format with 12 bits per pixel.</span></span> <span data-ttu-id="d3e65-374">Les échantillons Y apparaissent en premier dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="d3e65-374">The Y samples appear first in memory.</span></span> <span data-ttu-id="d3e65-375">Le plan Y est suivi d’un tableau d’échantillons compactés U (CB) et V (CR).</span><span class="sxs-lookup"><span data-stu-id="d3e65-375">The Y plane is followed by an array of packed U (Cb) and V (Cr) samples.</span></span> <span data-ttu-id="d3e65-376">Quand le tableau U-V combiné est adressé sous la forme d’un tableau de valeurs de **mot** Little-endian, les échantillons u sont contenus dans le LSBs de chaque **mot**, et les exemples V sont contenus dans le MSBS.</span><span class="sxs-lookup"><span data-stu-id="d3e65-376">When the combined U-V array is addressed as an array of little-endian **WORD** values, the U samples are contained in the LSBs of each **WORD**, and the V samples are contained in the MSBs.</span></span> <span data-ttu-id="d3e65-377">(Cette disposition de mémoire est similaire à NV12, bien que l’échantillonnage Chroma soit différent.)</span><span class="sxs-lookup"><span data-stu-id="d3e65-377">(This memory layout is similar to NV12 although the chroma sampling is different.)</span></span>
-   <span data-ttu-id="d3e65-378">Y41P est un format compressé de 4:1:1, avec vous et V échantillonnés tous les quatre pixels horizontalement.</span><span class="sxs-lookup"><span data-stu-id="d3e65-378">Y41P is a 4:1:1 packed format, with U and V sampled every fourth pixel horizontally.</span></span> <span data-ttu-id="d3e65-379">Chaque macropixel contient 8 pixels en trois octets, avec la disposition d’octets suivante : `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`</span><span class="sxs-lookup"><span data-stu-id="d3e65-379">Each macropixel contains 8 pixels in three bytes, with the following byte layout: `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`</span></span>
-   <span data-ttu-id="d3e65-380">Y41T est identique à Y41P, sauf que le bit le moins significatif de chaque échantillon Y spécifie la clé de chrominance (0 = transparent, 1 = opaque).</span><span class="sxs-lookup"><span data-stu-id="d3e65-380">Y41T is identical to Y41P, except the least-significant bit of each Y sample specifies the chroma key (0 = transparent, 1 = opaque).</span></span>
-   <span data-ttu-id="d3e65-381">Y42T est identique à UYVY, sauf que le bit le moins significatif de chaque échantillon Y spécifie la clé de chrominance (0 = transparent, 1 = opaque).</span><span class="sxs-lookup"><span data-stu-id="d3e65-381">Y42T is identical to UYVY, except the least-significant bit of each Y sample specifies the chroma key (0 = transparent, 1 = opaque).</span></span>
-   <span data-ttu-id="d3e65-382">YVYU est équivalent à YUYV, sauf que les exemples vous et V sont permutés.</span><span class="sxs-lookup"><span data-stu-id="d3e65-382">YVYU is equivalent to YUYV except the U and V samples are swapped.</span></span>

## <a name="identifying-yuv-formats-in-media-foundation"></a><span data-ttu-id="d3e65-383">Identification des formats YUV dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d3e65-383">Identifying YUV Formats in Media Foundation</span></span>

<span data-ttu-id="d3e65-384">Chaque format YUV décrit dans cet article est associé à un code FOURCC.</span><span class="sxs-lookup"><span data-stu-id="d3e65-384">Each of the YUV formats described in this article has an assigned FOURCC code.</span></span> <span data-ttu-id="d3e65-385">Un code FOURCC est un entier non signé 32 bits créé par la concaténation de quatre caractères ASCII.</span><span class="sxs-lookup"><span data-stu-id="d3e65-385">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span>

<span data-ttu-id="d3e65-386">Il existe plusieurs macros C/C++ qui facilitent la déclaration de valeurs FOURCC dans le code source.</span><span class="sxs-lookup"><span data-stu-id="d3e65-386">There are various C/C++ macros that make it easier to declare FOURCC values in source code.</span></span> <span data-ttu-id="d3e65-387">Par exemple, la macro **MAKEFOURCC** est déclarée dans Mmsystem. h, et la macro **FCC** est déclarée dans Aviriff. h.</span><span class="sxs-lookup"><span data-stu-id="d3e65-387">For example, the **MAKEFOURCC** macro is declared in Mmsystem.h, and the **FCC** macro is declared in Aviriff.h.</span></span> <span data-ttu-id="d3e65-388">Utilisez-les comme suit :</span><span class="sxs-lookup"><span data-stu-id="d3e65-388">Use them as follows:</span></span>

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```

<span data-ttu-id="d3e65-389">Vous pouvez également déclarer directement un code FOURCC en tant que littéral de chaîne en inversant l’ordre des caractères.</span><span class="sxs-lookup"><span data-stu-id="d3e65-389">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="d3e65-390">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="d3e65-390">For example:</span></span>

``` syntax
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'
```

<span data-ttu-id="d3e65-391">L’inversion de l’ordre est nécessaire, car le système d’exploitation Windows utilise une architecture Little endian.</span><span class="sxs-lookup"><span data-stu-id="d3e65-391">Reversing the order is necessary because the Windows operating system uses a little-endian architecture.</span></span> <span data-ttu-id="d3e65-392">'Y' = 0x59, 'U' = 0x55, et' 2 ' = 0x32, donc' 2YUY’est 0x32595559.</span><span class="sxs-lookup"><span data-stu-id="d3e65-392">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.</span></span>

<span data-ttu-id="d3e65-393">Dans Media Foundation, les formats sont identifiés par un GUID de type principal et un GUID de sous-type.</span><span class="sxs-lookup"><span data-stu-id="d3e65-393">In Media Foundation, formats are identified by a major type GUID and a subtype GUID.</span></span> <span data-ttu-id="d3e65-394">Le type majeur pour les formats vidéo d’ordinateur est toujours MFMediaType \_ .</span><span class="sxs-lookup"><span data-stu-id="d3e65-394">The major type for computer video formats is always MFMediaType\_Video .</span></span> <span data-ttu-id="d3e65-395">Le sous-type peut être construit en mappant le code FOURCC à un GUID, comme suit :</span><span class="sxs-lookup"><span data-stu-id="d3e65-395">The subtype can be constructed by mapping the FOURCC code to a GUID, as follows:</span></span>

``` syntax
XXXXXXXX-0000-0010-8000-00AA00389B71 
```

<span data-ttu-id="d3e65-396">où `XXXXXXXX` est le code FourCC.</span><span class="sxs-lookup"><span data-stu-id="d3e65-396">where `XXXXXXXX` is the FOURCC code.</span></span> <span data-ttu-id="d3e65-397">Par conséquent, le GUID de sous-type pour YUY2 est :</span><span class="sxs-lookup"><span data-stu-id="d3e65-397">Thus, the subtype GUID for YUY2 is:</span></span>

``` syntax
32595559-0000-0010-8000-00AA00389B71 
```

<span data-ttu-id="d3e65-398">Les constantes pour les GUID de format YUV les plus courants sont définies dans le fichier d’en-tête mfapi. h.</span><span class="sxs-lookup"><span data-stu-id="d3e65-398">Constants for the most common YUV format GUIDs are defined in the header file mfapi.h.</span></span> <span data-ttu-id="d3e65-399">Pour obtenir la liste de ces constantes, consultez [GUID sous-type de vidéo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="d3e65-399">For a list of these constants, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3e65-400">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3e65-400">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3e65-401">À propos de la vidéo YUV</span><span class="sxs-lookup"><span data-stu-id="d3e65-401">About YUV Video</span></span>](about-yuv-video.md)
</dt> <dt>

[<span data-ttu-id="d3e65-402">Types de média vidéo</span><span class="sxs-lookup"><span data-stu-id="d3e65-402">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 



