---
title: Concepts de base (DirectComposition)
description: Cette rubrique fournit une vue d’ensemble des concepts de base de Microsoft DirectComposition.
ms.assetid: F442BDCA-C913-4438-BFFA-D3F28B68EE85
keywords:
- Concepts DirectComposition
- DirectComposition concepts de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0550dc12cb0dcc5262701658d8e3883ee1ce8d82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922079"
---
# <a name="basic-concepts"></a>Concepts de base

> [!NOTE]
> pour les applications sur Windows 10, nous vous recommandons d’utiliser des api Windows. UI. Composition au lieu de DirectComposition. Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).

Cette rubrique fournit une vue d’ensemble des concepts de base de Microsoft DirectComposition. Il contient les sections suivantes :

-   [Composition](#composition-target-window)
-   [Visuels](#visuals)
    -   [Arborescence d’éléments visuels](#visual-tree)
    -   [Propriétés d’un objet visuel](#properties-of-a-visual-object)
-   [Objet d’appareil](#device-object)
-   [Fenêtre cible de la composition](#composition-target-window)
-   [Composition transactionnelle](#transactional-composition)
    -   [Traitement par lot](#batching)
    -   [Synchronisation](#synchronization)
    -   [Arborescences d’éléments visuels entre appareils](#cross-device-visual-trees)
-   [Rubriques connexes](#related-topics)

## <a name="composition"></a>Composition

DirectComposition définit une *composition* en tant que collection de bitmaps combinés et manipulés en appliquant différentes transformations, effets et animations pour produire un résultat visuel dans une interface utilisateur d’application. DirectComposition fonctionne uniquement avec le contenu de la bitmap. elle ne prend pas en charge les vecteurs ou le texte. DirectComposition ne fournit pas de contenu bitmap. Au lieu de cela, il fournit des interfaces dans lesquelles les utilisateurs peuvent dessiner avec D2D, DXGI ou charger leur propre contenu de texture.

Une application DirectComposition crée deux ensembles d’objets pour composer une scène : les bitmaps qui sont composés ensemble, et les visuels qui définissent les relations spatiales entre les bitmaps. Pour plus d’informations sur les objets bitmap pris en charge par DirectComposition, consultez [objets bitmap](bitmap-surfaces.md).

## <a name="visuals"></a>Visuels

Les éléments *visuels* (ou *objets visuels*) sont les éléments fondamentaux de DirectComposition. Il s’agit des blocs de construction de base que vous utilisez pour créer des compositions et des animations dans l’interface utilisateur de votre application.

En termes de programmation, un visuel est un objet qui a un ensemble de propriétés et expose une interface que vous utilisez pour définir la valeur des propriétés. La propriété de contenu d’un visuel associe une image bitmap particulière au visuel, tandis que d’autres propriétés contrôlent la façon dont DirectComposition positionne et manipule le visuel tel qu’il est affiché à l’écran.

Pour plus d’informations, consultez [propriétés d’un visuel](#properties-of-a-visual-object).

### <a name="visual-tree"></a>Arborescence d’éléments visuels

DirectComposition crée une composition à partir d’une collection hiérarchique d’objets visuels appelée *arborescence* d’éléments visuels. Le visuel à la racine d’une arborescence est appelé le *visuel racine* et peut être associé à un ou plusieurs *visuels enfants* . Un visuel enfant peut avoir un ou plusieurs visuels enfants. Tout visuel associé à des éléments visuels enfants est appelé un *visuel parent*, et tous les visuels enfants qui partagent le même parent sont appelés des *visuels frères*. Un visuel particulier, ainsi que tous ses éléments visuels enfants et descendants, sont appelés *sous-arborescences visuelles*.

L’emplacement d’un visuel dans l’arborescence permet de déterminer la position de l’écran et l’ordre de plan par rapport aux autres éléments visuels de la composition. Le visuel racine est positionné par rapport à l’angle supérieur gauche de la zone cliente de la fenêtre cible où la composition est rendue. Tous les éléments visuels enfants sont positionnés par rapport à l’angle supérieur gauche de leur visuel parent (ou le visuel spécifié par la propriété TransformParent) et apparaissent toujours devant leur parent dans l’ordre de plan.

L’illustration suivante montre une composition d’éléments visuels et la structure de l’arborescence d’éléments visuels utilisée pour produire la composition. Visual 1 est le visuel racine et est également le parent des éléments visuels enfants 2 et 3, qui sont des visuels frères. Visual 3 a ses propres visuels enfants, les éléments visuels 4 et 5. Ensemble, les éléments 3 à 5 composent une sous-arborescence visuelle.

![une composition d’éléments visuels et l’arborescence d’éléments visuels correspondante](images/visuals-and-corresponding-tree.png)

Un visuel parent conserve une liste triée de ses éléments visuels enfants. Lorsque les éléments visuels frères sont positionnés de sorte qu’ils se chevauchent, DirectComposition définit l’ordre de plan des frères en fonction de l’ordre dans lequel ils apparaissent dans la liste des enfants du visuel parent. Un frère qui apparaît plus loin dans la liste est placé devant tous les frères qui apparaissent précédemment dans la liste. L’illustration suivante montre l’ordre de plan des éléments visuels enfants qui se chevauchent.

![ordre de plan des éléments visuels enfants qui se chevauchent](images/overlapping-child-visuals.png)

### <a name="properties-of-a-visual-object"></a>Propriétés d’un objet visuel

Un objet visuel expose un ensemble de propriétés qui vous permettent de définir le contenu de la bitmap pour le visuel et de contrôler la façon dont DirectComposition positionne et manipule le contenu visuel. Les sections suivantes décrivent chaque propriété en détail.

-   [Propriété de contenu](#content-property)
-   [Clip, propriété](#clip-property)
-   [Propriété BorderMode](#bordermode-property)
-   [Propriété BitmapInterpolationMode](#bitmapinterpolationmode-property)
-   [Propriété CompositeMode](#compositemode-property)
-   [OffsetX et propriétés OffsetY](#offsetx-and-offsety-properties)
-   [Propriété Effect](#effect-property)
-   [Transform (propriété)](#transform-property)
-   [Propriété TransformParent](#transformparent-property)

### <a name="content-property"></a>Propriété de contenu

La propriété de contenu d’un visuel spécifie le contenu de la bitmap associée au visuel. Il s’agit de la bitmap que DirectComposition utilise lorsque vous incluez le visuel dans une composition.

Vous définissez la propriété de contenu d’un visuel en appelant la méthode [**IDCompositionVisual :: SetContent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent) .

Pour plus d’informations sur les types de contenu de bitmap pris en charge par DirectComposition, consultez [objets bitmap](bitmap-surfaces.md).

### <a name="clip-property"></a>Clip, propriété

La propriété clip d’un élément visuel spécifie une zone rectangulaire appelée zone de *découpage* (ou *rectangle* de découpage). Quand un visuel est rendu, seule la partie du visuel qui se trouve à l’intérieur de la zone de découpage est affichée, tandis que tout contenu qui s’étend hors de la zone de découpage est coupé (c’est-à-dire, non affiché). DirectComposition prend en charge les régions de découpage qui ont des angles arrondis ou au carré.

Vous définissez la propriété clip d’un élément visuel en appelant la méthode [**IDCompositionVisual :: SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) .

Pour plus d’informations, consultez [découpage](clipping.md).

### <a name="bordermode-property"></a>Propriété BorderMode

La propriété BorderMode spécifie comment composer les bords des bitmaps et des clips associés à cet élément visuel, ou avec des éléments visuels dans la sous-arborescence enracinée dans ce visuel.

Le mode Border affecte la façon dont les bords d’une image bitmap sont composés lorsque la bitmap est transformée de telle sorte que les bords ne sont pas alignés sur l’axe avec les coordonnées entières. Cela affecte également la façon dont le contenu est coupé aux angles d’un élément qui a des angles arrondis, et au bord d’un élément qui est transformé de telle sorte que les bords ne sont pas alignés sur l’axe avec les coordonnées d’entier.

Pour plus d’informations, consultez [**IDCompositionVisual :: SetBorderMode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setbordermode).

### <a name="bitmapinterpolationmode-property"></a>Propriété BitmapInterpolationMode

La propriété BitmapInterpolationMode indique à DirectComposition Comment composer une image bitmap lorsqu’elle est transformée de telle sorte qu’il n’existe pas de correspondance un-à-un entre les pixels de la bitmap et les pixels de l’écran.

Vous définissez la propriété BitmapInterpolationMode d’un visuel en appelant la méthode [**IDCompositionVisual :: SetBitmapInterpolationMode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setbitmapinterpolationmode) .

### <a name="compositemode-property"></a>Propriété CompositeMode

La propriété CompositeMode indique à DirectComposition comment fusionner le contenu bitmap d’un visuel avec la cible de rendu. Pour obtenir une description des modes composites pris en charge, consultez [**\_ \_ mode composite DCOMPOSITION**](/windows/desktop/api/DcompTypes/ne-dcomptypes-dcomposition_composite_mode).

Vous définissez la propriété CompositeMode d’un visuel en appelant la méthode [**IDCompositionVisual :: SetCompositeMode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcompositemode) .

### <a name="offsetx-and-offsety-properties"></a>OffsetX et propriétés OffsetY

Les propriétés OffsetX et OffsetY indiquent à DirectComposition où positionner un visuel horizontalement et verticalement. Ils définissent la position fixe à deux dimensions à partir de laquelle toutes les transformations et tous les effets du visuel sont calculés.

Pour un visuel racine, les propriétés OffsetX et OffsetY définissent la coordonnée x et la coordonnée y d’un point par rapport à l’angle supérieur gauche de la fenêtre qui héberge le visuel. Pour un visuel enfant, les coordonnées sont relatives à l’angle supérieur gauche du parent ou, si la [propriété TransformParent](#transformparent-property) est spécifiée, à l’angle supérieur gauche du visuel spécifié. Quand un visuel est rendu, il est positionné de telle sorte que l’angle supérieur gauche du visuel coïncide avec les coordonnées spécifiées.

Vous définissez les propriétés OffsetX et OffsetY d’un visuel en appelant les méthodes [**IDCompositionVisual :: SetOffsetX**](/previous-versions/windows/desktop/legacy/hh449126(v=vs.85)) et [**SetOffsetY**](/previous-versions/windows/desktop/legacy/hh449131(v=vs.85)) .

### <a name="effect-property"></a>Propriété Effect

La propriété Effect vous permet de spécifier un effet ou un groupe d’effets qui modifiera la façon dont un visuel et sa sous-arborescence sont composés. Par exemple, vous pouvez spécifier des effets qui contrôlent l’opacité d’un visuel, fusionner le visuel avec un autre bitmap de différentes façons et appliquer des transformations de perspective à l’visuel.

Vous définissez la propriété Effect d’un visuel en appelant la méthode [**IDCompositionVisual :: SetEffect**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect) .

Pour plus d’informations, consultez [Effets](effects.md).

### <a name="transform-property"></a>Transform (propriété)

La propriété Transform spécifie une transformation à deux dimensions (2D), ou un groupe de transformations 2D, que DirectComposition doit effectuer sur le visuel. Une transformation (ou transformation) est une opération qui modifie le système de coordonnées d’un visuel par rapport à son parent, ou par rapport au visuel spécifié par la [propriété TransformParent](#transformparent-property). Vous pouvez utiliser les transformations pour modifier la position, la taille ou la nature d’un visuel en le déplaçant vers un autre emplacement (translation), en le rendant plus grand ou plus petit (mise à l’échelle), en le transformant (rotation), en déformant sa forme (inclinaison), et ainsi de suite.

Vous définissez la propriété de transformation d’un visuel en appelant la méthode [**IDCompositionVisual :: setTransform**](/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)) .

Pour plus d’informations, consultez l’article [Transforms (Transformations MSBuild)](transforms.md).

### <a name="transformparent-property"></a>Propriété TransformParent

Le système de coordonnées d’un visuel est modifié par les propriétés OffsetX, OffsetY et Transform. Normalement, ces propriétés définissent le système de coordonnées d’un visuel par rapport à son parent immédiat. Pour utiliser un visuel autre que le parent comme base pour le système de coordonnées d’un visuel enfant, utilisez la propriété TransformParent pour spécifier un visuel différent comme « parent » à des fins de transformation.

Vous définissez la propriété TransformParent d’un visuel en appelant la méthode [**IDCompositionVisual :: SetTransformParent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransformparent) .

## <a name="device-object"></a>Objet d’appareil

Pour utiliser DirectComposition, vous devez créer et manipuler une variété d’objets COM (Component Object Model). Le premier objet que vous devez créer est l' *objet appareil* DirectComposition, car il sert de fabrique pour la création de tous les autres objets utilisés dans une composition.

Vous créez un objet appareil en appelant la fonction [**DCompositionCreateDevice**](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice) , qui retourne un pointeur d’interface [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) . Cette interface expose un ensemble de méthodes que vous utilisez pour créer des objets visuels, des objets clip, des objets d’animation, des objets Transform, des objets Effects, etc.

L’objet appareil a une autre finalité que d’être une fabrique pour la création d’autres objets. Il expose une méthode appelée [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) qui passe une arborescence d’éléments visuels à DirectComposition pour traitement. Pour plus d’informations, consultez [composition transactionnelle](#transactional-composition).

N’oubliez pas que, bien que vous puissiez créer plusieurs instances de l’objet appareil dans votre application, tous les objets que vous utilisez dans une composition particulière doivent être créés par le même objet appareil, à une exception près : vous pouvez combiner des objets visuels de différents objets appareil dans la même arborescence d’éléments visuels. Dans ce cas, DirectComposition traite l’arborescence d’éléments visuels comme il le ferait normalement, sauf que les modifications apportées à un objet visuel particulier dans l’arborescence prennent effet uniquement lorsque la méthode de [**validation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) est appelée sur l’objet appareil qui a créé l’objet visuel.

La possibilité d’utiliser des visuels à partir de différents appareils dans la même arborescence d’éléments visuels permet à plusieurs threads de créer et de manipuler une arborescence d’éléments visuels unique tout en conservant deux appareils indépendants qui peuvent être utilisés pour valider les modifications de manière asynchrone. Pour plus d’informations, consultez [arborescences d’éléments visuels entre appareils](#cross-device-visual-trees).

## <a name="composition-target-window"></a>Fenêtre cible de la composition

Une arborescence d’éléments visuels doit être liée à une fenêtre avant que l’un des visuels de l’arborescence ne puisse être affiché à l’écran. La fenêtre, appelée fenêtre *cible* de la composition, peut être une fenêtre de niveau supérieur ou une fenêtre enfant. En outre, la fenêtre cible de la composition peut être une fenêtre superposée. autrement dit, il peut avoir le style de fenêtre en [**\_ \_ couches WS ex**](/windows/desktop/winmsg/extended-window-styles) .

DirectComposition permet à une application de lier au maximum deux arborescences visuelles à chaque fenêtre. Les arborescences d’éléments visuels incluent une qui est composée en haut de la fenêtre elle-même, mais derrière toutes les fenêtres enfants de la fenêtre, et une autre composée en haut de la fenêtre et en haut des fenêtres enfants. En d’autres termes, chaque fenêtre possède quatre couches conceptuelles, et toutes les couches sont découpées vers la région visible de la fenêtre cible. L’illustration suivante montre les quatre couches conceptuelles d’une fenêtre.

![couches conceptuelles d’une fenêtre](images/directcomposition-layers.png)

## <a name="transactional-composition"></a>Composition transactionnelle

DirectComposition utilise un modèle transactionnel dans lequel vous créez un ensemble de modifications par lot dans un visuel, puis « validez » le jeu à DirectComposition pour le traitement en tout. Vous pouvez modifier le même objet visuel DirectComposition et valider les modifications autant de fois que vous le voulez. Lorsque le Gestionnaire de fenêtrage (DWM) sélectionne des lots, il récupère tous les lots en attente et les applique à l’image suivante dans l’ordre dans lequel ils ont été validés.

Toutes les modifications au sein d’une seule validation sont assurées d’être appliquées à une seule trame. Étant donné que DWM collecte les lots une fois par Frame, vous ne pouvez modifier un objet particulier qu’une seule fois par image. Les validations suivantes qui modifient différents objets peuvent également être appliquées au frame actuel, mais DirectComposition ne garantit pas que les modifications se produiront dans le même frame.

Les méthodes [**IDCompositionSurface :: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) et [**IDCompositionSurface :: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) vous permettent de synchroniser les mises à jour de rendu avec les mises à jour visuelles. Par exemple, vous pouvez appeler **IDCompositionSurface :: BeginDraw**, mettre à jour les OffsetX et les propriétés de clip d’un élément visuel, appeler [**IDCompositionDevice :: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit), dessiner le contenu avec Microsoft DirectX, puis appeler **IDCompositionSurface :: EndDraw**. Dans ce cas, Microsoft DirectComposition garantit que le contenu de la bitmap et les propriétés visuelles sont mis à jour en même temps.

### <a name="batching"></a>Traitement par lot

Vous pouvez valider plusieurs modifications dans le même visuel, ou plusieurs modifications dans différents visuels, au sein du même frame. Lorsque vous apportez plusieurs modifications au même visuel dans le même cadre, gardez les points suivants à l’esprit :

-   Si vous apportez plusieurs modifications à la même propriété d’un visuel, seule la dernière modification est appliquée. Par exemple, si vous définissez l’opacité sur 0, puis sur 0,5 et enfin sur 1,0, seule une opacité de 1,0 est appliquée au visuel.
-   Si vous modifiez plusieurs propriétés du même visuel, DirectComposition applique les modifications d’abord au visuel, puis à tous les visuels enfants. Les propriétés sont appliquées dans l’ordre suivant, quel que soit l’ordre dans lequel vous les spécifiez :

    1.  Offset
    2.  Transformer
    3.  Découper
    4.  Résultat

    L’illustration suivante montre le résultat de l’application de l’ensemble des quatre propriétés à un visuel.

    ![résultat de l’application de l’ensemble des quatre propriétés à un visuel](images/order-of-properties.png)

    N’oubliez pas que toutes les modifications sont appliquées simultanément au visuel dans le contexte du même frame. Cela signifie que, du point de vue de l’utilisateur, les modifications apportées au visuel se produisent instantanément.

-   Pour la propriété Transform, vous pouvez utiliser [**IDCompositionDevice :: CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) pour créer un groupe de transformations à appliquer simultanément à un visuel. DirectComposition applique les transformations dans l’ordre que vous spécifiez.
-   Pour la propriété Effect, vous pouvez utiliser [**IDCompositionEffectGroup**](/windows/win32/api/dcomp/nn-dcomp-idcompositioneffectgroup) pour appliquer un groupe d’effets. DirectComposition applique les effets dans l’ordre que vous spécifiez. En outre, les transformations de perspective 3D entraînent l’aplatissement de l’arborescence d’éléments visuels après que toutes les transformations 3D de l’objet visuel en cours ont été appliquées. Cela permet de s’assurer que le visuel obtenu semble le plus proche possible de la 3D.

### <a name="synchronization"></a>Synchronisation

Votre application peut appeler DirectComposition à partir de plusieurs threads en même temps. L’ordre d’exécution est garanti pour les appels séquentiels, mais pas pour les appels simultanés. Par exemple, si le thread A modifie un visuel et que le thread B valide le lot en même temps, il n’est pas défini si cette modification visuelle est incluse dans le lot validé ou si elle démarre un nouveau lot. En revanche, si votre application utilise d’autres mécanismes de synchronisation pour s’assurer qu’une méthode est appelée avant l’autre, DirectComposition honore l’ordre d’appel et les traite comme si les deux appels étaient émis dans cet ordre à partir d’un thread unique.

### <a name="cross-device-visual-trees"></a>Arborescences d’éléments visuels entre appareils

Les objets DirectComposition ne sont pas liés aux threads ; vous pouvez utiliser plusieurs threads pour modifier le même jeu d’objets. Toutefois, tenez compte des problèmes suivants lors du partage du même objet d’appareil.

-   Les deux threads doivent être en mesure d’appeler [**IDCompositionDevice :: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit). Si un seul des threads appelle **IDCompositionDevice :: Commit**, l’autre thread ne peut pas valider les modifications apportées à DirectComposition.
-   Le comportement transactionnel peut être perdu si un thread appelle [**IDCompositionDevice :: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) alors que l’autre thread effectue encore des modifications destinées à faire partie de la même transaction.

Si vous devez valider plusieurs transactions simultanées dans DirectComposition, vous devez utiliser plusieurs objets d’appareil, éventuellement à partir de plusieurs threads. Dans ce scénario, la même arborescence d’éléments visuels est partagée par les deux objets d’appareil, et chaque objet d’appareil valide ses propres transactions.

L’illustration suivante montre une arborescence d’éléments visuels partagée par deux objets d’appareil. Les éléments visuels 1, 2, 4 et 5 sont détenus par un appareil ou l’autre, mais Visual 3 est partagé par les deux appareils et peut donc être utilisé pour connecter deux sous-arbres dans une arborescence d’éléments visuels unique et plus grande. Le partage de l’arborescence d’éléments visuels permet aux deux appareils d’être manipulés à partir de deux threads différents de manière asynchrone.

![arborescence d’éléments visuels partagée par deux appareils](images/shared-visual-tree-1.png)

Pour illustrer l’utilité du partage d’une arborescence d’éléments visuels entre deux appareils, envisagez une architecture qui permet une entrée tactile à faible latence. L’architecture peut utiliser deux threads, un qui gère la plupart des tâches d’interface utilisateur et un deuxième thread dédié au traitement des événements d’entrée tactile. Le thread tactile met à jour la transformation d’un visuel particulier en fonction du mouvement d’entrée utilisateur. En mettant à jour la transformation, le thread tactile peut rendre l’intégralité de la sous-arborescence sous cet visuel suivre le doigt de l’utilisateur, monter ou baisser en puissance à mesure que l’utilisateur exécute un mouvement tactile multipoint, et ainsi de suite. Le thread d’interface utilisateur conserve la propriété de la majeure partie de l’arborescence de composition, avec le thread tactile qui possède uniquement les éléments visuels marqués pour une réponse tactile asynchrone. L’illustration suivante montre une version simplifiée d’une telle arborescence de composition :

![arborescence d’éléments visuels partagée entre un thread d’interface utilisateur et un thread tactile](images/shared-visual-tree-2.png)

En règle générale, le thread d’interface utilisateur modifie uniquement les visuels qu’il possède exclusivement, et le thread tactile modifie uniquement le visuel partagé. La seule exception se produit lors de la création ou de la destruction d’une sous-arborescence tactile.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IDCompositionSurface :: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)
</dt> <dt>

[**IDCompositionSurface :: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)
</dt> <dt>

[**IDCompositonDevice :: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)
</dt> <dt>

[Concepts DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 