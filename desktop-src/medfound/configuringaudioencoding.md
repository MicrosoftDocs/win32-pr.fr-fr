---
description: Configuration de l’encodage audio
ms.assetid: 40004f07-0b8c-49cd-9e17-1f6ad7604fbb
title: Configuration de l’encodage audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e47595f440d10ad0d3c5695f117204f357035d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201172"
---
# <a name="configuring-audio-encoding-microsoft-media-foundation"></a><span data-ttu-id="626ee-103">Configuration de l’encodage audio (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="626ee-103">Configuring Audio Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="626ee-104">L’encodeur Windows Media Audio énumère tous les types de sortie pris en charge dans leur forme complète.</span><span class="sxs-lookup"><span data-stu-id="626ee-104">The Windows Media Audio encoder enumerates all of its supported output types in their complete form.</span></span> <span data-ttu-id="626ee-105">Récupérez le type souhaité en appelant **IMediaObject :: GetOutputType** ou **IMFTransform :: GetAvailableOutputType**, puis définissez le type récupéré, non modifié, comme type de sortie en appelant **IMediaObject :: SetOutputType** ou **IMFTransform :: SetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="626ee-105">Retrieve the type that you want by calling **IMediaObject::GetOutputType** or **IMFTransform::GetAvailableOutputType**, and then set the retrieved type, unaltered, as the output type by calling **IMediaObject::SetOutputType** or **IMFTransform::SetOutputType**.</span></span>

<span data-ttu-id="626ee-106">Les types de supports de sortie pris en charge par les propriétés changer d’encodeur audio sont configurés.</span><span class="sxs-lookup"><span data-stu-id="626ee-106">The output media types supported by the audio encoder change as encoder properties are configured.</span></span> <span data-ttu-id="626ee-107">Vous devez configurer toutes les propriétés d’encodeur que vous souhaitez utiliser avant d’énumérer le type de sortie.</span><span class="sxs-lookup"><span data-stu-id="626ee-107">You must configure all of the encoder properties you want to use before you enumerate the output type.</span></span>

<span data-ttu-id="626ee-108">Les modes deux-passe et VBR sont pris en charge par les encodeurs audio, mais ils sont configurés différemment de pour la vidéo.</span><span class="sxs-lookup"><span data-stu-id="626ee-108">Two-pass and VBR modes are supported by the audio encoders, but are configured differently than for video.</span></span> <span data-ttu-id="626ee-109">Pour plus d’informations, consultez [énumération des types audio pour des modes d’encodage spécifiques](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="626ee-109">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="626ee-110">Les types d’entrée pris en charge par l’encodeur audio ne sont pas disponibles tant que vous n’avez pas défini le type de sortie.</span><span class="sxs-lookup"><span data-stu-id="626ee-110">The input types supported by the audio encoder are not available until you set the output type.</span></span> <span data-ttu-id="626ee-111">Si vous appelez **IMediaObject :: GetInputType** ou **IMFTransform :: GetInputType** avant de définir un type de sortie, la méthode retourne DMO \_ e \_ n’a plus d' \_ \_ éléments ni de MFT \_ e plus de types, \_ \_ \_ respectivement.</span><span class="sxs-lookup"><span data-stu-id="626ee-111">If you call **IMediaObject::GetInputType** or **IMFTransform::GetInputType** before setting an output type, the method returns DMO\_E\_NO\_MORE\_ITEMS or MFT\_E\_NO\_MORE\_TYPES respectively.</span></span> <span data-ttu-id="626ee-112">Une fois que le type de sortie est défini, l’encodeur énumère les types d’entrée qu’il prend en charge pour le type de sortie sélectionné.</span><span class="sxs-lookup"><span data-stu-id="626ee-112">After the output type is set, the encoder enumerates the input types that it supports for the selected output type.</span></span>

<span data-ttu-id="626ee-113">Aucun rééchantillonnage audio n’est effectué par l’encodeur Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="626ee-113">No audio resampling is performed by the Windows Media Audio encoder.</span></span> <span data-ttu-id="626ee-114">Cela signifie que le type de sortie de l’encodeur et le type d’entrée de l’encodeur doivent avoir le même nombre de canaux, le nombre de bits par échantillon et le taux d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="626ee-114">This means that the encoder output type and the encoder input type must have the same number of channels, bits per sample, and sample rate.</span></span> <span data-ttu-id="626ee-115">Pour plus d’informations, consultez [recherche de types de sortie d’encodeur audio](findingaudioencoderoutputtypes.md).</span><span class="sxs-lookup"><span data-stu-id="626ee-115">For more information, see [Finding Audio Encoder Output Types](findingaudioencoderoutputtypes.md).</span></span>

> [!Note]  
>    <span data-ttu-id="626ee-116">Chaque type de sortie énuméré par l’encodeur audio contient une structure **WAVEFORMATEX** (pointée par **am \_ Media \_ type. pbFormat**) avec les données étendues qui lui sont ajoutées.</span><span class="sxs-lookup"><span data-stu-id="626ee-116">Each output type enumerated by the audio encoder contains a **WAVEFORMATEX** structure (pointed to by **AM\_MEDIA\_TYPE.pbFormat**) with extended data appended to it.</span></span> <span data-ttu-id="626ee-117">La taille des données étendues est spécifiée par **WAVEFORMATEX. cbSize**.</span><span class="sxs-lookup"><span data-stu-id="626ee-117">The size of the extended data is specified by **WAVEFORMATEX.cbSize**.</span></span> <span data-ttu-id="626ee-118">Ces données doivent être conservées avec le contenu encodé afin qu’elles puissent être remises au décodeur.</span><span class="sxs-lookup"><span data-stu-id="626ee-118">This data must be kept with the encoded content so that it can be delivered to the decoder.</span></span> <span data-ttu-id="626ee-119">Impossible de décompresser le contenu sans les données de format étendu.</span><span class="sxs-lookup"><span data-stu-id="626ee-119">The content cannot be decompressed without the extended format data.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="626ee-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="626ee-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="626ee-121">Utilisation de l’audio</span><span class="sxs-lookup"><span data-stu-id="626ee-121">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



