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
# <a name="previewing-effects-and-transitions"></a>Aperçu des effets et des transitions

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Le rendu de certains effets et transitions prend beaucoup de temps. Pendant la préversion, la vidéo peut être hachée ou désynchronisée avec l’audio. Vous pouvez augmenter la vitesse d’affichage en désactivant les effets ou les transitions :

-   Pour désactiver tous les effets, appelez [**IAMTimeline :: EnableEffects**](iamtimeline-enableeffects.md).
-   Pour désactiver toutes les transitions, appelez [**IAMTimeline :: EnableTransitions**](iamtimeline-enabletransitions.md).
-   Pour désactiver une transition particulière, appelez [**IAMTimelineTrans :: SetCutsOnly**](iamtimelinetrans-setcutsonly.md).

Lorsque les effets sont désactivés, ils ne sont pas rendus au cours de la préversion. Quand une transition est désactivée, elle est rendue sous la forme d’une coupe de saut. Le segue entre les pistes se produit toujours, mais l’effet visuel n’est pas rendu.

Si un effet ou une transition ne peut pas être rendu, le moteur de rendu remplace un effet ou une transition par défaut. Appelez la méthode [**IAMTimeline :: SetDefaultEffect**](iamtimeline-setdefaulteffect.md) pour définir l’effet par défaut, et la méthode [**IAMTimeline :: SetDefaultTransition**](iamtimeline-setdefaulttransition.md) pour définir la transition par défaut. Si vous ne spécifiez pas de valeur par défaut, ou si celle que vous spécifiez est également à l’origine d’une erreur, l’algorithme DES utilise sa propre valeur par défaut.

> [!Note]  
> Vous pouvez également améliorer la qualité de l’aperçu en accroissant la quantité de mémoire tampon de trame. Consultez [**IAMTimelineGroup :: SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des effets et des transitions](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



