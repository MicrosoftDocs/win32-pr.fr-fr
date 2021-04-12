---
description: Aperçu des effets et des transitions
ms.assetid: aa13bd57-69c1-462c-86e3-64026a03bfc4
title: Aperçu des effets et des transitions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25506b7e50fe83c2e4fca7bb4166748ec43d33dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109554"
---
# <a name="previewing-effects-and-transitions"></a><span data-ttu-id="c5845-103">Aperçu des effets et des transitions</span><span class="sxs-lookup"><span data-stu-id="c5845-103">Previewing Effects and Transitions</span></span>

<span data-ttu-id="c5845-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="c5845-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="c5845-105">Le rendu de certains effets et transitions prend beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="c5845-105">Some effects and transitions take a relatively long time to render.</span></span> <span data-ttu-id="c5845-106">Pendant la préversion, la vidéo peut être hachée ou désynchronisée avec l’audio.</span><span class="sxs-lookup"><span data-stu-id="c5845-106">During preview this can cause the video to become choppy or out of sync with the audio.</span></span> <span data-ttu-id="c5845-107">Vous pouvez augmenter la vitesse d’affichage en désactivant les effets ou les transitions :</span><span class="sxs-lookup"><span data-stu-id="c5845-107">You can increase preview speed by disabling effects or transitions:</span></span>

-   <span data-ttu-id="c5845-108">Pour désactiver tous les effets, appelez [**IAMTimeline :: EnableEffects**](iamtimeline-enableeffects.md).</span><span class="sxs-lookup"><span data-stu-id="c5845-108">To disable all effects, call [**IAMTimeline::EnableEffects**](iamtimeline-enableeffects.md).</span></span>
-   <span data-ttu-id="c5845-109">Pour désactiver toutes les transitions, appelez [**IAMTimeline :: EnableTransitions**](iamtimeline-enabletransitions.md).</span><span class="sxs-lookup"><span data-stu-id="c5845-109">To disable all transitions, call [**IAMTimeline::EnableTransitions**](iamtimeline-enabletransitions.md).</span></span>
-   <span data-ttu-id="c5845-110">Pour désactiver une transition particulière, appelez [**IAMTimelineTrans :: SetCutsOnly**](iamtimelinetrans-setcutsonly.md).</span><span class="sxs-lookup"><span data-stu-id="c5845-110">To disable a particular transition, call [**IAMTimelineTrans::SetCutsOnly**](iamtimelinetrans-setcutsonly.md).</span></span>

<span data-ttu-id="c5845-111">Lorsque les effets sont désactivés, ils ne sont pas rendus au cours de la préversion.</span><span class="sxs-lookup"><span data-stu-id="c5845-111">When effects are disabled, they are not rendered during preview.</span></span> <span data-ttu-id="c5845-112">Quand une transition est désactivée, elle est rendue sous la forme d’une coupe de saut.</span><span class="sxs-lookup"><span data-stu-id="c5845-112">When a transition is disabled, it is rendered as a jump cut.</span></span> <span data-ttu-id="c5845-113">Le segue entre les pistes se produit toujours, mais l’effet visuel n’est pas rendu.</span><span class="sxs-lookup"><span data-stu-id="c5845-113">The segue between tracks still occurs, but the visual effect is not rendered.</span></span>

<span data-ttu-id="c5845-114">Si un effet ou une transition ne peut pas être rendu, le moteur de rendu remplace un effet ou une transition par défaut.</span><span class="sxs-lookup"><span data-stu-id="c5845-114">If an effect or transition cannot be rendered, the render engine substitutes a default effect or transition.</span></span> <span data-ttu-id="c5845-115">Appelez la méthode [**IAMTimeline :: SetDefaultEffect**](iamtimeline-setdefaulteffect.md) pour définir l’effet par défaut, et la méthode [**IAMTimeline :: SetDefaultTransition**](iamtimeline-setdefaulttransition.md) pour définir la transition par défaut.</span><span class="sxs-lookup"><span data-stu-id="c5845-115">Call the [**IAMTimeline::SetDefaultEffect**](iamtimeline-setdefaulteffect.md) method to set the default effect, and the [**IAMTimeline::SetDefaultTransition**](iamtimeline-setdefaulttransition.md) method to set the default transition.</span></span> <span data-ttu-id="c5845-116">Si vous ne spécifiez pas de valeur par défaut, ou si celle que vous spécifiez est également à l’origine d’une erreur, l’algorithme DES utilise sa propre valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="c5845-116">If you do not specify a default, or if the one you specify also causes an error, DES uses its own default.</span></span>

> [!Note]  
> <span data-ttu-id="c5845-117">Vous pouvez également améliorer la qualité de l’aperçu en accroissant la quantité de mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="c5845-117">You can also improve preview quality by increasing the amount of frame buffering.</span></span> <span data-ttu-id="c5845-118">Consultez [**IAMTimelineGroup :: SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md).</span><span class="sxs-lookup"><span data-stu-id="c5845-118">See [**IAMTimelineGroup::SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c5845-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c5845-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5845-120">Utilisation des effets et des transitions</span><span class="sxs-lookup"><span data-stu-id="c5845-120">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



