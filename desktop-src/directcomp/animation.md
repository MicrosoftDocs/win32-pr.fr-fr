---
title: Animation (DirectComposition)
description: Cette rubrique décrit les principes fondamentaux de l’animation Microsoft DirectComposition.
ms.assetid: 65DA3971-97C0-4B59-BC67-287AAEAAE340
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f7462a10fd83b45c1b90450fdde806ef306a2f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922091"
---
# <a name="animation-directcomposition"></a>Animation (DirectComposition)

> [!NOTE]
> pour les applications sur Windows 10, nous vous recommandons d’utiliser des api Windows. UI. Composition au lieu de DirectComposition. Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).

Cette rubrique décrit les principes fondamentaux de l’animation Microsoft DirectComposition. Elle contient les rubriques suivantes :

-   [Qu’est-ce qu’une animation ?](#what-is-an-animation)
-   [Propriétés qui peuvent être animées](#properties-that-can-be-animated)
-   [Fonctions d’animation](#animation-functions)
-   [Segments d’animation](#animation-segments)
    -   [Segment cubique](#cubic-segment)
    -   [Segment sinusoïdal](#sinusoidal-segment)
    -   [Répéter le segment](#repeat-segment)
    -   [Segment de fin](#end-segment)
-   [compatibilité avec Windows gestionnaire d’animations](#compatibility-with-windows-animation-manager)
-   [Rubriques connexes](#related-topics)

## <a name="what-is-an-animation"></a>Qu’est-ce qu’une animation ?

L' *animation* est une illusion optique créée en apportant rapidement des modifications incrémentielles à un visuel pendant une période de temps, tout en redessinant le visuel après chaque modification. Étant donné que les redessins se produisent rapidement, le cerveau perçoit les modifications incrémentielles sous la forme d’une seule scène changeante, tout comme dans un film ou une vidéo d’action en direct.

Le tableau suivant décrit quelques-unes des façons classiques d’utiliser l’animation.

| Animation                 | Description                                                                                                                                                                                                                                          |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Défilement                 | Utilisez l’animation pour ajouter des fonctionnalités telles que le dynamisme d’émulation physique à un contrôle de liste de défilement.                                                                                                                                                           |
| Transitions de scènes         | Utilisez l’animation pour créer des transitions de scène de navigation qui assurent la continuité entre les tâches d’un Workflow. Les transitions de scène de navigation fournissent un contexte qui montre à l’utilisateur où ils se trouvent, où ils se trouvent et où ils doivent aller à la suite. |
| Interactions entre les fenêtres | Animez des éléments d’interface utilisateur d’applications différentes d’une manière qui donne la perception d’une continuité transparente entre elles pour aider l’utilisateur à effectuer des tâches qui impliquent le basculement d’une application à une autre.                                         |



 

## <a name="properties-that-can-be-animated"></a>Propriétés qui peuvent être animées

Dans DirectComposition, vous animez un visuel en appliquant une animation à des propriétés individuelles des objets qui définissent l’objet visuel. Par exemple, si vous souhaitez déplacer un visuel horizontalement sur l’écran, vous devez appliquer une animation à la propriété OffsetX de l’visuel. De même, si vous souhaitez effectuer une rotation 2D animée simple d’un visuel, vous devez appliquer une animation à la propriété angle d’un objet de transformation 2D, puis appliquer l’objet de transformation 2D à la propriété transformer du visuel.

DirectComposition vous permet d’appliquer une animation à toute propriété d’objet qui prend une valeur scalaire. Vous pouvez appliquer des animations simultanées à plusieurs propriétés et à plusieurs objets.

DirectComposition exécute les animations sur un thread séparé. Vous pouvez démarrer une animation ou un ensemble d’animations, puis effectuer d’autres tâches sur vos threads d’application, ou même placer les threads en mode veille, tandis que le moteur de composition exécute les animations à la fréquence d’images appropriée.

## <a name="animation-functions"></a>Fonctions d’animation

DirectComposition anime une propriété d’objet en fonction d’une fonction d’animation que vous définissez. Une *fonction d’animation* est une construction qui spécifie le mode de modification de la valeur d’une propriété d’objet sur une période donnée. Par exemple, vous pouvez définir une fonction d’animation qui modifie la valeur d’une propriété de 1 à 360 au cours de 4 secondes. Ensuite, si vous appliquez la fonction d’animation à la propriété angle d’un objet de transformation de rotation 2D, puis appliquez l’objet de transformation à la propriété de transformation d’un visuel, la fonction d’animation fait pivoter l’objet visuel dans un cercle entier pendant 4 secondes.

Une fonction d’animation est représentée par un *objet d’animation* créé par un appel à la méthode [**IDCompositionDevice :: CreateAnimation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation) . Vous créez une fonction d’animation à l’aide des méthodes de l’interface [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) d’un objet d’animation pour ajouter des *segments d’animation*, un à la fois, au tableau qui définit la fonction d’animation. Lorsque vous ajoutez un segment, vous spécifiez un décalage de base zéro qui marque l’heure de début du segment, par rapport au début de la fonction d’animation. Les segments d’animation doivent être ajoutés dans l’ordre de plus en plus élevé des heures de début. Toute tentative d’ajout d’un segment d’animation dont l’heure de début est antérieure ou égale à un segment précédent échoue. Une fonction d’animation peut avoir une heure de fin spécifiée, indiquant à quel moment la fonction doit se terminer.

Sauf spécification contraire, une fonction d’animation démarre lorsque le Gestionnaire de fenêtrage (DWM) reçoit la commande pour exécuter l’animation. Chaque segment s’exécute jusqu’à ce que l’heure de début du segment suivant soit atteinte. Toutes les modifications discontinues qui se produisent dans la valeur de la propriété animée entre les segments sont considérées comme des modifications discrètes.

Vous appliquez une fonction d’animation à une propriété en affectant à la valeur de propriété le pointeur [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) de l’objet d’animation qui représente la fonction d’animation. Le même objet d’animation peut être appliqué à plusieurs propriétés du même objet, ainsi qu’aux propriétés d’autres objets créés par le même appareil.

## <a name="animation-segments"></a>Segments d’animation

Les segments d’animation sont les définitions de minuterie fondamentales d’une fonction d’animation. Il s’agit des primitives à partir desquelles les fonctions d’animation plus complexes et de niveau supérieur sont générées. Un segment d’animation est construit à partir d’une série de paramètres qui décrivent la fonction et l’heure à laquelle le segment commence, par rapport au début de la fonction d’animation. Pour chaque segment, le temps (*t*) progresse le long de l’axe horizontal et commence à *t* = 0.

### <a name="cubic-segment"></a>Segment cubique

La synchronisation d’un segment cubique est définie par un polynôme cubique. Pour une entrée de temps donnée (*t*), la valeur de sortie est donnée par l’équation suivante :

*x*(*t*) = *à*³ + *BT*² + *CT*  +  *d*

Le diagramme suivant montre une fonction d’animation qui contient deux segments cubiques. Le premier segment passe d’une valeur comprise entre 0 et 16 sur 4 secondes, et la seconde modifie la valeur de façon linéaire de 16 à 0 au cours des 4 secondes suivantes. La première transition se produit le long de ce polynôme cubique :

*x*(*t*) = *t*³-6 *t*² + 12 *t*

et la deuxième transition se produit le long de celle-ci :

*x*(*t*) =-4 *t* + 16

![diagramme d’une fonction d’animation avec deux segments cubiques](images/cubicsegment.png)

Vous ajoutez un segment cubique à une fonction d’animation à l’aide de la méthode [**IDCompositionAnimation :: AddCubic**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addcubic) .

### <a name="sinusoidal-segment"></a>Segment sinusoïdal

La synchronisation d’un segment sinusoïdal est définie par l’équation suivante :

*x*(*t*) = *écart*  +  *amplitude* \* Sin (*t* \* *Frequency* \* 2 \* pi + *phase* \* PI/180.0)

Vous ajoutez un segment sinusoïdal à une fonction d’animation à l’aide de la méthode [**IDCompositionAnimation :: AddSinusoidal**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addsinusoidal) .

### <a name="repeat-segment"></a>Répéter le segment

Un segment repeat répète une partie précédente spécifiée d’une fonction d’animation. Un segment REPEAT fait en sorte que la partie spécifiée de la fonction d’animation boucle indéfiniment jusqu’à ce que le segment suivant soit rencontré ou que la terminaison spécifiée de l’animation soit atteinte. La partie précédente d’une animation est constituée d’autres segments, y compris d’autres segments de répétition. Un segment REPEAT ne peut pas être utilisé en tant que premier segment dans une fonction d’animation.

Le diagramme suivant montre une fonction d’animation qui comprend deux segments cubiques d’une durée de 4 secondes chacune, suivis d’un segment de répétition qui dure 12 secondes. Le segment REPEAT commence 8 secondes dans l’animation et répète les 6 secondes précédentes de l’animation deux fois jusqu’à ce que le segment de fin soit atteint à 20 secondes.

![diagramme d’une fonction d’animation qui contient deux segments cubiques et un segment de répétition](images/repeatsegment.png)

Pour ajouter un segment REPEAT à une fonction d’animation, utilisez la méthode [**IDCompositionAnimation :: AddRepeat**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addrepeat) .

### <a name="end-segment"></a>Segment de fin

Après avoir construit une fonction d’animation à partir de segments, vous pouvez ajouter un segment de fin pour faire en sorte que la fonction d’animation se termine à un moment donné. Si vous n’ajoutez pas de segment de fin, le dernier segment de la fonction d’animation s’exécute indéfiniment.

Vous ajoutez un segment de fin en appelant la méthode [**IDCompositionAnimation :: end**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end) , en spécifiant un offset à partir du début de la fonction d’animation qui indique le point de terminaison de la fonction. Le décalage doit être supérieur au décalage de début du segment précédent. En outre, un segment de fin ne peut pas être utilisé comme première primitive dans une fonction d’animation.

Lorsque vous appelez [**end**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end), vous spécifiez également une valeur finale pour la propriété animée. La propriété est définie sur la valeur finale spécifiée au moment où le point de terminaison de la fonction d’animation est atteint.

Après avoir ajouté un segment de fin, vous ne pouvez pas ajouter d’autres segments à la fonction d’animation. Autrement dit, tous les appels de méthode sur l’objet d’animation échouent sauf [**IDCompositionAnimation :: Reset**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-reset). L’appel de **Reset** retourne l’objet d’animation à l’État Clean dans lequel la fonction d’animation ne contient aucun segment. à partir de là, vous pouvez ajouter de nouveau des segments.

## <a name="compatibility-with-windows-animation-manager"></a>compatibilité avec Windows gestionnaire d’animations

Windows le gestionnaire d’animations (animation Windows) génère des primitives d’animation dans un format compatible avec l’API DirectComposition. cela signifie que DirectComposition peut créer des animations basées sur des primitives d’animation créées par Windows animation.

pour plus d’informations, consultez [Windows le gestionnaire d’animations](/windows/desktop/UIAnimation/-main-portal), la méthode [**IUIAnimationVariable2 :: GetCurve**](/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getcurve) et [Managing DirectComposition animation with Windows animation manager v2](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 
