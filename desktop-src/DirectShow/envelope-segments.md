---
description: Segments d’enveloppe
ms.assetid: 1b59cd1c-7c37-4c70-a36c-2ee1f42b42c5
title: Segments d’enveloppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bac997667f52ef9bbf14760584889fa16cbbd04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521636"
---
# <a name="envelope-segments"></a><span data-ttu-id="4507f-103">Segments d’enveloppe</span><span class="sxs-lookup"><span data-stu-id="4507f-103">Envelope Segments</span></span>

<span data-ttu-id="4507f-104">Une courbe de paramètres se compose d’un ou de plusieurs segments d’enveloppe, définis à l’aide de la structure de [**\_ \_ segment d’enveloppe MP**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) .</span><span class="sxs-lookup"><span data-stu-id="4507f-104">A parameter curve consists of one or more envelope segments, defined using the [**MP\_ENVELOPE\_SEGMENT**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) structure.</span></span> <span data-ttu-id="4507f-105">Cette structure contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="4507f-105">This structure contains the following information:</span></span>

-   <span data-ttu-id="4507f-106">Heures de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="4507f-106">The start and end times.</span></span>
-   <span data-ttu-id="4507f-107">Valeurs de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="4507f-107">The starting and ending values.</span></span>
-   <span data-ttu-id="4507f-108">Le type de courbe (linéaire, carré, etc.).</span><span class="sxs-lookup"><span data-stu-id="4507f-108">The curve type (linear, square, and so forth).</span></span>
-   <span data-ttu-id="4507f-109">Indicateurs facultatifs, décrits dans un instant.</span><span class="sxs-lookup"><span data-stu-id="4507f-109">Optional flags, described shortly.</span></span>

<span data-ttu-id="4507f-110">Le client ajoute des segments d’enveloppe à un paramètre en appelant la méthode [**IMediaParams :: AddEnvelope**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) et en passant un tableau de structures de **\_ \_ segment d’enveloppe MP** .</span><span class="sxs-lookup"><span data-stu-id="4507f-110">The client adds envelope segments to a parameter by calling the [**IMediaParams::AddEnvelope**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) method and passing in an array of **MP\_ENVELOPE\_SEGMENT** structures.</span></span> <span data-ttu-id="4507f-111">Le client doit trier les segments dans l’ordre chronologique croissant avant d’appeler la méthode.</span><span class="sxs-lookup"><span data-stu-id="4507f-111">The client should sort the segments into ascending time order before calling the method.</span></span> <span data-ttu-id="4507f-112">Au fur et à mesure que DMO traite les données, vous pouvez imaginer le paramètre en déplacement sur chaque segment d’enveloppe, par exemple une voiture qui se dirige sur une série de collines.</span><span class="sxs-lookup"><span data-stu-id="4507f-112">As the DMO processes data, you can imagine the parameter traveling over each envelope segment, like a car driving over a series of hills.</span></span> <span data-ttu-id="4507f-113">La méthode [**IMediaParams :: GetParam**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam) retourne la valeur la plus récente.</span><span class="sxs-lookup"><span data-stu-id="4507f-113">The [**IMediaParams::GetParam**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam) method returns the most recent value.</span></span>

<span data-ttu-id="4507f-114">Deux segments adjacents peuvent avoir un intervalle entre eux.</span><span class="sxs-lookup"><span data-stu-id="4507f-114">Two adjacent segments can have a gap between them.</span></span> <span data-ttu-id="4507f-115">Pendant les lacunes, le paramètre conserve sa valeur précédente, comme suit :</span><span class="sxs-lookup"><span data-stu-id="4507f-115">During gaps, the parameter retains its previous value, as follows:</span></span>

-   <span data-ttu-id="4507f-116">Avant le premier segment, la valeur est la valeur neutre.</span><span class="sxs-lookup"><span data-stu-id="4507f-116">Before the first segment, the value is the neutral value.</span></span>
-   <span data-ttu-id="4507f-117">Entre les segments, la valeur est la valeur de fin du segment précédent.</span><span class="sxs-lookup"><span data-stu-id="4507f-117">Between segments, the value is the ending value of the previous segment.</span></span>
-   <span data-ttu-id="4507f-118">Après le dernier segment, la valeur reste à la valeur de fin de ce segment.</span><span class="sxs-lookup"><span data-stu-id="4507f-118">After the last segment, the value remains at the ending value of that segment.</span></span>
-   <span data-ttu-id="4507f-119">Si le client vide le DMO, la valeur est rétablie à la valeur neutre.</span><span class="sxs-lookup"><span data-stu-id="4507f-119">If the client flushes the DMO, the value reverts to the neutral value.</span></span>

<span data-ttu-id="4507f-120">Vous pouvez modifier un segment en définissant l’un des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="4507f-120">You can alter a segment by setting either of the following flags:</span></span>

-   <span data-ttu-id="4507f-121">MPF \_ ENVLP \_ Begin \_ CURRENTVAL.</span><span class="sxs-lookup"><span data-stu-id="4507f-121">MPF\_ENVLP\_BEGIN\_CURRENTVAL.</span></span> <span data-ttu-id="4507f-122">DMO utilise la valeur la plus récente du paramètre comme valeur de départ du segment.</span><span class="sxs-lookup"><span data-stu-id="4507f-122">The DMO uses the most recent value of the parameter as the starting value for the segment.</span></span> <span data-ttu-id="4507f-123">Il peut s’agir de la valeur neutre ou de la valeur de fin du segment précédent.</span><span class="sxs-lookup"><span data-stu-id="4507f-123">This might be the neutral value, or the ending value from the previous segment.</span></span> <span data-ttu-id="4507f-124">DMO ignore le membre **valStart** de la structure **du \_ \_ segment d’enveloppe MP** .</span><span class="sxs-lookup"><span data-stu-id="4507f-124">The DMO ignores the **valStart** member of the **MP\_ENVELOPE\_SEGMENT** structure.</span></span>
-   <span data-ttu-id="4507f-125">MPF \_ ENVLP \_ Begin \_ NEUTRALVAL.</span><span class="sxs-lookup"><span data-stu-id="4507f-125">MPF\_ENVLP\_BEGIN\_NEUTRALVAL.</span></span> <span data-ttu-id="4507f-126">DMO utilise la valeur neutre du paramètre comme valeur de départ du segment.</span><span class="sxs-lookup"><span data-stu-id="4507f-126">The DMO uses the neutral value of the parameter as the starting value for the segment.</span></span> <span data-ttu-id="4507f-127">Elle ignore **valStart**.</span><span class="sxs-lookup"><span data-stu-id="4507f-127">It ignores **valStart**.</span></span>

<span data-ttu-id="4507f-128">Vous pouvez considérer ces indicateurs comme saisissant le point de départ du segment et le déplacer vers le haut ou vers le haut, tandis que la valeur de fin reste fixe.</span><span class="sxs-lookup"><span data-stu-id="4507f-128">You can think of these flags as grabbing the starting point of the segment and moving it up or down, while the ending value remains fixed.</span></span> <span data-ttu-id="4507f-129">Le segment est « stretch » en conséquence.</span><span class="sxs-lookup"><span data-stu-id="4507f-129">The segment will "stretch" accordingly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4507f-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4507f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4507f-131">Paramètres de média</span><span class="sxs-lookup"><span data-stu-id="4507f-131">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



