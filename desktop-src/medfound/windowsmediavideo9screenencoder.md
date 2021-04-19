---
description: L’encodeur d’écran Windows Media Video 9 est optimisé pour l’encodage des captures d’écran séquentielles à partir des moniteurs d’ordinateur.
ms.assetid: 22faebf8-40c0-47f9-b66b-c0a8b5ba7202
title: Encodeur d’écran Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e0729a7b8ef09ad9b86b07e6668a933a307550
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541448"
---
# <a name="windows-media-video-9-screen-encoder"></a><span data-ttu-id="731d6-103">Encodeur d’écran Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="731d6-103">Windows Media Video 9 Screen Encoder</span></span>

<span data-ttu-id="731d6-104">L’encodeur d’écran Windows Media Video 9 est optimisé pour l’encodage des captures d’écran séquentielles à partir des moniteurs d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="731d6-104">The Windows Media Video 9 Screen encoder is optimized for encoding sequential screen shots from computer monitors.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="731d6-105">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="731d6-105">Class Identifier</span></span>

<span data-ttu-id="731d6-106">L’identificateur de classe (CLSID) de l’encodeur d’écran Windows Media Video 9 est représenté par la constante **CLSID \_ CMSSCEncMediaObject2**.</span><span class="sxs-lookup"><span data-stu-id="731d6-106">The class identifier (CLSID) for the Windows Media Video 9 Screen encoder is represented by the constant **CLSID\_CMSSCEncMediaObject2**.</span></span> <span data-ttu-id="731d6-107">Vous pouvez créer une instance de l’encodeur en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="731d6-107">You can create an instance of the encoder by calling **CoCreateInstance**.</span></span>

## <a name="input-types"></a><span data-ttu-id="731d6-108">Types d’entrée</span><span class="sxs-lookup"><span data-stu-id="731d6-108">Input Types</span></span>

<span data-ttu-id="731d6-109">Les types d’entrée suivants sont pris en charge par l’encodeur d’écran de la version 9 lorsqu’il est utilisé en tant qu’objet de média DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="731d6-109">The following input types are supported by the Version 9 Screen encoder when it is being used as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="731d6-110">MEDIASUBTYPE \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="731d6-110">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="731d6-111">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="731d6-111">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="731d6-112">MEDIASUBTYPE \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="731d6-112">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="731d6-113">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="731d6-113">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="731d6-114">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="731d6-114">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="731d6-115">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="731d6-115">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="731d6-116">Les types d’entrée suivants sont pris en charge par l’encodeur d’écran de la version 9 lorsqu’il est utilisé en tant que Media Foundation Transform (MFT).</span><span class="sxs-lookup"><span data-stu-id="731d6-116">The following input types are supported by the Version 9 Screen encoder when it is being used as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="731d6-117">MFVideoFormat \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="731d6-117">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="731d6-118">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="731d6-118">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="731d6-119">MFVideoFormat \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="731d6-119">MFVideoFormat\_ARGB32</span></span>
-   <span data-ttu-id="731d6-120">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="731d6-120">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="731d6-121">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="731d6-121">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="731d6-122">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="731d6-122">MFVideoFormat\_RGB8</span></span>

## <a name="output-types"></a><span data-ttu-id="731d6-123">Types de sortie</span><span class="sxs-lookup"><span data-stu-id="731d6-123">Output Types</span></span>

<span data-ttu-id="731d6-124">Le code à quatre caractères (FOURCC) pour Windows Media Video contenu encodé à l’écran version 9 est « MSS2 ».</span><span class="sxs-lookup"><span data-stu-id="731d6-124">The four-character code (FOURCC) for Windows Media Video Screen Version 9 encoded content is "MSS2".</span></span>

<span data-ttu-id="731d6-125">Les types de sortie suivants sont pris en charge par l’encodeur d’écran de la version 9.</span><span class="sxs-lookup"><span data-stu-id="731d6-125">The following output types are supported by the Version 9 Screen encoder.</span></span>

-   <span data-ttu-id="731d6-126">MEDIASUBTYPE \_ MSS2</span><span class="sxs-lookup"><span data-stu-id="731d6-126">MEDIASUBTYPE\_MSS2</span></span>

## <a name="encoder-properties"></a><span data-ttu-id="731d6-127">Propriétés de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="731d6-127">Encoder Properties</span></span>

<span data-ttu-id="731d6-128">L’encodeur d’écran Windows Media Video 9 prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="731d6-128">The Windows Media Video 9 Screen encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="731d6-129">Propriété</span><span class="sxs-lookup"><span data-stu-id="731d6-129">Property</span></span></th>
<th><span data-ttu-id="731d6-130">Description</span><span class="sxs-lookup"><span data-stu-id="731d6-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="731d6-131"><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></span><span class="sxs-lookup"><span data-stu-id="731d6-131"><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></span></span></td>
<td><span data-ttu-id="731d6-132">Spécifie la surcharge, en octets par paquet, requise pour le conteneur utilisé pour stocker le contenu compressé.</span><span class="sxs-lookup"><span data-stu-id="731d6-132">Specifies the overhead, in bytes per packet, required for the container that is used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="731d6-133">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-133">Windows XP and later.</span></span><br />
<span data-ttu-id="731d6-134">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="731d6-134">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="731d6-135"><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></span><span class="sxs-lookup"><span data-stu-id="731d6-135"><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></span></span></td>
<td><span data-ttu-id="731d6-136">Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) contraints à sa vitesse de transmission moyenne (spécifiée par <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>).</span><span class="sxs-lookup"><span data-stu-id="731d6-136">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>).</span></span><br/> <dl> <span data-ttu-id="731d6-137">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-137">Windows XP and later.</span></span><br />
<span data-ttu-id="731d6-138">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="731d6-138">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="731d6-139"><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></span><span class="sxs-lookup"><span data-stu-id="731d6-139"><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></span></span></td>
<td><span data-ttu-id="731d6-140">Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) avec restriction à sa vitesse de transmission maximale (spécifiée par <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>).</span><span class="sxs-lookup"><span data-stu-id="731d6-140">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>).</span></span><br/> <dl> <span data-ttu-id="731d6-141">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-141">Windows XP and later.</span></span><br />
<span data-ttu-id="731d6-142">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="731d6-142">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="731d6-143"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></span><span class="sxs-lookup"><span data-stu-id="731d6-143"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></span></span></td>
<td><span data-ttu-id="731d6-144">Spécifie si le flux de bits vidéo encodé contient une valeur de saturation de la mémoire tampon avec chaque image clé.</span><span class="sxs-lookup"><span data-stu-id="731d6-144">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="731d6-145">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-145">Windows XP and later.</span></span><br />
<span data-ttu-id="731d6-146">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="731d6-146">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="731d6-147"><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="731d6-147"><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></span></span></td>
<td><span data-ttu-id="731d6-148">Spécifie le nombre de trames vidéo encodées par le codec.</span><span class="sxs-lookup"><span data-stu-id="731d6-148">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="731d6-149">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-149">Windows XP and later.</span></span><br />
<span data-ttu-id="731d6-150">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="731d6-150">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="731d6-151"><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="731d6-151"><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></span></span></td>
<td><span data-ttu-id="731d6-152">Spécifie le nombre de trames vidéo encodées par le codec qui contiennent réellement des données.</span><span class="sxs-lookup"><span data-stu-id="731d6-152">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="731d6-153">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-153">Windows XP and later.</span></span><br />
<span data-ttu-id="731d6-154">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="731d6-154">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="731d6-155"><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></span><span class="sxs-lookup"><span data-stu-id="731d6-155"><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></span></span></td>
<td><span data-ttu-id="731d6-156">Cette propriété est remplacée par <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span><span class="sxs-lookup"><span data-stu-id="731d6-156">This property is superseded by <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="731d6-157"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></span><span class="sxs-lookup"><span data-stu-id="731d6-157"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></span></span></td>
<td><span data-ttu-id="731d6-158">Spécifie la complexité de l’algorithme d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="731d6-158">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="731d6-159">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="731d6-160">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="731d6-160">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="731d6-161"><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></span><span class="sxs-lookup"><span data-stu-id="731d6-161"><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></span></span></td>
<td><span data-ttu-id="731d6-162">Spécifie une représentation numérique du compromis entre le lissage du mouvement et la qualité de l’image dans la sortie du codec.</span><span class="sxs-lookup"><span data-stu-id="731d6-162">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="731d6-163">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-163">Windows XP and later.</span></span><br />
<span data-ttu-id="731d6-164">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="731d6-164">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="731d6-165"><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="731d6-165"><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></span></span></td>
<td><span data-ttu-id="731d6-166">Spécifie le nombre de trames vidéo supprimées pendant l’encodage.</span><span class="sxs-lookup"><span data-stu-id="731d6-166">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="731d6-167">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-167">Windows XP and later.</span></span><br />
<span data-ttu-id="731d6-168">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="731d6-168">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="731d6-169"><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></span><span class="sxs-lookup"><span data-stu-id="731d6-169"><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></span></span></td>
<td><span data-ttu-id="731d6-170">Spécifie la fin d’une passe d’encodage.</span><span class="sxs-lookup"><span data-stu-id="731d6-170">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="731d6-171">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-171">Windows XP and later.</span></span><br />
<span data-ttu-id="731d6-172">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="731d6-172">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="731d6-173"><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></span><span class="sxs-lookup"><span data-stu-id="731d6-173"><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></span></span></td>
<td><span data-ttu-id="731d6-174">Spécifie le FOURCC qui identifie l’encodeur que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="731d6-174">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="731d6-175">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-175">Windows XP and later.</span></span><br />
<span data-ttu-id="731d6-176">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="731d6-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="731d6-177"><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></span><span class="sxs-lookup"><span data-stu-id="731d6-177"><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></span></span></td>
<td><span data-ttu-id="731d6-178">Spécifie la durée maximale, en millisecondes, entre les images clés de la sortie du codec.</span><span class="sxs-lookup"><span data-stu-id="731d6-178">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="731d6-179">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-179">Windows XP and later.</span></span><br />
<span data-ttu-id="731d6-180">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="731d6-180">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="731d6-181"><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></span><span class="sxs-lookup"><span data-stu-id="731d6-181"><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></span></span></td>
<td><span data-ttu-id="731d6-182">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="731d6-182">Obsolete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="731d6-183"><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></span><span class="sxs-lookup"><span data-stu-id="731d6-183"><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></span></span></td>
<td><span data-ttu-id="731d6-184">Spécifie le nombre maximal de passes prises en charge par le codec.</span><span class="sxs-lookup"><span data-stu-id="731d6-184">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="731d6-185">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-185">Windows XP and later.</span></span><br />
<span data-ttu-id="731d6-186">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="731d6-186">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="731d6-187"><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></span><span class="sxs-lookup"><span data-stu-id="731d6-187"><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></span></span></td>
<td><span data-ttu-id="731d6-188">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-188">Windows XP and later.</span></span> <span data-ttu-id="731d6-189">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="731d6-189">Read/write.</span></span><br/> <span data-ttu-id="731d6-190">Spécifie le nombre de passes qui seront utilisées par le codec pour encoder le contenu.</span><span class="sxs-lookup"><span data-stu-id="731d6-190">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="731d6-191">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-191">Windows XP and later.</span></span><br />
<span data-ttu-id="731d6-192">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="731d6-192">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="731d6-193"><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></span><span class="sxs-lookup"><span data-stu-id="731d6-193"><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></span></span></td>
<td><span data-ttu-id="731d6-194">Spécifie QP.</span><span class="sxs-lookup"><span data-stu-id="731d6-194">Specifies QP.</span></span> <span data-ttu-id="731d6-195">Les valeurs possibles sont 1,0 à 31,0.</span><span class="sxs-lookup"><span data-stu-id="731d6-195">Possible values are 1.0 through 31.0.</span></span><br/> <dl> <span data-ttu-id="731d6-196">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-196">Windows Vista and later.</span></span><br />
<span data-ttu-id="731d6-197">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="731d6-197">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="731d6-198"><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></span><span class="sxs-lookup"><span data-stu-id="731d6-198"><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></span></span></td>
<td><span data-ttu-id="731d6-199">Spécifie la vitesse de transmission moyenne, en bits par seconde, utilisée pour l’encodage VBR (variable-bit-rate) à 2 passes.</span><span class="sxs-lookup"><span data-stu-id="731d6-199">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="731d6-200">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-200">Windows XP and later.</span></span><br />
<span data-ttu-id="731d6-201">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="731d6-201">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="731d6-202"><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></span><span class="sxs-lookup"><span data-stu-id="731d6-202"><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></span></span></td>
<td><span data-ttu-id="731d6-203">Spécifie le taux de bits de pointe, en bits par seconde, utilisé pour l’encodage VBR (variable-bit-rate) avec restriction de 2 passes.</span><span class="sxs-lookup"><span data-stu-id="731d6-203">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="731d6-204">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-204">Windows XP and later.</span></span><br />
<span data-ttu-id="731d6-205">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="731d6-205">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="731d6-206"><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="731d6-206"><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></span></span></td>
<td><span data-ttu-id="731d6-207">Spécifie le nombre de trames vidéo transmises à l’encodeur pendant le processus d’encodage.</span><span class="sxs-lookup"><span data-stu-id="731d6-207">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="731d6-208">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-208">Windows XP and later.</span></span><br />
<span data-ttu-id="731d6-209">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="731d6-209">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="731d6-210"><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></span><span class="sxs-lookup"><span data-stu-id="731d6-210"><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></span></span></td>
<td><span data-ttu-id="731d6-211">Spécifie si le codec utilise l’encodage VBR (variable-bit-rate).</span><span class="sxs-lookup"><span data-stu-id="731d6-211">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="731d6-212">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-212">Windows XP and later.</span></span><br />
<span data-ttu-id="731d6-213">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="731d6-213">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="731d6-214"><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></span><span class="sxs-lookup"><span data-stu-id="731d6-214"><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></span></span></td>
<td><span data-ttu-id="731d6-215">Spécifie le niveau de qualité réel pour l’encodage VBR (variable-bit-rate) basé sur la qualité (1 passe).</span><span class="sxs-lookup"><span data-stu-id="731d6-215">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="731d6-216">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-216">Windows XP and later.</span></span><br />
<span data-ttu-id="731d6-217">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="731d6-217">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="731d6-218"><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="731d6-218"><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></span></span></td>
<td><span data-ttu-id="731d6-219">Quantité de contenu, en millisecondes, qui peut tenir dans la mémoire tampon du modèle.</span><span class="sxs-lookup"><span data-stu-id="731d6-219">The amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="731d6-220">Windows XP et versions ultérieures,</span><span class="sxs-lookup"><span data-stu-id="731d6-220">Windows XP and later,</span></span><br />
<span data-ttu-id="731d6-221">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="731d6-221">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="731d6-222"><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="731d6-222"><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></span></span></td>
<td><span data-ttu-id="731d6-223">Spécifie le nombre de trames vidéo qui ont été ignorées, car il s’agissait de doublons de trames précédentes.</span><span class="sxs-lookup"><span data-stu-id="731d6-223">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="731d6-224">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="731d6-224">Windows XP and later.</span></span><br />
<span data-ttu-id="731d6-225">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="731d6-225">Read-only.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="731d6-226">Notes</span><span class="sxs-lookup"><span data-stu-id="731d6-226">Remarks</span></span>

<span data-ttu-id="731d6-227">Un objet d’encodeur d’écran expose l’interface **IMediaObject** afin que l’objet puisse être utilisé en tant qu’objet de média DirectX (DMO) et expose l’interface **IMFTransform** afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="731d6-227">A screen encoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="731d6-228">Un encodeur d’écran se comporte comme un DMO ou une table MFT selon les interfaces que vous obtenez et la version de Windows en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="731d6-228">A screen encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="731d6-229">Le tableau suivant indique les conditions sous lesquelles un encodeur d’écran se comporte comme un DMO ou une table MFT.</span><span class="sxs-lookup"><span data-stu-id="731d6-229">The following table shows the conditions under which a screen encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="731d6-230">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="731d6-230">Operating system</span></span>            | <span data-ttu-id="731d6-231">Comportement de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="731d6-231">Encoder behavior</span></span>                                                                                                                                    |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="731d6-232">Windows XP</span><span class="sxs-lookup"><span data-stu-id="731d6-232">Windows XP</span></span>                  | <span data-ttu-id="731d6-233">Un encodeur d’écran Windows Media se comporte toujours comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="731d6-233">A Windows Media Screen encoder always behaves as a DMO.</span></span>                                                                                             |
| <span data-ttu-id="731d6-234">Windows Vista et Windows 7</span><span class="sxs-lookup"><span data-stu-id="731d6-234">Windows Vista and Windows 7</span></span> | <span data-ttu-id="731d6-235">Par défaut, un encodeur d’écran Windows Media se comporte comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="731d6-235">By default, a Windows Media Screen encoder behaves as a DMO.</span></span> <span data-ttu-id="731d6-236">Si vous obtenez une interface **IMFTransform** sur un encodeur d’écran, elle se comporte comme une table MFT.</span><span class="sxs-lookup"><span data-stu-id="731d6-236">If you obtain an **IMFTransform** interface on a screen encoder, it behaves as an MFT.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="731d6-237">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="731d6-237">Requirements</span></span>



| <span data-ttu-id="731d6-238">Condition requise</span><span class="sxs-lookup"><span data-stu-id="731d6-238">Requirement</span></span> | <span data-ttu-id="731d6-239">Valeur</span><span class="sxs-lookup"><span data-stu-id="731d6-239">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="731d6-240">Client</span><span class="sxs-lookup"><span data-stu-id="731d6-240">Client</span></span><br/> | <span data-ttu-id="731d6-241">Windows XP, Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="731d6-241">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="731d6-242">En-tête</span><span class="sxs-lookup"><span data-stu-id="731d6-242">Header</span></span><br/> | <dl> <span data-ttu-id="731d6-243"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="731d6-243"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="731d6-244">DLL</span><span class="sxs-lookup"><span data-stu-id="731d6-244">DLL</span></span><br/>    | <dl> <span data-ttu-id="731d6-245"><dt>Wmvsencd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="731d6-245"><dt>Wmvsencd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="731d6-246">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="731d6-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="731d6-247">Objets codec</span><span class="sxs-lookup"><span data-stu-id="731d6-247">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="731d6-248">Implémentation du codec</span><span class="sxs-lookup"><span data-stu-id="731d6-248">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="731d6-249">Utilisation du codec d’écran Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="731d6-249">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[<span data-ttu-id="731d6-250">Décodeur d’écran Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="731d6-250">Windows Media Video 9 Screen Decoder</span></span>](windowsmediavideo9screendecoder.md)
</dt> </dl>

 

 




