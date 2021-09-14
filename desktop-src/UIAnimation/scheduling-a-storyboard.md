---
title: Planifier une table de montage séquentiel
description: Une fois la table de montage séquentiel créée, elle est planifiée par le gestionnaire d’animations.
ms.assetid: f3c8fe34-8bca-4421-a390-9e0ba9af27b4
keywords:
- storyboards Windows Animation, planification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3feae253804d20711c9bbd8ed50895f43272a3f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193351"
---
# <a name="schedule-a-storyboard"></a>Planifier une table de montage séquentiel

Une fois la table de montage séquentiel créée, elle est planifiée par le gestionnaire d’animations.

## <a name="overview"></a>Vue d’ensemble

Par défaut, chaque Storyboard démarre immédiatement lorsqu’il est planifié. Cela signifie que lorsqu’un Storyboard commence à animer une ou plusieurs variables, il peut interrompre les autres storyboards animant ces mêmes variables. Toutefois, une application peut spécifier d’autres comportements en déterminant la priorité relative entre les storyboards.

Une fois qu’une table de montage séquentiel a été planifiée, elle ne peut plus être modifiée. Toutefois, une fois qu’une table de montage séquentiel a été supprimée de la planification, elle peut être planifiée pour une nouvelle lecture. Les développeurs doivent faire preuve de prudence lors de la réutilisation des storyboards, car cette opération ne doit être effectuée que si le même Storyboard peut devoir être mis en file d’attente en raison d’une action de l’utilisateur lorsqu’il est déjà en cours de création ou en file d’attente dans la planification.

## <a name="example-code"></a>Exemple de code

l’exemple de code suivant est extrait de MainWindow. cpp dans l’Windows animation exemples d’animation [pilotée](application-driven-animation-sample.md) par l’Application et [animation pilotée par un minuteur](timer-driven-animation-sample.md). Elle utilise la méthode [**IUIAnimationStoryboard :: Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) pour planifier le Storyboard. Cette méthode requiert l’heure actuelle en tant que paramètre.


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



## <a name="previous-step"></a>Étape précédente

Avant de commencer cette étape, vous devez avoir terminé cette étape : [créer une table de montage séquentiel et ajouter des transitions](updating---timer-driven-animation.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IUIAnimationStoryboard :: Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule)
</dt> <dt>

[**IUIAnimationTimer :: GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[Vue d’ensemble du storyboard](storyboard-construction.md)
</dt> </dl>

 

 




