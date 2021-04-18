---
title: Types de médias pour Windows Media Format SDK
description: En savoir plus sur les types de médias qui peuvent être utilisés par le kit de développement logiciel (SDK) Windows Media format. Les types de média sont des valeurs GUID affectées à des constantes dans le kit de développement logiciel (SDK).
ms.assetid: 00dcbb20-09ed-44c5-992c-20f3d17ad47c
keywords:
- Windows Media Format SDK, types de média
- ASF (Advanced Systems Format), types de média
- ASF (format des systèmes avancés), types de média
- types de média, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6d15255ab311c67562a6c9dde83650240b0803
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106533528"
---
# <a name="media-types-for-windows-media-format-sdk"></a><span data-ttu-id="c07f5-108">Types de médias pour Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="c07f5-108">Media Types for Windows Media Format SDK</span></span>

<span data-ttu-id="c07f5-109">Les types de médias identifient les différents types de médias qui peuvent être utilisés par le kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="c07f5-109">Media types identify the different types of media that can be used by the Windows Media Format SDK.</span></span> <span data-ttu-id="c07f5-110">Tous les types de média sont des valeurs GUID qui ont été affectées à des constantes dans le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="c07f5-110">All media types are GUID values that have been assigned to constants in the SDK.</span></span> <span data-ttu-id="c07f5-111">Les valeurs GUID représentées par les constantes répertoriées dans cette section sont répertoriées dans la section [identificateurs de type de média](media-type-identifiers.md) de cette référence.</span><span class="sxs-lookup"><span data-stu-id="c07f5-111">The GUID values represented by the constants listed in this section are listed in the [Media Type Identifiers](media-type-identifiers.md) section of this reference.</span></span>

<span data-ttu-id="c07f5-112">Le tableau suivant répertorie les principaux types de médias.</span><span class="sxs-lookup"><span data-stu-id="c07f5-112">The following table lists major media types.</span></span> <span data-ttu-id="c07f5-113">Ces constantes définissent la classification générale des supports numériques pris en charge par le kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c07f5-113">These constants define the high level classification of digital media supported by the Windows Media Format SDK.</span></span>



| <span data-ttu-id="c07f5-114">Type principal</span><span class="sxs-lookup"><span data-stu-id="c07f5-114">Major type</span></span>                | <span data-ttu-id="c07f5-115">Description</span><span class="sxs-lookup"><span data-stu-id="c07f5-115">Description</span></span>                                                                                             |
|---------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c07f5-116">\_Vidéo WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="c07f5-116">WMMEDIATYPE\_Video</span></span>        | <span data-ttu-id="c07f5-117">Flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="c07f5-117">A video stream.</span></span>                                                                                         |
| <span data-ttu-id="c07f5-118">WMMEDIATYPE \_ audio</span><span class="sxs-lookup"><span data-stu-id="c07f5-118">WMMEDIATYPE\_Audio</span></span>        | <span data-ttu-id="c07f5-119">Flux audio.</span><span class="sxs-lookup"><span data-stu-id="c07f5-119">An audio stream.</span></span>                                                                                        |
| <span data-ttu-id="c07f5-120">\_Script WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="c07f5-120">WMMEDIATYPE\_Script</span></span>       | <span data-ttu-id="c07f5-121">Flux de script.</span><span class="sxs-lookup"><span data-stu-id="c07f5-121">A script stream.</span></span>                                                                                        |
| <span data-ttu-id="c07f5-122">WMMEDIATYPE \_ filetransfer</span><span class="sxs-lookup"><span data-stu-id="c07f5-122">WMMEDIATYPE\_FileTransfer</span></span> | <span data-ttu-id="c07f5-123">Flux qui contient des fichiers de données.</span><span class="sxs-lookup"><span data-stu-id="c07f5-123">A stream that contains data files.</span></span> <span data-ttu-id="c07f5-124">Les flux Web, qui se composent de fichiers HTML, ont également ce type majeur.</span><span class="sxs-lookup"><span data-stu-id="c07f5-124">Web streams, which consist of HTML files, also have this major type.</span></span> |
| <span data-ttu-id="c07f5-125">\_Image WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="c07f5-125">WMMEDIATYPE\_Image</span></span>        | <span data-ttu-id="c07f5-126">Flux d’images JPEG pour un fichier audio illustré (comme dans un diaporama).</span><span class="sxs-lookup"><span data-stu-id="c07f5-126">A JPEG image stream for an illustrated audio file (as in a slide show).</span></span>                                 |
| <span data-ttu-id="c07f5-127">\_Texte WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="c07f5-127">WMMEDIATYPE\_Text</span></span>         | <span data-ttu-id="c07f5-128">Flux de texte.</span><span class="sxs-lookup"><span data-stu-id="c07f5-128">A text stream.</span></span>                                                                                          |



 

<span data-ttu-id="c07f5-129">Outre les types de média majeurs pris en charge explicitement, vous pouvez créer vos propres types de données arbitraires.</span><span class="sxs-lookup"><span data-stu-id="c07f5-129">In addition to the explicitly supported major media types, you can create your own arbitrary data types.</span></span> <span data-ttu-id="c07f5-130">Pour les types de données arbitraires personnalisés, vous devez vous assurer que le GUID que vous utilisez ne correspond pas à un type majeur existant.</span><span class="sxs-lookup"><span data-stu-id="c07f5-130">For custom arbitrary data types, you must ensure that the GUID you use does not match an existing major type.</span></span>

<span data-ttu-id="c07f5-131">Un flux de média aura souvent un sous-type en plus de son type principal.</span><span class="sxs-lookup"><span data-stu-id="c07f5-131">A media stream will often have a subtype in addition to its major type.</span></span> <span data-ttu-id="c07f5-132">Les sections suivantes répertorient les sous-types pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c07f5-132">The following sections list the supported subtypes.</span></span>



| <span data-ttu-id="c07f5-133">Section</span><span class="sxs-lookup"><span data-stu-id="c07f5-133">Section</span></span>                                                        | <span data-ttu-id="c07f5-134">Description</span><span class="sxs-lookup"><span data-stu-id="c07f5-134">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c07f5-135">Sous-types de médias non compressés</span><span class="sxs-lookup"><span data-stu-id="c07f5-135">Uncompressed Media Subtypes</span></span>](uncompressed-media-subtypes.md) | <span data-ttu-id="c07f5-136">Décrit les sous-types disponibles pour les médias non compressés.</span><span class="sxs-lookup"><span data-stu-id="c07f5-136">Describes the subtypes available for uncompressed media.</span></span> <span data-ttu-id="c07f5-137">Ce sont les types généralement associés à un média d’entrée ou de sortie.</span><span class="sxs-lookup"><span data-stu-id="c07f5-137">These are the types typically associated with input or output media.</span></span>              |
| [<span data-ttu-id="c07f5-138">Sous-types de média compressés</span><span class="sxs-lookup"><span data-stu-id="c07f5-138">Compressed Media Subtypes</span></span>](compressed-media-subtypes.md)     | <span data-ttu-id="c07f5-139">Décrit les sous-types disponibles pour les médias compressés.</span><span class="sxs-lookup"><span data-stu-id="c07f5-139">Describes the subtypes available for compressed media.</span></span> <span data-ttu-id="c07f5-140">Ce sont les types généralement associés à des médias dans un flux d’un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="c07f5-140">These are the types typically associated with media in a stream within an ASF file.</span></span> |
| [<span data-ttu-id="c07f5-141">Formats d’entrée vidéo</span><span class="sxs-lookup"><span data-stu-id="c07f5-141">Video Input Formats</span></span>](video-input-formats.md)                 | <span data-ttu-id="c07f5-142">Répertorie les formats vidéo acceptés en tant qu’entrées pour le codec Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="c07f5-142">Lists the video formats accepted as inputs for the Windows Media Video 9 codec.</span></span>                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="c07f5-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c07f5-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c07f5-144">**Identificateurs de type de média**</span><span class="sxs-lookup"><span data-stu-id="c07f5-144">**Media Type Identifiers**</span></span>](media-type-identifiers.md)
</dt> <dt>

[<span data-ttu-id="c07f5-145">**Guide de référence de programmation**</span><span class="sxs-lookup"><span data-stu-id="c07f5-145">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 




