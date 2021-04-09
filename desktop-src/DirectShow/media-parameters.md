---
description: Paramètres de média
ms.assetid: 48b2bc2e-897d-4aa9-8a50-c2855a17dca5
title: Paramètres de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9276a3d38b9176458299bfd1a47057cac6236e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869473"
---
# <a name="media-parameters"></a><span data-ttu-id="43d10-103">Paramètres de média</span><span class="sxs-lookup"><span data-stu-id="43d10-103">Media Parameters</span></span>

<span data-ttu-id="43d10-104">Les paramètres de média permettent à une application de configurer les propriétés d’un objet afin qu’elles évoluent dans le temps d’une manière mathématique déterministe.</span><span class="sxs-lookup"><span data-stu-id="43d10-104">Media parameters enable an application to configure an object's properties so that they change over time in a mathematically deterministic way.</span></span>

<span data-ttu-id="43d10-105">Par exemple, supposons qu’un ingénieur de son mélange une bande maître numérique et souhaite appliquer un léger délai à une section de voix pour remplir le son.</span><span class="sxs-lookup"><span data-stu-id="43d10-105">For example, suppose that a sound engineer is mixing a digital master tape and wants to apply a slight delay to a vocal section, to fill out the sound.</span></span> <span data-ttu-id="43d10-106">L’effet sera transférerez si le retard se découpe brusquement.</span><span class="sxs-lookup"><span data-stu-id="43d10-106">The effect will be jarring if the delay cuts in abruptly.</span></span> <span data-ttu-id="43d10-107">Au lieu de cela, l’effet doit commencer à 100 pour cent (sans délai) et la combinaison humide/sèche doit augmenter graduellement jusqu’à atteindre le niveau souhaité.</span><span class="sxs-lookup"><span data-stu-id="43d10-107">Instead, the effect should begin 100 percent dry (no delay), and the wet/dry mix should increase gradually until it reaches the desired level.</span></span> <span data-ttu-id="43d10-108">En outre, cette transition doit suivre une courbe lisse ou une progression linéaire.</span><span class="sxs-lookup"><span data-stu-id="43d10-108">Moreover, this transition should follow a smooth curve or linear progression.</span></span> <span data-ttu-id="43d10-109">Pour prendre en charge ce scénario, un DMO peut exposer les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="43d10-109">To support this scenario, a DMO can expose the following interfaces:</span></span>

-   <span data-ttu-id="43d10-110">[**IMediaParamInfo**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) contient des méthodes permettant de découvrir des informations sur les propriétés prises en charge.</span><span class="sxs-lookup"><span data-stu-id="43d10-110">[**IMediaParamInfo**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) contains methods for discovering information about the supported properties.</span></span> <span data-ttu-id="43d10-111">En règle générale, le client appellera ces méthodes avant de commencer à diffuser des données en continu.</span><span class="sxs-lookup"><span data-stu-id="43d10-111">Typically, the client will call these methods before it begins to stream data.</span></span>
-   <span data-ttu-id="43d10-112">[**IMediaParams**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) contient des méthodes permettant de définir les courbes qu’un paramètre suivra pendant la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="43d10-112">[**IMediaParams**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) contain methods for setting the curves that a parameter will follow during streaming.</span></span>

<span data-ttu-id="43d10-113">Ces interfaces sont principalement conçues pour DMOs, mais tout objet peut les prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="43d10-113">These interfaces are designed primarily for DMOs, but any object can support them.</span></span> <span data-ttu-id="43d10-114">Dans cette section, le terme *paramètre* fait référence à toute propriété qui prend en charge ces deux interfaces.</span><span class="sxs-lookup"><span data-stu-id="43d10-114">Within this section, the term *parameter* refers to any property that supports these two interfaces.</span></span>

<span data-ttu-id="43d10-115">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="43d10-115">This section contains the following topics:</span></span>

-   [<span data-ttu-id="43d10-116">Courbes de paramètres</span><span class="sxs-lookup"><span data-stu-id="43d10-116">Parameter Curves</span></span>](parameter-curves.md)
-   [<span data-ttu-id="43d10-117">Informations sur les paramètres</span><span class="sxs-lookup"><span data-stu-id="43d10-117">Parameter Information</span></span>](parameter-information.md)
-   [<span data-ttu-id="43d10-118">Segments d’enveloppe</span><span class="sxs-lookup"><span data-stu-id="43d10-118">Envelope Segments</span></span>](envelope-segments.md)
-   [<span data-ttu-id="43d10-119">Calcul des valeurs de paramètre</span><span class="sxs-lookup"><span data-stu-id="43d10-119">Calculating Parameter Values</span></span>](calculating-parameter-values.md)

## <a name="related-topics"></a><span data-ttu-id="43d10-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="43d10-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43d10-121">Objets multimédia DirectX</span><span class="sxs-lookup"><span data-stu-id="43d10-121">DirectX Media Objects</span></span>](directx-media-objects.md)
</dt> </dl>

 

 



