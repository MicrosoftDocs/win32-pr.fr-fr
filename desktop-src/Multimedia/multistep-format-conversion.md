---
title: Conversion de format à étapes
description: Conversion de format à étapes
ms.assetid: 21d837e7-d665-461d-9676-68add3829fb0
keywords:
- Gestionnaire de compression audio (ACM), conversion de données
- ACM (gestionnaire de compression audio), conversion de données
- Exemples ACM, conversion de données
- convertir des données
- acmFormatSuggest fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e81ebd5bef17d6a97cb5735e15219c39d3116b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940020"
---
# <a name="multistep-format-conversion"></a><span data-ttu-id="ad2e9-108">Conversion de format à étapes</span><span class="sxs-lookup"><span data-stu-id="ad2e9-108">Multistep Format Conversion</span></span>

<span data-ttu-id="ad2e9-109">Parfois, l’ACM ne peut pas convertir les données d’un format à un autre en une seule étape.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-109">Sometimes the ACM cannot convert data from one format to another in a single step.</span></span> <span data-ttu-id="ad2e9-110">Par exemple, une application peut avoir besoin de convertir des données stéréo 16 bits 44-kHz en ADPCM mono 11-kHz.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-110">For example, an application might need to convert 16-bit, 44-kHz stereo data to 11-kHz mono ADPCM.</span></span> <span data-ttu-id="ad2e9-111">Si le compresseur ou le décompresseur ne peut pas effectuer cette conversion directement, l’application peut l’essayer en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-111">If the compressor or decompressor cannot do this conversion directly, the application might attempt it in two steps.</span></span> <span data-ttu-id="ad2e9-112">Cela signifie généralement qu’il y a une conversion entre deux formats PCM, puis une autre conversion vers le type de format final.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-112">This usually means making one conversion between two PCM formats, then another conversion to the final format type.</span></span>

<span data-ttu-id="ad2e9-113">Pour effectuer une conversion en deux étapes, utilisez la fonction [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) pour rechercher un format PCM qui correspond au format ADPCM.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-113">To convert in two steps, use the [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) function to find a PCM format that matches the ADPCM format.</span></span> <span data-ttu-id="ad2e9-114">Utilisez ensuite deux flux de conversion pour effectuer la conversion.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-114">Then use two conversion streams to perform the conversion.</span></span> <span data-ttu-id="ad2e9-115">Par exemple, effectuez une conversion du PCM stéréo 16 bits, 44-kHz vers la valeur mono 16 bits, 11 kHz, puis convertissez-les de 16 bits, de 11 kHz mono à 11-kHz Mono ADPCM.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-115">For example, perform one conversion from 16-bit, 44-kHz stereo PCM to 16-bit, 11-kHz mono, then convert from 16-bit, 11-kHz mono to 11-kHz mono ADPCM.</span></span>

<span data-ttu-id="ad2e9-116">La conversion en une seule étape se produit également lorsque le format source ou de destination n’est pas PCM.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-116">Multistep conversion also happens when either the source or the destination format is not PCM.</span></span> <span data-ttu-id="ad2e9-117">Si le format source n’est pas PCM, vous devez le remplacer par un format PCM avant la conversion.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-117">If the source format is not PCM, it should be changed to a PCM format before conversion.</span></span> <span data-ttu-id="ad2e9-118">Si le format de destination n’est pas PCM, la source doit être convertie au format PCM intermédiaire, puis convertie au format de destination final.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-118">If the destination format is not PCM, the source must be converted to an intermediate PCM format and then converted to the final destination format.</span></span>

<span data-ttu-id="ad2e9-119">Les conversions les plus simples se produisent lorsque les formats source et destination sont tous deux des formats PCM.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-119">The most straightforward conversions occur when the source and destination formats are both PCM formats.</span></span> <span data-ttu-id="ad2e9-120">Lorsque le format source ou de destination n’est pas PCM, la conversion peut nécessiter une étape supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-120">When either the source or destination format is not PCM, the conversion might require an additional step.</span></span> <span data-ttu-id="ad2e9-121">Si les formats source et de destination ne sont pas PCM, la conversion nécessitera généralement plus d’une étape et, dans certains cas, la conversion peut ne pas être possible.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-121">If both source and destination formats are not PCM, the conversion will usually require more than one step, and, in some instances, conversion might not be possible.</span></span>

 

 




