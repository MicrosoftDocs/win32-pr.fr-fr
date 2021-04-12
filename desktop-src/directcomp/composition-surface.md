---
title: Surface de la composition
description: Cette rubrique décrit les types de surfaces pris en charge par Microsoft DirectComposition.
ms.assetid: E19B4F0E-1CFA-4E93-BB6A-BFB701BC72CA
keywords:
- surface de la composition
- Surface logique DirectComposition
- Surface virtuelle DirectComposition
- mise à jour d’une surface logique
- surface logique, mise à jour
- découpage d’une surface virtuelle
- surface virtuelle, découpage
- supprimer la surface virtuelle
- redimensionnement d’une surface virtuelle
- Surace virtuel, redimensionnement
- redimensionner la surface virtuelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4bd30bfbd1de91444b7076184db597cd7a8c82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031417"
---
# <a name="composition-surface"></a>Surface de la composition

> [!NOTE]
> Pour les applications sur Windows 10, nous vous recommandons d’utiliser des API Windows. UI. composition au lieu de DirectComposition. Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).

Cette rubrique décrit les types de surfaces pris en charge par Microsoft DirectComposition.

-   [Surface logique DirectComposition](#directcomposition-logical-surface)
    -   [Mise à jour d’une surface logique](#updating-a-logical-surface)
    -   [Interruption des mises à jour d’une surface logique](#suspending-updates-to-a-logical-surface)
    -   [Reprise des mises à jour sur une surface logique](#resuming-updates-to-a-logical-surface)
    -   [Fin des mises à jour d’une surface logique](#suspending-updates-to-a-logical-surface)
    -   [Exemple d’utilisation d’une surface logique](#example-of-using-a-logical-surface)
-   [Surface virtuelle DirectComposition](#directcomposition-virtual-surface)
    -   [Redimensionnement d’une surface virtuelle](#resizing-a-virtual-surface)
    -   [Découpage d’une surface virtuelle](#trimming-a-virtual-surface)
-   [Rubriques connexes](#related-topics)

## <a name="directcomposition-logical-surface"></a>Surface logique DirectComposition

DirectComposition expose l’objet [**IDCompositionSurface**](/windows/win32/api/dcomp/nn-dcomp-idcompositionsurface) pour représenter une surface de composition logique. DirectComposition expose les API que vous pouvez utiliser pour créer, mettre à jour et supprimer ces surfaces logiques. Chaque surface peut être associée à un ou plusieurs visuels. Une application est responsable de la gestion de la durée de vie des surfaces logiques.

### <a name="updating-a-logical-surface"></a>Mise à jour d’une surface logique

Une application peut mettre à jour une surface logique en appelant [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) et en spécifiant la taille et le décalage du rectangle sur la surface logique que l’application veut mettre à jour. DirectComposition alloue un rectangle de la taille spécifiée, puis retourne la surface et le décalage correspondant que l’application doit dessiner ou mettre à jour. Les limites du rectangle de mise à jour sont liées par la taille de la surface. Par exemple, le rectangle de mise à jour d’une surface de pixels de 40 par 100 peut atteindre (0, 0, 40100). En outre, la région pouvant être mise à jour est appliquée par un rectangle de protection. Étant donné qu’il ne peut y avoir qu’un seul rectangle de protection à la fois, une seule surface logique peut être mise à jour à la fois. **BeginDraw** retourne un code d’erreur si [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) ou [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) n’a pas été appelé après un appel précédent à **BeginDraw**. Une application peut ajouter un appel validé à **BeginDraw** à un lot, mais elle ne prend pas effet tant que **EndDraw** n’est pas appelé et validé.

### <a name="suspending-updates-to-a-logical-surface"></a>Interruption des mises à jour d’une surface logique

Une application qui doit mettre à jour des surfaces différentes peut appeler [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) sur la mise à jour actuelle, puis appeler [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) pour commencer une nouvelle mise à jour. Microsoft DirectComposition autorise plusieurs mises à jour, mais une seule peut être active à la fois. Cela signifie que vous devez appeler **SuspendDraw** ou [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) sur une surface avant d’appeler **BeginDraw** sur la suivante. Contrairement à **EndDraw**, un lot validé peut contenir une surface qui est dans un état **SuspendDraw** , mais ces mises à jour ne s’affichent pas à l’écran tant que **EndDraw** n’est pas appelé.

### <a name="resuming-updates-to-a-logical-surface"></a>Reprise des mises à jour sur une surface logique

Une application peut reprendre une mise à jour d’une surface qui est dans un état [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) en appelant [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw). Cette méthode peut être appelée uniquement sur une surface suspendue.

### <a name="ending-updates-to-a-logical-surface"></a>Fin des mises à jour d’une surface logique

L’appel de [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) et de [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) est le seul moyen d’afficher les modifications de mise à jour bitmap à l’écran. Chaque appel à **EndDraw** doit avoir un appel correspondant à [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) pour supprimer le rectangle de garde. La surface logique conserve toutes les mises à jour jusqu’à ce que la **validation** soit appelée. Vous pouvez également appeler **EndDraw** sur une surface qui se trouve dans l’état [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) , car **EndDraw** est une reprise/fin implicite. Une fois que vous avez appelé **EndDraw**, le contenu mis à jour est présenté à l’écran et ignoré afin que la mémoire pour la mise à jour puisse être réutilisée pour une mise à jour ultérieure.

### <a name="example-of-using-a-logical-surface"></a>Exemple d’utilisation d’une surface logique

L’exemple suivant décrit les étapes qu’une application doit suivre si elle a créé une arborescence d’éléments visuels composée de deux éléments visuels, puis si nécessaire pour mettre à jour des régions spécifiques des deux surfaces logiques associées aux visuels :

1.  Créez un appareil DirectComposition.
2.  Créez l’arborescence d’éléments visuels composée d’un nœud racine et de visuels 1 et 2.
3.  Créez des surfaces logiques 1 et 2.
4.  Appelez [**SetContent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent) pour associer une surface logique aux éléments visuels 1 et 2.
5.  Appelez [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) sur un sous-rectangle de la surface logique 1.
6.  Mettez à jour la surface au décalage retourné par DirectComposition.
7.  Étapes facultatives :
    1.  Appelez [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) sur la surface logique 1.
    2.  Appelez [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) sur le sous-rectangle de la surface logique 2.
    3.  Mettez à jour la surface au décalage retourné par DirectComposition.
    4.  Appelez [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) sur la surface logique 2.
    5.  Appelez [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) sur la surface logique 1.
8.  Mettez à jour la surface au décalage retourné par DirectComposition.
9.  Appelez [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) sur la surface logique 1.
10. Appel de [**validation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit).

## <a name="directcomposition-virtual-surface"></a>Surface virtuelle DirectComposition

DirectComposition expose l’interface [**IDCompositionVirtualSurface**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvirtualsurface) pour représenter une surface virtuelle, qui est une collection de surfaces logiques (vignettes) organisées dans une grille fixe avec des vignettes d’une taille fixe. L’application spécifie la taille de la texture virtuelle au moment de la création. La taille établit les limites de la surface virtuelle. La surface peut être associée à un ou plusieurs visuels.

Lorsqu’une surface virtuelle est initialisée, elle n’est pas sauvegardée par des allocations réelles. En d’autres termes, il ne contient aucun bit. DirectComposition alloue des vignettes (autrement dit, des objets de surface de composition) après que l’application a démarré la mise à jour de l’aire. L’application met à jour la surface virtuelle en appelant [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) et en spécifiant la zone d’intérêt en ce qui concerne les coordonnées de la surface virtuelle. Ensuite, DirectComposition alloue les vignettes nécessaires pour contenir la mise à jour et retourne la surface et le décalage de la composition à mettre à jour.

Comme avec les surfaces logiques, vous pouvez appeler [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) et [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) sur une surface virtuelle. En outre, DirectComposition expose les méthodes que vous pouvez utiliser pour redimensionner et supprimer une surface virtuelle existante.

### <a name="resizing-a-virtual-surface"></a>Redimensionnement d’une surface virtuelle

La méthode [**Resize**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-resize) modifie les limites de la surface virtuelle, ce qui signifie que toutes les nouvelles mises à jour ou allocations doivent se situer dans les limites définies par la nouvelle taille. Une application utilise **redimensionnement** pour indiquer à DirectComposition qu’une région particulière de la surface virtuelle n’est plus nécessaire et peut être récupérée. Si le **redimensionnement** réduit la surface virtuelle, l’application ne peut plus mettre à jour les régions en dehors des nouvelles limites.

L’illustration suivante montre une surface virtuelle 3 par 3 redimensionnée à 2 par 2. La région rouge représente les vignettes qui sont ignorées dans le cadre de l’opération de redimensionnement, et la mémoire est récupérée par DirectComposition. Après le redimensionnement, l’application ne peut pas mettre à jour la région rouge sans redimensionner à nouveau la surface virtuelle.

![redimensionnement d’une surface virtuelle ](images/resize-virtual-surface.png)

L’opération de redimensionnement prend effet immédiatement. DirectComposition n’attend pas que l’application appelle la [**validation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) pour effectuer les mises à jour de redimensionnement. Par exemple, supposons qu’une application effectue la séquence d’appels suivante.


```
pVirtualSurface->Resize(0, 0);
pVirtualSurface->Resize(INT_MAX, INT_MAX);
pDevice->Commit();
```



Dans cet exemple, l’application perd tout le contenu lors du premier redimensionnement. Le deuxième redimensionnement n’a aucun effet bien qu’il ait été appelé avant la [**validation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit). Dans ce cas, rien ne s’affiche à l’écran.

### <a name="trimming-a-virtual-surface"></a>Découpage d’une surface virtuelle

La méthode [**Trim**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-trim) identifie la région de la surface virtuelle dont l’application a besoin. Elle ne redimensionne pas les limites de la surface virtuelle, mais elle indique à DirectComposition les surfaces logiques qui doivent être allouées.

Dans l’illustration suivante, le carré vert est la fenêtre d’affichage de l’application. L’application est initialement rendue aux six premières mosaïques (bleues) de la surface virtuelle (gris clair) qui se trouvent dans la fenêtre d’affichage. Comme la page qui est représentée par la surface virtuelle fait défiler, l’application doit afficher les six dernières vignettes. L’application appelle [**Trim**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-trim) pour indiquer que la région définie par les six dernières vignettes correspond à l’emplacement du contenu et que le reste n’est pas nécessaire pour le moment. DirectComposition peut ensuite choisir de recycler les surfaces logiques qui représentaient à l’origine les six premières vignettes (gris foncé).

![découpage d’une surface virtuelle](images/trim-virtual-surface.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 