---
description: Transitions
ms.assetid: 432db77f-c3fa-4234-bbce-cf17d8878b99
title: Transitions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01fef1cd888293ad83ab1ba9f05ab4bb83ddafa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868262"
---
# <a name="transitions"></a><span data-ttu-id="958ef-103">Transitions</span><span class="sxs-lookup"><span data-stu-id="958ef-103">Transitions</span></span>

<span data-ttu-id="958ef-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="958ef-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="958ef-105">Une transition est un moyen de Segue d’une piste vidéo à une autre, à l’aide d’un effet visuel tel qu’un fondu ou une réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="958ef-105">A transition is a way to segue from one video track to another, using a visual effect such as a fade or a wipe.</span></span> <span data-ttu-id="958ef-106">L’illustration suivante montre une chronologie avec une transition :</span><span class="sxs-lookup"><span data-stu-id="958ef-106">The following illustration shows a timeline with a transition:</span></span>

![chronologie avec transition](images/timeline3.png)

<span data-ttu-id="958ef-108">L’objet de transition est sur Track 1 et représente une transition de Track 0 à Track 1.</span><span class="sxs-lookup"><span data-stu-id="958ef-108">The transition object is on track 1, and it represents a transition from track 0 to track 1.</span></span> <span data-ttu-id="958ef-109">Au début de la transition, la vidéo rendue est entièrement à partir de Track 0 (source A).</span><span class="sxs-lookup"><span data-stu-id="958ef-109">At the start of the transition, the rendered video is entirely from Track 0 (source A).</span></span> <span data-ttu-id="958ef-110">À la fin, la vidéo provient entièrement de Track 1 (source C).</span><span class="sxs-lookup"><span data-stu-id="958ef-110">At the end, the video is entirely from Track 1 (source C).</span></span> <span data-ttu-id="958ef-111">Dans between, la sortie passe de la source A à la source C. Par exemple, dans une transition de fondu, une source apparaît progressivement en fondu.</span><span class="sxs-lookup"><span data-stu-id="958ef-111">In between, the output transitions from source A to source C. For example, in a fade transition, one source progressively fades to the other.</span></span> <span data-ttu-id="958ef-112">La sortie finale est schématisés dans la partie inférieure de l’illustration.</span><span class="sxs-lookup"><span data-stu-id="958ef-112">The final output is schematized along the bottom of the illustration.</span></span>

<span data-ttu-id="958ef-113">Les transitions ne peuvent pas se chevaucher dans le temps d’une même piste, mais vous pouvez créer des transitions qui se chevauchent à l’aide de l’objet composition, comme décrit dans [composition et structuration en couches](composition-and-layering.md).</span><span class="sxs-lookup"><span data-stu-id="958ef-113">Transitions cannot overlap in time within the same track, but you can create overlapping transitions by using the composition object, as described in [Composition and Layering](composition-and-layering.md).</span></span>

<span data-ttu-id="958ef-114">Une transition a une direction.</span><span class="sxs-lookup"><span data-stu-id="958ef-114">A transition has a direction.</span></span> <span data-ttu-id="958ef-115">Par défaut, il démarre à partir de la piste de priorité la plus basse (source A, dans l’exemple précédent) et se termine à la piste de priorité la plus élevée (source C).</span><span class="sxs-lookup"><span data-stu-id="958ef-115">By default, it starts from the lower priority track (source A, in the previous example.) and ends at the higher-priority track (source C).</span></span> <span data-ttu-id="958ef-116">Entre-présent, la vidéo est un mélange des deux sources.</span><span class="sxs-lookup"><span data-stu-id="958ef-116">In between, the video is a mixture of the two sources.</span></span> <span data-ttu-id="958ef-117">Toutefois, vous pouvez spécifier le comportement opposé, comme indiqué dans l’illustration suivante :</span><span class="sxs-lookup"><span data-stu-id="958ef-117">However, you can specify the opposite behavior, as shown in the following illustration:</span></span>

![nTrack avec deux transitions](images/fade.png)

<span data-ttu-id="958ef-119">Ici, la première transition disparaît de la piste 0 atténue la piste 1, qui est le comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="958ef-119">Here, the first transition fades from track 0 fades track 1, which is the default behavior.</span></span> <span data-ttu-id="958ef-120">La deuxième transition disparaît de la piste 1 vers la piste 0.</span><span class="sxs-lookup"><span data-stu-id="958ef-120">The second transition fades from track 1 back to Track 0.</span></span> <span data-ttu-id="958ef-121">Notez que les deux transitions se trouvent sur Track 1.</span><span class="sxs-lookup"><span data-stu-id="958ef-121">Note that both transitions are located on track 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="958ef-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="958ef-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="958ef-123">Prise en main avec les services d’édition DirectShow</span><span class="sxs-lookup"><span data-stu-id="958ef-123">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[<span data-ttu-id="958ef-124">Transitions et effets</span><span class="sxs-lookup"><span data-stu-id="958ef-124">Transitions and Effects</span></span>](transitions-and-effects.md)
</dt> <dt>

[<span data-ttu-id="958ef-125">Utilisation des effets et des transitions</span><span class="sxs-lookup"><span data-stu-id="958ef-125">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



