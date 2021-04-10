---
description: Cette section décrit comment configurer les flux VBR.
ms.assetid: 9dd3ff5b-4c7c-41a8-b1b9-7ea380175193
title: Utilisation de l’encodage VBR (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd1f317308d79c696e26a8671cc9d84ca8effa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201840"
---
# <a name="using-vbr-encoding-microsoft-media-foundation"></a><span data-ttu-id="7498c-103">Utilisation de l’encodage VBR (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="7498c-103">Using VBR Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="7498c-104">Comme indiqué dans la rubrique [méthodes d’encodage](encodingmethods.md) , l’encodage VBR (variable bit rate) est utilisé pour améliorer la cohérence de la qualité du contenu.</span><span class="sxs-lookup"><span data-stu-id="7498c-104">As detailed in the [Encoding Methods](encodingmethods.md) topic, variable bit rate (VBR) encoding is used to improve the consistency of content quality.</span></span> <span data-ttu-id="7498c-105">Vous configurez les flux VBR de la même façon que vous encodez des flux à débit binaire constant (CBR), à l’exception des paramètres de mémoire tampon (vitesse de transmission et mémoire tampon).</span><span class="sxs-lookup"><span data-stu-id="7498c-105">You configure VBR streams in the same way that you encode constant bit rate (CBR) streams, except for the buffer parameters (bit rate and buffer window).</span></span> <span data-ttu-id="7498c-106">Cette section décrit comment configurer les flux VBR.</span><span class="sxs-lookup"><span data-stu-id="7498c-106">This section describes how to configure VBR streams.</span></span>

## <a name="configuring-quality-based-vbr"></a><span data-ttu-id="7498c-107">Configuration du VBR basé sur la qualité</span><span class="sxs-lookup"><span data-stu-id="7498c-107">Configuring Quality Based VBR</span></span>

<span data-ttu-id="7498c-108">L’encodage à l’aide de la méthode VBR basée sur la qualité ne requiert pas de paramètres de mémoire tampon prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="7498c-108">Encoding using the quality based VBR method does not require any predefined buffer parameters.</span></span> <span data-ttu-id="7498c-109">Au lieu de cela, vous spécifiez un niveau de qualité (compris entre 0 et 100) que l’encodeur utilise pour déterminer dynamiquement les paramètres de mémoire tampon appropriés.</span><span class="sxs-lookup"><span data-stu-id="7498c-109">Instead, you specify a quality level (from 0 to 100) which the encoder uses to determine the appropriate buffer parameters dynamically.</span></span> <span data-ttu-id="7498c-110">Ce mode d’encodage n’utilise qu’un seul passe d’encodage.</span><span class="sxs-lookup"><span data-stu-id="7498c-110">This encoding mode uses only one encoding pass.</span></span>

<span data-ttu-id="7498c-111">Vous pouvez énumérer les types de sortie VBR basés sur la qualité pris en charge pour les codecs audio.</span><span class="sxs-lookup"><span data-stu-id="7498c-111">You can enumerate the supported quality-based VBR output types for the audio codecs.</span></span> <span data-ttu-id="7498c-112">Vous devez utiliser l’un des types retournés par DMO lors de la définition du type de sortie.</span><span class="sxs-lookup"><span data-stu-id="7498c-112">You must use one of the types returned by the DMO when setting the output type.</span></span> <span data-ttu-id="7498c-113">Pour plus d’informations, consultez [énumération des types audio pour des modes d’encodage spécifiques](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="7498c-113">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="7498c-114">Pour configurer un flux vidéo VBR basé sur la qualité, vous devez définir les propriétés qui sont répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7498c-114">To configure a quality-based VBR video stream, you must set the properties that are listed in the following table.</span></span>



| <span data-ttu-id="7498c-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="7498c-115">Property</span></span>                                            | <span data-ttu-id="7498c-116">Description</span><span class="sxs-lookup"><span data-stu-id="7498c-116">Description</span></span>                                                                                                                                             |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7498c-117">MFPKEY \_ VBRENABLED</span><span class="sxs-lookup"><span data-stu-id="7498c-117">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="7498c-118">A la valeur VARIANT \_ true.</span><span class="sxs-lookup"><span data-stu-id="7498c-118">Set to VARIANT\_TRUE.</span></span>                                                                                                                                   |
| [<span data-ttu-id="7498c-119">MFPKEY \_ VBRQUALITY</span><span class="sxs-lookup"><span data-stu-id="7498c-119">MFPKEY\_VBRQUALITY</span></span>](mfpkey-vbrqualityproperty.md) | <span data-ttu-id="7498c-120">Définissez sur la valeur de qualité souhaitée, de 0 à 100.</span><span class="sxs-lookup"><span data-stu-id="7498c-120">Set to the desired quality value, from 0 to 100.</span></span> <span data-ttu-id="7498c-121">Toutes les valeurs de qualité ne représentent pas des paramètres discrets.</span><span class="sxs-lookup"><span data-stu-id="7498c-121">Not all quality values represent discrete settings.</span></span> <span data-ttu-id="7498c-122">Pour plus d’informations, consultez la description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="7498c-122">See the property description for more information.</span></span> |



 

## <a name="configuring-unconstrained-vbr"></a><span data-ttu-id="7498c-123">Configuration de la VBR sans contrainte</span><span class="sxs-lookup"><span data-stu-id="7498c-123">Configuring Unconstrained VBR</span></span>

<span data-ttu-id="7498c-124">L’encodage VBR non restreint permet à l’encodeur de modifier la taille des échantillons individuels sans aucune limite de mémoire tampon explicite.</span><span class="sxs-lookup"><span data-stu-id="7498c-124">Unconstrained VBR encoding enables the encoder to vary the size of individual samples without any explicit buffer limits.</span></span> <span data-ttu-id="7498c-125">Toutefois, la vitesse de transmission moyenne sur la durée du contenu résultant doit être inférieure ou égale à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7498c-125">However, the average bit rate over the duration of the resulting content must be less than or equal to the specified value.</span></span> <span data-ttu-id="7498c-126">Le VBR sans contrainte requiert deux passes d’encodage.</span><span class="sxs-lookup"><span data-stu-id="7498c-126">Unconstrained VBR requires two encoding passes.</span></span>

<span data-ttu-id="7498c-127">Vous pouvez énumérer les types de sortie VBR en deux passes pris en charge pour les codecs audio.</span><span class="sxs-lookup"><span data-stu-id="7498c-127">You can enumerate the supported two-pass VBR output types for the audio codecs.</span></span> <span data-ttu-id="7498c-128">Vous devez utiliser l’un des types retournés par DMO lors de la définition du type de sortie.</span><span class="sxs-lookup"><span data-stu-id="7498c-128">You must use one of the types returned by the DMO when setting the output type.</span></span> <span data-ttu-id="7498c-129">Pour plus d’informations, consultez [énumération des types audio pour des modes d’encodage spécifiques](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="7498c-129">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="7498c-130">Pour configurer un flux vidéo VBR non restreint, vous devez définir les propriétés répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7498c-130">To configure an unconstrained VBR video stream, you must set the properties that are listed in the following table.</span></span>



| <span data-ttu-id="7498c-131">Propriété</span><span class="sxs-lookup"><span data-stu-id="7498c-131">Property</span></span>                                            | <span data-ttu-id="7498c-132">Description</span><span class="sxs-lookup"><span data-stu-id="7498c-132">Description</span></span>                          |
|-----------------------------------------------------|--------------------------------------|
| [<span data-ttu-id="7498c-133">MFPKEY \_ VBRENABLED</span><span class="sxs-lookup"><span data-stu-id="7498c-133">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="7498c-134">A la valeur VARIANT \_ true.</span><span class="sxs-lookup"><span data-stu-id="7498c-134">Set to VARIANT\_TRUE.</span></span>                |
| [<span data-ttu-id="7498c-135">MFPKEY \_ PASSESUSED</span><span class="sxs-lookup"><span data-stu-id="7498c-135">MFPKEY\_PASSESUSED</span></span>](mfpkey-passesusedproperty.md) | <span data-ttu-id="7498c-136">Défini sur 2.</span><span class="sxs-lookup"><span data-stu-id="7498c-136">Set to 2.</span></span>                            |
| [<span data-ttu-id="7498c-137">MFPKEY \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="7498c-137">MFPKEY\_RAVG</span></span>](mfpkey-ravgproperty.md)             | <span data-ttu-id="7498c-138">Définissez sur la vitesse de transmission moyenne souhaitée.</span><span class="sxs-lookup"><span data-stu-id="7498c-138">Set to the desired average bit rate.</span></span> |



 

## <a name="configuring-peak-constrained-vbr"></a><span data-ttu-id="7498c-139">Configuration de Peak-Constrained VBR</span><span class="sxs-lookup"><span data-stu-id="7498c-139">Configuring Peak-Constrained VBR</span></span>

<span data-ttu-id="7498c-140">Le VBR limité au maximum est comme un VBR non restreint en ce qu’il est limité à un débit binaire moyen sur la durée du flux.</span><span class="sxs-lookup"><span data-stu-id="7498c-140">Peak-constrained VBR is like unconstrained VBR in that it is confined to an average bit rate over the duration of the stream.</span></span> <span data-ttu-id="7498c-141">En outre, le VBR maximal restreint est conforme à une mémoire tampon de pointe.</span><span class="sxs-lookup"><span data-stu-id="7498c-141">In addition, peak-constrained VBR conforms to a peak buffer.</span></span> <span data-ttu-id="7498c-142">Cette mémoire tampon est décrite à l’aide d’un taux binaire de pointe et d’une fenêtre de mémoire tampon de pointe, tout comme une mémoire tampon CBR est décrite par une vitesse de transmission moyenne et une fenêtre de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7498c-142">This buffer is described using a peak bit rate and a peak buffer window, just as a CBR buffer is described by an average bit rate and a buffer window.</span></span> <span data-ttu-id="7498c-143">Ce mode offre à la flexibilité de l’encodeur la manière dont il encode des exemples individuels tout en adhérant aux limitations de pointe.</span><span class="sxs-lookup"><span data-stu-id="7498c-143">This mode gives the encoder flexibility in how it encodes individual samples while adhering to the peak limitations.</span></span> <span data-ttu-id="7498c-144">Cela s’avère particulièrement utile lorsque le décodage est effectué par une puce dans un appareil, comme un lecteur de DVD, où des limitations matérielles doivent être prises en compte.</span><span class="sxs-lookup"><span data-stu-id="7498c-144">This is particularly useful when decoding is performed by a chip in a device, like a DVD player, where there are hardware limitations that must be considered.</span></span>

<span data-ttu-id="7498c-145">Les types de sortie de l’encodeur audio VBR les plus pertenus pris en charge sont les mêmes que ceux énumérés pour le VBR sans contrainte.</span><span class="sxs-lookup"><span data-stu-id="7498c-145">The supported peak-constrained, VBR audio encoder output types are the same types enumerated for unconstrained VBR.</span></span> <span data-ttu-id="7498c-146">Définissez les valeurs de pic sur DMO et utilisez le type remis.</span><span class="sxs-lookup"><span data-stu-id="7498c-146">Set the peak values on the DMO and use the delivered type.</span></span> <span data-ttu-id="7498c-147">Pour plus d’informations, consultez [énumération des types audio pour des modes d’encodage spécifiques](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="7498c-147">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="7498c-148">Pour configurer un flux vidéo VBR avec des pics de charge, vous devez définir les propriétés répertoriées dans le tableau suivant à l’aide de la méthode **IPropertyBag :: Write** .</span><span class="sxs-lookup"><span data-stu-id="7498c-148">To configure a peak-constrained VBR video stream, you must set the properties that are listed in the following table using the **IPropertyBag::Write** method.</span></span>



| <span data-ttu-id="7498c-149">Propriété</span><span class="sxs-lookup"><span data-stu-id="7498c-149">Property</span></span>                                            | <span data-ttu-id="7498c-150">Description</span><span class="sxs-lookup"><span data-stu-id="7498c-150">Description</span></span>                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="7498c-151">MFPKEY \_ VBRENABLED</span><span class="sxs-lookup"><span data-stu-id="7498c-151">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="7498c-152">A la valeur VARIANT \_ true.</span><span class="sxs-lookup"><span data-stu-id="7498c-152">Set to VARIANT\_TRUE.</span></span>                                           |
| [<span data-ttu-id="7498c-153">MFPKEY \_ PASSESUSED</span><span class="sxs-lookup"><span data-stu-id="7498c-153">MFPKEY\_PASSESUSED</span></span>](mfpkey-passesusedproperty.md) | <span data-ttu-id="7498c-154">Défini sur 2.</span><span class="sxs-lookup"><span data-stu-id="7498c-154">Set to 2.</span></span>                                                       |
| [<span data-ttu-id="7498c-155">MFPKEY \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="7498c-155">MFPKEY\_RAVG</span></span>](mfpkey-ravgproperty.md)             | <span data-ttu-id="7498c-156">Définissez sur la vitesse de transmission moyenne souhaitée.</span><span class="sxs-lookup"><span data-stu-id="7498c-156">Set to the desired average bit rate.</span></span>                            |
| [<span data-ttu-id="7498c-157">MFPKEY \_ Rmax</span><span class="sxs-lookup"><span data-stu-id="7498c-157">MFPKEY\_RMAX</span></span>](mfpkey-rmaxproperty.md)             | <span data-ttu-id="7498c-158">Définissez sur le taux binaire de pointe souhaité.</span><span class="sxs-lookup"><span data-stu-id="7498c-158">Set to the desired peak bit rate.</span></span>                               |
| [<span data-ttu-id="7498c-159">MFPKEY \_ BMAX</span><span class="sxs-lookup"><span data-stu-id="7498c-159">MFPKEY\_BMAX</span></span>](mfpkey-bmaxproperty.md)             | <span data-ttu-id="7498c-160">Définissez sur la fenêtre de mémoire tampon qui correspond au taux de bits de pointe.</span><span class="sxs-lookup"><span data-stu-id="7498c-160">Set to the buffer window that corresponds to the peak bit rate.</span></span> |



 

> [!Note]  
> <span data-ttu-id="7498c-161">Il est recommandé de définir le taux de bits de pointe sur au moins deux fois la vitesse de transmission moyenne.</span><span class="sxs-lookup"><span data-stu-id="7498c-161">It is recommended that you set the peak bit rate to at least twice the average bit rate.</span></span> <span data-ttu-id="7498c-162">Si vous affectez une valeur inférieure au taux de pic, le codec peut encoder le contenu en deux passes CBR au lieu du VBR maximal.</span><span class="sxs-lookup"><span data-stu-id="7498c-162">Setting the peak rate to a lower value may cause the codec to encode the content as two-pass CBR instead of peak-constrained VBR.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7498c-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7498c-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7498c-164">Codecs Windows Media</span><span class="sxs-lookup"><span data-stu-id="7498c-164">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> <dt>

[<span data-ttu-id="7498c-165">Utilisation de l’encodage Two-Pass</span><span class="sxs-lookup"><span data-stu-id="7498c-165">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
</dt> <dt>

[<span data-ttu-id="7498c-166">Utilisation de l’audio</span><span class="sxs-lookup"><span data-stu-id="7498c-166">Working with Audio</span></span>](workingwithaudio.md)
</dt> <dt>

[<span data-ttu-id="7498c-167">Utilisation de la vidéo</span><span class="sxs-lookup"><span data-stu-id="7498c-167">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



