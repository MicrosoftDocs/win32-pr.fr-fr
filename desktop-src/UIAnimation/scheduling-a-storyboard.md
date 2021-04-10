---
title: Planifier une table de montage séquentiel
description: Une fois la table de montage séquentiel créée, elle est planifiée par le gestionnaire d’animations.
ms.assetid: f3c8fe34-8bca-4421-a390-9e0ba9af27b4
keywords:
- Animations de storyboards Windows, planification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3feae253804d20711c9bbd8ed50895f43272a3f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028651"
---
# <a name="schedule-a-storyboard"></a><span data-ttu-id="152d1-104">Planifier une table de montage séquentiel</span><span class="sxs-lookup"><span data-stu-id="152d1-104">Schedule a Storyboard</span></span>

<span data-ttu-id="152d1-105">Une fois la table de montage séquentiel créée, elle est planifiée par le gestionnaire d’animations.</span><span class="sxs-lookup"><span data-stu-id="152d1-105">After a storyboard is created, it is scheduled by the animation manager.</span></span>

## <a name="overview"></a><span data-ttu-id="152d1-106">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="152d1-106">Overview</span></span>

<span data-ttu-id="152d1-107">Par défaut, chaque Storyboard démarre immédiatement lorsqu’il est planifié.</span><span class="sxs-lookup"><span data-stu-id="152d1-107">By default, each storyboard starts immediately when it is scheduled.</span></span> <span data-ttu-id="152d1-108">Cela signifie que lorsqu’un Storyboard commence à animer une ou plusieurs variables, il peut interrompre les autres storyboards animant ces mêmes variables.</span><span class="sxs-lookup"><span data-stu-id="152d1-108">This means that when a storyboard starts to animate one or more variables, it may interrupt any other storyboards animating those same variables.</span></span> <span data-ttu-id="152d1-109">Toutefois, une application peut spécifier d’autres comportements en déterminant la priorité relative entre les storyboards.</span><span class="sxs-lookup"><span data-stu-id="152d1-109">However, an application may specify other behaviors by determining the relative priority between storyboards.</span></span>

<span data-ttu-id="152d1-110">Une fois qu’une table de montage séquentiel a été planifiée, elle ne peut plus être modifiée.</span><span class="sxs-lookup"><span data-stu-id="152d1-110">After a storyboard has been scheduled, it can no longer be altered.</span></span> <span data-ttu-id="152d1-111">Toutefois, une fois qu’une table de montage séquentiel a été supprimée de la planification, elle peut être planifiée pour une nouvelle lecture.</span><span class="sxs-lookup"><span data-stu-id="152d1-111">However, after a storyboard has been removed from the schedule, it can be scheduled for play again.</span></span> <span data-ttu-id="152d1-112">Les développeurs doivent faire preuve de prudence lors de la réutilisation des storyboards, car cette opération ne doit être effectuée que si le même Storyboard peut devoir être mis en file d’attente en raison d’une action de l’utilisateur lorsqu’il est déjà en cours de création ou en file d’attente dans la planification.</span><span class="sxs-lookup"><span data-stu-id="152d1-112">Developers should exercise caution when re-using storyboards, as this should only be done where there is no chance that the same storyboard might need to be queued due to a user action when it is already playing or queued in the schedule.</span></span>

## <a name="example-code"></a><span data-ttu-id="152d1-113">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="152d1-113">Example Code</span></span>

<span data-ttu-id="152d1-114">L’exemple de code suivant provient de MainWindow. cpp dans l’animation Windows Samples animation [pilotée](application-driven-animation-sample.md) par l’application et [animation pilotée par un minuteur](timer-driven-animation-sample.md).</span><span class="sxs-lookup"><span data-stu-id="152d1-114">The following example code is taken from MainWindow.cpp in the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="152d1-115">Elle utilise la méthode [**IUIAnimationStoryboard :: Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) pour planifier le Storyboard.</span><span class="sxs-lookup"><span data-stu-id="152d1-115">It uses the [**IUIAnimationStoryboard::Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) method to schedule the storyboard.</span></span> <span data-ttu-id="152d1-116">Cette méthode requiert l’heure actuelle en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="152d1-116">This method requires the current time as a parameter.</span></span>


```
// Get the current time and schedule the storyboard for play

UI_ANIMATION_SECONDS secondsNow;
hr = m_pAnimationTimer->GetTime(
    &secondsNow
    );
if (SUCCEEDED(hr))
{
    hr = pStoryboard->Schedule(
        secondsNow
    );
}
```



## <a name="previous-step"></a><span data-ttu-id="152d1-117">Étape précédente</span><span class="sxs-lookup"><span data-stu-id="152d1-117">Previous Step</span></span>

<span data-ttu-id="152d1-118">Avant de commencer cette étape, vous devez avoir terminé cette étape : [créer une table de montage séquentiel et ajouter des transitions](updating---timer-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="152d1-118">Before starting this step, you should have completed this step: [Create a Storyboard and Add Transitions](updating---timer-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="152d1-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="152d1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="152d1-120">**IUIAnimationStoryboard :: Schedule**</span><span class="sxs-lookup"><span data-stu-id="152d1-120">**IUIAnimationStoryboard::Schedule**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule)
</dt> <dt>

[<span data-ttu-id="152d1-121">**IUIAnimationTimer :: GetTime**</span><span class="sxs-lookup"><span data-stu-id="152d1-121">**IUIAnimationTimer::GetTime**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[<span data-ttu-id="152d1-122">Vue d’ensemble du storyboard</span><span class="sxs-lookup"><span data-stu-id="152d1-122">Storyboard Overview</span></span>](storyboard-construction.md)
</dt> </dl>

 

 




