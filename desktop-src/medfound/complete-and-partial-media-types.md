---
description: Cette rubrique décrit la différence entre les types de médias complets et les types de média partiels.
ms.assetid: 59b3f0b5-f378-41e6-9b49-85a16bb6e008
title: Types de média complets et partiels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac772c09668ee3db96e42d25b3089fa74be104af
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530525"
---
# <a name="complete-and-partial-media-types"></a><span data-ttu-id="86023-103">Types de média complets et partiels</span><span class="sxs-lookup"><span data-stu-id="86023-103">Complete and Partial Media Types</span></span>

<span data-ttu-id="86023-104">Cette rubrique décrit la différence entre les types de médias complets et les types de média partiels.</span><span class="sxs-lookup"><span data-stu-id="86023-104">This topic describes the difference between complete media types and partial media types.</span></span>

## <a name="complete-media-types"></a><span data-ttu-id="86023-105">Types de médias complets</span><span class="sxs-lookup"><span data-stu-id="86023-105">Complete Media Types</span></span>

<span data-ttu-id="86023-106">Un type de média *complet* est un type qui définit complètement le format du flux multimédia.</span><span class="sxs-lookup"><span data-stu-id="86023-106">A *complete* media type is one that fully defines the format of the media stream.</span></span> <span data-ttu-id="86023-107">Étant donné un type de média complet, un composant de pipeline peut analyser les données de flux associées au type de média, sans ambiguïté.</span><span class="sxs-lookup"><span data-stu-id="86023-107">Given a complete media type, a pipeline component can parse the stream data associated with the media type, with no ambiguity.</span></span>

<span data-ttu-id="86023-108">Pour les formats non compressés, les rubriques suivantes définissent les attributs requis pour un type de média complet :</span><span class="sxs-lookup"><span data-stu-id="86023-108">For uncompressed formats, the following topics define the attributes that are required for a complete media type:</span></span>

-   <span data-ttu-id="86023-109">Audio : [types de média audio non compressés](uncompressed-audio-media-types.md)</span><span class="sxs-lookup"><span data-stu-id="86023-109">Audio: [Uncompressed Audio Media Types](uncompressed-audio-media-types.md)</span></span>
-   <span data-ttu-id="86023-110">Vidéo : [types de média vidéo non compressés](uncompressed-video-media-types.md)</span><span class="sxs-lookup"><span data-stu-id="86023-110">Video: [Uncompressed Video Media Types](uncompressed-video-media-types.md)</span></span>

<span data-ttu-id="86023-111">Pour les flux compressés (ou *encodés*), la définition d’un type de média complet est définie par le codec.</span><span class="sxs-lookup"><span data-stu-id="86023-111">For compressed (or *encoded*) streams, the definition of a complete media type is defined by the codec.</span></span> <span data-ttu-id="86023-112">Toutefois, si des attributs de type non compressés sont connus pour le flux compressé, ces valeurs doivent être incluses dans le type de média du flux compressé.</span><span class="sxs-lookup"><span data-stu-id="86023-112">However, if any uncompressed type attributes are known for the compressed stream, these values should be included in the media type for the compressed stream.</span></span> <span data-ttu-id="86023-113">Par exemple, si la taille de trame est connue, définissez l’attribut de [**\_ \_ \_ taille de frame MT MF**](mf-mt-frame-size-attribute.md) sur le type de média, même si techniquement un flux compressé n’a pas de taille de trame.</span><span class="sxs-lookup"><span data-stu-id="86023-113">For example, if the frame size is known, set the [**MF\_MT\_FRAME\_SIZE**](mf-mt-frame-size-attribute.md) attribute on the media type, even though technically a compressed stream does not have a frame size.</span></span>

## <a name="partial-media-types"></a><span data-ttu-id="86023-114">Types de média partiels</span><span class="sxs-lookup"><span data-stu-id="86023-114">Partial Media Types</span></span>

<span data-ttu-id="86023-115">Un type de média *partiel* n’a pas un ou plusieurs des attributs nécessaires pour un type de média complet.</span><span class="sxs-lookup"><span data-stu-id="86023-115">A *partial* media type is lacks one or more of the attributes needed for a complete media type.</span></span> <span data-ttu-id="86023-116">Lors de l’énumération des types de média possibles, un composant Microsoft Media Foundation peut conserver une valeur non définie, pour indiquer qu’il peut gérer n’importe quelle valeur.</span><span class="sxs-lookup"><span data-stu-id="86023-116">When enumerating possible media types, a Microsoft Media Foundation component may leave a value unset, to indicate that it can handle any value.</span></span> <span data-ttu-id="86023-117">Par exemple, un processeur vidéo peut conserver l’attribut de [**\_ fréquence d' \_ images \_ MF MT**](mf-mt-frame-rate-attribute.md) unset, pour indiquer qu’il peut gérer toute fréquence d’images, et effectuera une conversion de fréquence d’images si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="86023-117">For example, a video processor might leave the [**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md) attribute unset, to indicate that it can handle any frame rate, and will perform a frame-rate conversion if necessary.</span></span>

<span data-ttu-id="86023-118">Si vous créez un type de média partiel, vous devez toujours inclure autant d’informations que vous le savez.</span><span class="sxs-lookup"><span data-stu-id="86023-118">If you create a partial media type, you should still include as much information as you know.</span></span> <span data-ttu-id="86023-119">Toutefois, un type de média ne doit pas inclure d’informations incertaines.</span><span class="sxs-lookup"><span data-stu-id="86023-119">However, a media type must not include information that is uncertain.</span></span> <span data-ttu-id="86023-120">Il est préférable de ne pas avoir d’informations erronées.</span><span class="sxs-lookup"><span data-stu-id="86023-120">It is better for information to be missing than wrong.</span></span>

<span data-ttu-id="86023-121">Au minimum, un type de média partiel ne doit inclure que deux attributs : [**MF \_ MT \_ major \_ type**](mf-mt-major-type-attribute.md) et [**MF \_ MT \_ SubType**](mf-mt-subtype-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="86023-121">At a minimum, a partial media type should include just two attributes: [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) and [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md).</span></span>

<span data-ttu-id="86023-122">Parfois Media Foundation composants doivent fournir des types de médias complets :</span><span class="sxs-lookup"><span data-stu-id="86023-122">Sometimes Media Foundation components must provide complete media types:</span></span>

-   <span data-ttu-id="86023-123">Les sources multimédias doivent fournir des types de sortie complets.</span><span class="sxs-lookup"><span data-stu-id="86023-123">Media sources must provide complete output types.</span></span>
-   <span data-ttu-id="86023-124">Les décodeurs doivent fournir des types de sortie complets, une fois que le type d’entrée est défini.</span><span class="sxs-lookup"><span data-stu-id="86023-124">Decoders must provide complete output types, after the input type is set.</span></span> <span data-ttu-id="86023-125">Avant de définir le type d’entrée, un décodeur peut fournir un type de sortie partiel.</span><span class="sxs-lookup"><span data-stu-id="86023-125">Before the input type is set, a decoder might provide a partial output type.</span></span>
-   <span data-ttu-id="86023-126">Les encodeurs doivent fournir des types d’entrée complets, une fois le type de sortie défini.</span><span class="sxs-lookup"><span data-stu-id="86023-126">Encoders must provide complete input types, after the output type is set.</span></span> <span data-ttu-id="86023-127">Avant de définir le type de sortie, un encodeur peut fournir un type d’entrée partiel.</span><span class="sxs-lookup"><span data-stu-id="86023-127">Before the output type is set, an encoder might provide a partial input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86023-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="86023-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86023-129">Types de médias</span><span class="sxs-lookup"><span data-stu-id="86023-129">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 



