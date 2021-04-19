---
description: 'L’encodeur Windows Media Audio encode des flux audio. L’encodeur prend en charge trois catégories de sorties encodées : Windows Media Audio standard, Windows Media Audio Professional et Windows Media Audio Lossless.'
ms.assetid: 1f6a3a9f-b534-4a6b-b773-0315c759624e
title: Encodeur Windows Media Audio (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f1d5b9e5f890a43958bcc304dd2d305844fdb4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537626"
---
# <a name="windows-media-audio-encoder"></a><span data-ttu-id="3d09f-104">Encodeur Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="3d09f-104">Windows Media Audio Encoder</span></span>

<span data-ttu-id="3d09f-105">L’encodeur Windows Media Audio encode des flux audio.</span><span class="sxs-lookup"><span data-stu-id="3d09f-105">The Windows Media Audio encoder encodes audio streams.</span></span> <span data-ttu-id="3d09f-106">L’encodeur prend en charge trois catégories de sorties encodées : Windows Media Audio standard, Windows Media Audio Professional et Windows Media Audio Lossless.</span><span class="sxs-lookup"><span data-stu-id="3d09f-106">The encoder supports three categories of encoded output: Windows Media Audio Standard, Windows Media Audio Professional, and Windows Media Audio Lossless.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="3d09f-107">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="3d09f-107">Class Identifier</span></span>

<span data-ttu-id="3d09f-108">L’identificateur de classe (CLSID) de l’encodeur de Windows Media Audio est représenté par la constante **CLSID \_ CWMAEncMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="3d09f-108">The class identifier (CLSID) for the Windows Media Audio Encoder is represented by the constant **CLSID\_CWMAEncMediaObject**.</span></span> <span data-ttu-id="3d09f-109">Vous pouvez créer une instance de l’encodeur audio en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="3d09f-109">You can create an instance of the audio encoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="3d09f-110">Formats d’entrée</span><span class="sxs-lookup"><span data-stu-id="3d09f-110">Input Formats</span></span>

<span data-ttu-id="3d09f-111">Le tableau suivant répertorie les balises de format audio qui représentent les catégories d’entrée prises en charge par l’encodeur Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="3d09f-111">The following table shows the audio format tags that represent the input categories supported by the Windows Media Audio encoder.</span></span> <span data-ttu-id="3d09f-112">Pour plus d’informations sur la définition des types d’entrée et de sortie pour l’encodeur, consultez Configuration de l' [encodage audio](configuringaudioencoding.md).</span><span class="sxs-lookup"><span data-stu-id="3d09f-112">For information about how to set the input and output types for the encoder, see [Configuring Audio Encoding](configuringaudioencoding.md).</span></span>



| <span data-ttu-id="3d09f-113">Balise de format, constante</span><span class="sxs-lookup"><span data-stu-id="3d09f-113">Format tag constant</span></span>       | <span data-ttu-id="3d09f-114">Mettre en forme la valeur de balise</span><span class="sxs-lookup"><span data-stu-id="3d09f-114">Format tag value</span></span> | <span data-ttu-id="3d09f-115">Format audio</span><span class="sxs-lookup"><span data-stu-id="3d09f-115">Audio format</span></span>                                          |
|---------------------------|------------------|-------------------------------------------------------|
| <span data-ttu-id="3d09f-116">\_PCM format \_ Wave</span><span class="sxs-lookup"><span data-stu-id="3d09f-116">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="3d09f-117">0x0001</span><span class="sxs-lookup"><span data-stu-id="3d09f-117">0x0001</span></span>           | <span data-ttu-id="3d09f-118">Format PCM</span><span class="sxs-lookup"><span data-stu-id="3d09f-118">PCM format</span></span>                                            |
| <span data-ttu-id="3d09f-119">\_format Wave \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="3d09f-119">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="3d09f-120">0x0003</span><span class="sxs-lookup"><span data-stu-id="3d09f-120">0x0003</span></span>           | <span data-ttu-id="3d09f-121">Virgule flottante IEEE</span><span class="sxs-lookup"><span data-stu-id="3d09f-121">IEEE floating point</span></span>                                   |
| <span data-ttu-id="3d09f-122">\_format Wave \_ extensible</span><span class="sxs-lookup"><span data-stu-id="3d09f-122">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="3d09f-123">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="3d09f-123">0xFFFE</span></span>           | <span data-ttu-id="3d09f-124">Format PCM/IEEE dans la structure **WAVEFORMATEXTENSIBLE**</span><span class="sxs-lookup"><span data-stu-id="3d09f-124">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="3d09f-125">Formats de sortie</span><span class="sxs-lookup"><span data-stu-id="3d09f-125">Output Formats</span></span>

<span data-ttu-id="3d09f-126">Le tableau suivant répertorie les balises de format audio qui représentent les catégories de sortie prises en charge par l’encodeur Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="3d09f-126">The following table shows the audio format tags that represent the output categories supported by the Windows Media Audio encoder.</span></span>



| <span data-ttu-id="3d09f-127">Balise de format, constante</span><span class="sxs-lookup"><span data-stu-id="3d09f-127">Format tag constant</span></span>             | <span data-ttu-id="3d09f-128">Mettre en forme la valeur de balise</span><span class="sxs-lookup"><span data-stu-id="3d09f-128">Format tag value</span></span> | <span data-ttu-id="3d09f-129">Format audio</span><span class="sxs-lookup"><span data-stu-id="3d09f-129">Audio format</span></span>                     |
|---------------------------------|------------------|----------------------------------|
| <span data-ttu-id="3d09f-130">\_WMAUDIO2 format \_ Wave</span><span class="sxs-lookup"><span data-stu-id="3d09f-130">WAVE\_FORMAT\_WMAUDIO2</span></span>          | <span data-ttu-id="3d09f-131">0x0161</span><span class="sxs-lookup"><span data-stu-id="3d09f-131">0x0161</span></span>           | <span data-ttu-id="3d09f-132">Windows Media Audio standard</span><span class="sxs-lookup"><span data-stu-id="3d09f-132">Windows Media Audio Standard</span></span>     |
| <span data-ttu-id="3d09f-133">\_WMAUDIO3 format \_ Wave</span><span class="sxs-lookup"><span data-stu-id="3d09f-133">WAVE\_FORMAT\_WMAUDIO3</span></span>          | <span data-ttu-id="3d09f-134">0x0162</span><span class="sxs-lookup"><span data-stu-id="3d09f-134">0x0162</span></span>           | <span data-ttu-id="3d09f-135">Windows Media Audio professionnel</span><span class="sxs-lookup"><span data-stu-id="3d09f-135">Windows Media Audio Professional</span></span> |
| <span data-ttu-id="3d09f-136">WAVE \_ format \_ WMAUDIO \_ Lossless</span><span class="sxs-lookup"><span data-stu-id="3d09f-136">WAVE\_FORMAT\_WMAUDIO\_LOSSLESS</span></span> | <span data-ttu-id="3d09f-137">0x0163</span><span class="sxs-lookup"><span data-stu-id="3d09f-137">0x0163</span></span>           | <span data-ttu-id="3d09f-138">Windows Media Audio sans perte</span><span class="sxs-lookup"><span data-stu-id="3d09f-138">Windows Media Audio Lossless</span></span>     |



 

## <a name="interfaces"></a><span data-ttu-id="3d09f-139">Interfaces</span><span class="sxs-lookup"><span data-stu-id="3d09f-139">Interfaces</span></span>

<span data-ttu-id="3d09f-140">Un objet endoder audio expose l’interface **IMediaObject** afin que l’objet puisse être utilisé en tant qu’objet de média DirectX (DMO) et expose l’interface **IMFTransform** afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="3d09f-140">An audio endoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="3d09f-141">Un encodeur Windows Media Audio se comporte comme un DMO ou une table MFT en fonction des interfaces que vous obtenez et de la version de Windows en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="3d09f-141">A Windows Media Audio encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="3d09f-142">Le tableau suivant indique les conditions dans lesquelles un encodeur audio se comporte comme un DMO ou une table MFT.</span><span class="sxs-lookup"><span data-stu-id="3d09f-142">The following table shows the conditions under which an audio encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="3d09f-143">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="3d09f-143">Operating system</span></span> | <span data-ttu-id="3d09f-144">Comportement de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="3d09f-144">Encoder behavior</span></span>                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d09f-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3d09f-145">Windows XP</span></span>       | <span data-ttu-id="3d09f-146">Un encodeur Windows Media Audio se comporte toujours comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="3d09f-146">A Windows Media Audio encoder always behaves as a DMO.</span></span>                                                                                                                                |
| <span data-ttu-id="3d09f-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d09f-147">Windows Vista</span></span>    | <span data-ttu-id="3d09f-148">Par défaut, un encodeur Windows Media Audio se comporte comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="3d09f-148">By default, a Windows Media Audio encoder behaves as a DMO.</span></span> <span data-ttu-id="3d09f-149">Si vous obtenez une interface **IMFTransform** ou une interface **IPropertyStore** sur un encodeur audio, elle se comporte comme une table MFT.</span><span class="sxs-lookup"><span data-stu-id="3d09f-149">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on an audio encoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="3d09f-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d09f-150">Windows 7</span></span>        | <span data-ttu-id="3d09f-151">Par défaut, un encodeur Windows Media Audio se comporte comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="3d09f-151">By default, a Windows Media Audio encoder behaves as a DMO.</span></span> <span data-ttu-id="3d09f-152">Si vous obtenez une interface **IMFTransform** sur un encodeur audio, elle se comporte comme une table MFT.</span><span class="sxs-lookup"><span data-stu-id="3d09f-152">If you obtain an **IMFTransform** interface on an audio encoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="encoder-properties"></a><span data-ttu-id="3d09f-153">Propriétés de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="3d09f-153">Encoder Properties</span></span>

<span data-ttu-id="3d09f-154">L’encodeur Windows Media Audio prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3d09f-154">The Windows Media Audio encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3d09f-155">Propriété</span><span class="sxs-lookup"><span data-stu-id="3d09f-155">Property</span></span></th>
<th><span data-ttu-id="3d09f-156">Description</span><span class="sxs-lookup"><span data-stu-id="3d09f-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d09f-157"><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-157"><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-158">Spécifie si l’encodeur utilise l’encodage VBR moyen-contrôlable.</span><span class="sxs-lookup"><span data-stu-id="3d09f-158">Specifies whether the encoder uses average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="3d09f-159">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-160">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-160">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-161">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-161">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-162"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-162"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-163">Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) avec restriction à sa vitesse de transmission maximale.</span><span class="sxs-lookup"><span data-stu-id="3d09f-163">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate.</span></span><br/> <dl> <span data-ttu-id="3d09f-164">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-164">Windows XP and later.</span></span><br />
<span data-ttu-id="3d09f-165">Standard, professionnel.</span><span class="sxs-lookup"><span data-stu-id="3d09f-165">Standard, Professional.</span></span><br />
<span data-ttu-id="3d09f-166">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-166">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-167"><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-167"><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-168">Spécifie si l’encodeur doit vérifier la cohérence des données entre les passes lors de l’exécution du codage VBR en deux passes.</span><span class="sxs-lookup"><span data-stu-id="3d09f-168">Specifies whether whether the encoder should check for data consistency across passes when performing two-pass VBR encoding.</span></span> <br/> <dl> <span data-ttu-id="3d09f-169">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-169">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-170">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-170">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-171">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3d09f-171">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-172"><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-172"><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-173">Spécifie si l’encodeur est limité par une latence maximale de décodeur.</span><span class="sxs-lookup"><span data-stu-id="3d09f-173">Specifies whether the encoder is constrained by a maximum decoder latency requirement.</span></span><br/> <dl> <span data-ttu-id="3d09f-174">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-174">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-175">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-175">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-176">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-176">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-177"><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-177"><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-178">Spécifie si la complexité de l’algorithme d’encodage est restreinte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-178">Specifies whether the complexity of the encoding algorithm is constrained.</span></span><br/> <dl> <span data-ttu-id="3d09f-179">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-179">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-180">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-180">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-181">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-181">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-182"><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-182"><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-183">Spécifie si l’encodeur est limité par une latence maximale.</span><span class="sxs-lookup"><span data-stu-id="3d09f-183">Specifies whether the encoder is constrained by a maximum latency requirement.</span></span><br/> <dl> <span data-ttu-id="3d09f-184">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-184">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-185">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-185">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-186">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-186">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-187"><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-187"><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-188">Spécifie si les modes énumérés par l’encodeur sont limités à ceux qui répondent à une exigence de qualité.</span><span class="sxs-lookup"><span data-stu-id="3d09f-188">Specifies whether modes enumerated by the encoder are limited to those that meet a quality requirement.</span></span><br/> <dl> <span data-ttu-id="3d09f-189">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-189">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-190">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-190">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-191">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-191">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-192"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-192"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-193">Spécifie le profil de complexité du contenu encodé.</span><span class="sxs-lookup"><span data-stu-id="3d09f-193">Specifies the complexity profile of the encoded content.</span></span><br/> <dl> <span data-ttu-id="3d09f-194">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-194">Windows XP and later.</span></span><br />
<span data-ttu-id="3d09f-195">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-195">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-196">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3d09f-196">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-197"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-197"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-198">Spécifie le niveau de qualité souhaité pour l’encodage VBR.</span><span class="sxs-lookup"><span data-stu-id="3d09f-198">Specifies the desired quality level for VBR encoding.</span></span><br/> <dl> <span data-ttu-id="3d09f-199">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-199">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-200">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-200">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-201">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="3d09f-201">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-202"><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-202"><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-203">Spécifie si l’encodeur utilise la substitution de bruit.</span><span class="sxs-lookup"><span data-stu-id="3d09f-203">Specifies whether the encoder uses noise substitution.</span></span><br/> <dl> <span data-ttu-id="3d09f-204">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-204">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-205">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-205">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-206">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-206">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-207"><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-207"><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-208">Spécifie si l’encodeur utilise la limitation de plage PCM.</span><span class="sxs-lookup"><span data-stu-id="3d09f-208">Specifies whether the encoder uses PCM range limiting.</span></span><br/> <dl> <span data-ttu-id="3d09f-209">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-209">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-210">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-210">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-211">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-211">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-212"><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-212"><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-213">Spécifie la bande passante codée maximale autorisée par la troncation de la bande dans l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="3d09f-213">Specifies the maximum coded bandwidth allowed by band truncation in the encoder.</span></span><br/> <dl> <span data-ttu-id="3d09f-214">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-214">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-215">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-215">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-216">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-216">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-217"><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-217"><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-218">Spécifie la bande passante codée minimale autorisée par la troncation de la bande dans l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="3d09f-218">Specifies the minimum coded bandwidth allowed by band truncation in the encoder.</span></span><br/> <dl> <span data-ttu-id="3d09f-219">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-219">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-220">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-220">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-221">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-221">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-222"><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-222"><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-223">Spécifie la qualité à laquelle la bande passante minimale codée est autorisée.</span><span class="sxs-lookup"><span data-stu-id="3d09f-223">Specifies the quality at which minimum coded bandwidth is allowed.</span></span> <br/> <dl> <span data-ttu-id="3d09f-224">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-224">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-225">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-225">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-226">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-226">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-227"><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-227"><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-228">Spécifie la qualité à laquelle la bande passante codée maximale est autorisée.</span><span class="sxs-lookup"><span data-stu-id="3d09f-228">Specifies the quality at which maximum coded bandwidth is allowed.</span></span><br/> <dl> <span data-ttu-id="3d09f-229">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-229">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-230">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-230">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-231">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-231">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-232"><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-232"><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-233">Spécifie si l’encodeur effectue une troncation de bande.</span><span class="sxs-lookup"><span data-stu-id="3d09f-233">Specifies whether the encoder performs band truncation.</span></span><br/> <dl> <span data-ttu-id="3d09f-234">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-234">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-235">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-235">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-236">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-236">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-237"><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-237"><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-238">Spécifie si l’encodeur utilise le style de calcul de masque effectué par la version 7 de l’encodeur Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="3d09f-238">Specifies whether the encoder uses the style of mask computation performed by version 7 of the Windows Media Audio encoder.</span></span><br/> <dl> <span data-ttu-id="3d09f-239">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-239">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-240">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-240">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-241">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-241">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-242"><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-242"><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-243">Spécifie si l’encodeur effectue un traitement d’image stéréo.</span><span class="sxs-lookup"><span data-stu-id="3d09f-243">Specifies whether the encoder performs stereo image processing.</span></span> <br/> <dl> <span data-ttu-id="3d09f-244">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-244">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-245">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-245">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-246">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-246">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-247"><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-247"><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-248">Spécifie la fenêtre de mémoire tampon, en millisecondes, pour un encodeur qui est configuré pour utiliser l’encodage VBR moyen-contrôlable.</span><span class="sxs-lookup"><span data-stu-id="3d09f-248">Specifies the buffer window, in milliseconds, for an encoder that is configured to use average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="3d09f-249">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-249">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-250">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-250">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-251">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-251">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-252"><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-252"><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-253">Spécifie la vitesse de transmission moyenne, en bits par seconde, pour un encodeur qui est configuré pour utiliser l’encodage VBR moyen-contrôlable.</span><span class="sxs-lookup"><span data-stu-id="3d09f-253">Specifies the average bit rate, in bits per second, for an encoder that is configured to use average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="3d09f-254">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-254">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-255">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-255">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-256">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-256">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-257"><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-257"><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-258">Spécifie la complexité de l’algorithme d’encodage.</span><span class="sxs-lookup"><span data-stu-id="3d09f-258">Specifies the complexity of the encoding algorithm.</span></span><br/> <dl> <span data-ttu-id="3d09f-259">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-259">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-260">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-260">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-261">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-261">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-262"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-262"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-263">Spécifie la fin d’une passe d’encodage.</span><span class="sxs-lookup"><span data-stu-id="3d09f-263">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="3d09f-264">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-264">Windows XP and later.</span></span><br />
<span data-ttu-id="3d09f-265">Standard, professionnel.</span><span class="sxs-lookup"><span data-stu-id="3d09f-265">Standard, Professional.</span></span><br />
<span data-ttu-id="3d09f-266">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="3d09f-266">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-267"><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-267"><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-268">Spécifie si l’encodeur principal utilise la &quot; &quot; fonctionnalité plus.</span><span class="sxs-lookup"><span data-stu-id="3d09f-268">Specifies whether the core encoder uses the &quot;Plus&quot; feature.</span></span><br/> <dl> <span data-ttu-id="3d09f-269">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-269">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-270">Professionnel.</span><span class="sxs-lookup"><span data-stu-id="3d09f-270">Professional.</span></span><br />
<span data-ttu-id="3d09f-271">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-271">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-272"><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-272"><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-273">Spécifie la latence maximale pour le décodeur, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="3d09f-273">Specifies the maximum latency for the decoder, in milliseconds.</span></span><br/> <dl> <span data-ttu-id="3d09f-274">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-274">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-275">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-275">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-276">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="3d09f-276">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-277"><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-277"><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-278">Spécifie la latence maximale pour l’encodeur, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="3d09f-278">Specifies the maximum latency for the encoder, in milliseconds.</span></span><br/> <dl> <span data-ttu-id="3d09f-279">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-279">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-280">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-280">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-281">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="3d09f-281">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-282"><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-282"><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-283">Spécifie le niveau de qualité VBR du type de sortie énuméré le plus récemment.</span><span class="sxs-lookup"><span data-stu-id="3d09f-283">Specifies the VBR quality level of the most recently enumerated output type.</span></span><br/> <dl> <span data-ttu-id="3d09f-284">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-284">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-285">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-285">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-286">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3d09f-286">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-287"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-287"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-288">Spécifie le nombre maximal de passes prises en charge par l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="3d09f-288">Specifies the maximum number of passes supported by the encoder.</span></span><br/> <dl> <span data-ttu-id="3d09f-289">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-289">Windows XP and later.</span></span><br />
<span data-ttu-id="3d09f-290">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-290">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-291">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3d09f-291">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-292"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-292"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-293">Spécifie le nombre de passes qui seront utilisées par l’encodeur pour encoder le contenu.</span><span class="sxs-lookup"><span data-stu-id="3d09f-293">Specifies the number of passes that the encoder will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="3d09f-294">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-294">Windows XP and later.</span></span><br />
<span data-ttu-id="3d09f-295">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-295">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-296">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-296">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-297"><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-297"><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-298">Spécifie si l’encodeur est imposé par une vitesse de transmission de pic.</span><span class="sxs-lookup"><span data-stu-id="3d09f-298">Specifies whether the encoder is constrained by a peak bit rate.</span></span><br/> <dl> <span data-ttu-id="3d09f-299">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-299">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-300">Standard, professionnel.</span><span class="sxs-lookup"><span data-stu-id="3d09f-300">Standard, Professional.</span></span><br />
<span data-ttu-id="3d09f-301">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-301">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-302"><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-302"><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-303">Spécifie le nombre d’échantillons par défaut par image.</span><span class="sxs-lookup"><span data-stu-id="3d09f-303">Specifies the preferred number of samples per frame.</span></span><br/> <dl> <span data-ttu-id="3d09f-304">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-304">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-305">Professionnel.</span><span class="sxs-lookup"><span data-stu-id="3d09f-305">Professional.</span></span><br />
<span data-ttu-id="3d09f-306">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-306">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-307"><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-307"><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-308">Spécifie si l’encodeur doit utiliser une taille de frame préférée.</span><span class="sxs-lookup"><span data-stu-id="3d09f-308">Specifies whether the encoder should use a preferred frame size.</span></span><br/> <dl> <span data-ttu-id="3d09f-309">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-309">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-310">Professionnel.</span><span class="sxs-lookup"><span data-stu-id="3d09f-310">Professional.</span></span><br />
<span data-ttu-id="3d09f-311">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-311">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-312"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-312"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-313">Spécifie le taux de bits de pointe, en bits par seconde, utilisé pour l’encodage VBR (variable-bit-rate) avec restriction de 2 passes.</span><span class="sxs-lookup"><span data-stu-id="3d09f-313">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) encoding.</span></span> <br/> <dl> <span data-ttu-id="3d09f-314">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-314">Windows XP and later.</span></span><br />
<span data-ttu-id="3d09f-315">Standard, professionnel.</span><span class="sxs-lookup"><span data-stu-id="3d09f-315">Standard, Professional.</span></span><br />
<span data-ttu-id="3d09f-316">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-316">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-317"><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-317"><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-318">Spécifie la fenêtre de mémoire tampon moyenne, en millisecondes, d’un flux encodé.</span><span class="sxs-lookup"><span data-stu-id="3d09f-318">Specifies the average buffer window, in milliseconds, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="3d09f-319">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-319">Windows XP and later.</span></span><br />
<span data-ttu-id="3d09f-320">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-320">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-321">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3d09f-321">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-322"><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-322"><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-323">Spécifie la fenêtre de mémoire tampon maximale, en millisecondes, d’un flux encodé.</span><span class="sxs-lookup"><span data-stu-id="3d09f-323">Specifies the maximum buffer window, in milliseconds, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="3d09f-324">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-324">Windows XP and later.</span></span><br />
<span data-ttu-id="3d09f-325">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-325">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-326">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3d09f-326">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-327"><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-327"><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-328">Spécifie la vitesse de transmission moyenne, en bits par seconde, d’un flux encodé.</span><span class="sxs-lookup"><span data-stu-id="3d09f-328">Specifies the average bit rate, in bits per second, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="3d09f-329">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-329">Windows XP and later.</span></span><br />
<span data-ttu-id="3d09f-330">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-330">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-331">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3d09f-331">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-332"><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-332"><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-333">Spécifie la vitesse de transmission maximale, en bits par seconde, d’un flux encodé.</span><span class="sxs-lookup"><span data-stu-id="3d09f-333">Specifies the maximum bit rate, in bits per second, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="3d09f-334">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-334">Windows XP and later.</span></span><br />
<span data-ttu-id="3d09f-335">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-335">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-336">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3d09f-336">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-337"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-337"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-338">Spécifie si l’encodeur utilise l’encodage VBR.</span><span class="sxs-lookup"><span data-stu-id="3d09f-338">Specifies whether the encoder uses VBR encoding.</span></span><br/> <dl> <span data-ttu-id="3d09f-339">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-339">Windows XP and later.</span></span><br />
<span data-ttu-id="3d09f-340">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-340">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-341">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-341">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-342"><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-342"><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-343">Cette propriété n’est pas utilisée actuellement par le codec Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="3d09f-343">This property is currently not used by the Windows Media Audio codec.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-344"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-344"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-345">Spécifie le niveau de volume moyen de contenu audio.</span><span class="sxs-lookup"><span data-stu-id="3d09f-345">Specifies the average volume level of audio content.</span></span><br/> <dl> <span data-ttu-id="3d09f-346">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-346">Windows XP and later.</span></span><br />
<span data-ttu-id="3d09f-347">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-347">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-348">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3d09f-348">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-349"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-349"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-350">Spécifie le niveau de volume le plus élevé dans le contenu audio.</span><span class="sxs-lookup"><span data-stu-id="3d09f-350">Specifies the highest volume level occurring in audio content.</span></span><br/> <dl> <span data-ttu-id="3d09f-351">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-351">Windows XP and later.</span></span><br />
<span data-ttu-id="3d09f-352">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-352">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-353">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3d09f-353">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-354"><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-354"><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-355">Spécifie le nombre moyen d’octets par seconde pour le son encodé en VBR.</span><span class="sxs-lookup"><span data-stu-id="3d09f-355">Specifies the average bytes per second for VBR encoded audio.</span></span><br/> <dl> <span data-ttu-id="3d09f-356">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-356">Windows XP and later.</span></span><br />
<span data-ttu-id="3d09f-357">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-357">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-358">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3d09f-358">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-359"><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-359"><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-360">Spécifie si l’encodeur doit produire 1 paquet WMA par trame.</span><span class="sxs-lookup"><span data-stu-id="3d09f-360">Specifies whether the encoder should produce 1 WMA packet per frame.</span></span><br/> <dl> <span data-ttu-id="3d09f-361">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-361">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-362">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-362">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-363">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-363">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-364"><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-364"><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-365">Spécifie si l’encodeur doit générer des paramètres de contrôle de plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="3d09f-365">Specifies whether the encoder should generate dynamic range control parameters.</span></span><br/> <dl> <span data-ttu-id="3d09f-366">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-366">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-367">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="3d09f-367">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="3d09f-368">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-368">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d09f-369"><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-369"><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-370">Spécifie la structure <strong>WAVEFORMATEX</strong> décrivant le contenu audio d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3d09f-370">Specifies the <strong>WAVEFORMATEX</strong> structure describing the input audio content.</span></span><br/> <dl> <span data-ttu-id="3d09f-371">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-371">Windows XP and later.</span></span><br />
<span data-ttu-id="3d09f-372">Standard, professionnel.</span><span class="sxs-lookup"><span data-stu-id="3d09f-372">Standard, Professional.</span></span><br />
<span data-ttu-id="3d09f-373">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-373">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d09f-374"><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d09f-374"><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></span></span></td>
<td><span data-ttu-id="3d09f-375">Spécifie si l’encodeur doit activer l’encodage S/PDIF en temps réel.</span><span class="sxs-lookup"><span data-stu-id="3d09f-375">Specifies whether the encoder should enable real-time S/PDIF encoding .</span></span><br/> <dl> <span data-ttu-id="3d09f-376">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d09f-376">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d09f-377">Professionnel.</span><span class="sxs-lookup"><span data-stu-id="3d09f-377">Professional.</span></span><br />
<span data-ttu-id="3d09f-378">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d09f-378">Read/write.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="3d09f-379">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d09f-379">Requirements</span></span>



| <span data-ttu-id="3d09f-380">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d09f-380">Requirement</span></span> | <span data-ttu-id="3d09f-381">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d09f-381">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d09f-382">Client</span><span class="sxs-lookup"><span data-stu-id="3d09f-382">Client</span></span><br/> | <span data-ttu-id="3d09f-383">Windows XP, Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d09f-383">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="3d09f-384">En-tête</span><span class="sxs-lookup"><span data-stu-id="3d09f-384">Header</span></span><br/> | <dl> <span data-ttu-id="3d09f-385"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d09f-385"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="3d09f-386">DLL</span><span class="sxs-lookup"><span data-stu-id="3d09f-386">DLL</span></span><br/>    | <dl> <span data-ttu-id="3d09f-387"><dt>Wmadmoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d09f-387"><dt>Wmadmoe.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3d09f-388">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d09f-388">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d09f-389">Objets codec</span><span class="sxs-lookup"><span data-stu-id="3d09f-389">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="3d09f-390">Implémentation du codec</span><span class="sxs-lookup"><span data-stu-id="3d09f-390">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 




