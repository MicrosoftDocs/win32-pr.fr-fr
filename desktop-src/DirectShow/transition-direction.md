---
description: Sens de la transition
ms.assetid: d18525de-bb75-4c5e-b387-cfec7ba03df7
title: Sens de la transition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d43ec4258d2f23c8b8961e3e1b8fd3d554b057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104552014"
---
# <a name="transition-direction"></a><span data-ttu-id="c7527-103">Sens de la transition</span><span class="sxs-lookup"><span data-stu-id="c7527-103">Transition Direction</span></span>

<span data-ttu-id="c7527-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="c7527-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="c7527-105">Une transition passe de l’entrée A à l’entrée B et de l’heure t ₀ à t ₁.</span><span class="sxs-lookup"><span data-stu-id="c7527-105">A transition goes from input A to input B, and from time t₀ to t₁.</span></span> <span data-ttu-id="c7527-106">Par conséquent, la *direction* d’une transition peut signifier l’un des deux éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c7527-106">Therefore, the *direction* of a transition can mean one of two things:</span></span>

-   <span data-ttu-id="c7527-107">Mappage des couches de la chronologie aux entrées.</span><span class="sxs-lookup"><span data-stu-id="c7527-107">The mapping of timeline layers to inputs.</span></span>
-   <span data-ttu-id="c7527-108">Progression dans le temps.</span><span class="sxs-lookup"><span data-stu-id="c7527-108">The progression over time.</span></span>

<span data-ttu-id="c7527-109">La première est la *direction d’entrée*, tandis que la seconde est la *direction de progression*.</span><span class="sxs-lookup"><span data-stu-id="c7527-109">The first is the *input direction*, and the second is the *progress direction*.</span></span> <span data-ttu-id="c7527-110">Vous pouvez contrôler les deux directions.</span><span class="sxs-lookup"><span data-stu-id="c7527-110">You can control both directions.</span></span>

-   <span data-ttu-id="c7527-111">Direction d’entrée : par défaut, une transition passe de l’composite des couches de faible priorité à la couche qui contient la transition.</span><span class="sxs-lookup"><span data-stu-id="c7527-111">Input direction: By default, a transition goes from the composite of the lower-priority layers to the layer that contains the transition.</span></span> <span data-ttu-id="c7527-112">Pour inverser cette direction, appelez la méthode [**IAMTimelineTrans :: SetSwapInputs**](iamtimelinetrans-setswapinputs.md) .</span><span class="sxs-lookup"><span data-stu-id="c7527-112">To reverse this direction, call the [**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md) method.</span></span>
-   <span data-ttu-id="c7527-113">Direction de la progression : la plupart des transitions prennent en charge une propriété de **progression** standard, qui spécifie le pourcentage de la transition qui est reflété dans la sortie à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="c7527-113">Progress direction: Most transitions support a standard **Progress** property, which specifies what percentage of the transition is reflected in the output at a given moment.</span></span> <span data-ttu-id="c7527-114">Par défaut, la valeur de la propriété **Progress** passe de 0,0 à 1,0 pendant la durée de la transition.</span><span class="sxs-lookup"><span data-stu-id="c7527-114">By default, the value of the **Progress** property goes from 0.0 to 1.0 over the duration of the transition.</span></span> <span data-ttu-id="c7527-115">Pour inverser la progression, affectez à la propriété **Progress** la valeur allant de 1,0 à 0,0.</span><span class="sxs-lookup"><span data-stu-id="c7527-115">To reverse the progress, set the **Progress** property to go from 1.0 to 0.0.</span></span>

<span data-ttu-id="c7527-116">Le diagramme suivant illustre la différence entre la direction d’entrée et la direction de progression.</span><span class="sxs-lookup"><span data-stu-id="c7527-116">The following diagram illustrates the difference between input direction and progress direction.</span></span> <span data-ttu-id="c7527-117">Il présente quatre variations sur une transition de [réinitialisation SMPTE](smpte-wipe-transition.md) standard.</span><span class="sxs-lookup"><span data-stu-id="c7527-117">It shows four variations on a standard [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span>

![instructions de réinitialisation](images/wipedirections.png)

<span data-ttu-id="c7527-119">La transition réside sur la piste 1.</span><span class="sxs-lookup"><span data-stu-id="c7527-119">The transition resides on track 1.</span></span> <span data-ttu-id="c7527-120">Par défaut, la réinitialisation va de gauche à droite et de Track 0 à Track 1.</span><span class="sxs-lookup"><span data-stu-id="c7527-120">By default, the wipe goes from left to right and from track 0 to track 1.</span></span> <span data-ttu-id="c7527-121">Si vous échangez des entrées, la réinitialisation passe de Track 1 pour suivre 0, mais toujours de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="c7527-121">Swapping inputs causes the wipe to go from track 1 to track 0, but still from left to right.</span></span> <span data-ttu-id="c7527-122">L’inversion de la progression fait passer la transition de droite à gauche.</span><span class="sxs-lookup"><span data-stu-id="c7527-122">Reversing the progress makes the transition go from right to left.</span></span> <span data-ttu-id="c7527-123">Vous pouvez combiner les deux, comme indiqué à l’extrême gauche.</span><span class="sxs-lookup"><span data-stu-id="c7527-123">You can combine both, as shown on the far left.</span></span>

<span data-ttu-id="c7527-124">Pour plus d’informations sur l’affichage DES transitions par, consultez [le modèle de chronologie](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="c7527-124">For more information about how DES renders transitions, see [The Timeline Model](the-timeline-model.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7527-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c7527-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7527-126">Utilisation des effets et des transitions</span><span class="sxs-lookup"><span data-stu-id="c7527-126">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



