---
title: Rendu de texte avec Direct2D et DirectWrite
description: Contrairement à d’autres API, telles que GDI, GDI+ ou WPF, Direct2D interagit avec une autre API, DirectWrite, pour manipuler et restituer le texte. Cette rubrique décrit les avantages et l’interopérabilité de ces composants distincts.
ms.assetid: 1d5b8deb-34e2-433c-8de3-4ef66fb4e49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c49a8f341377bcf78a9a99699a3bd4852411dd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104564779"
---
# <a name="text-rendering-with-direct2d-and-directwrite"></a>Rendu de texte avec Direct2D et DirectWrite

Contrairement à d’autres API, telles que [GDI](/windows/desktop/gdi/windows-gdi), GDI+ ou WPF, [Direct2D](./direct2d-portal.md) interagit avec une autre API, [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), pour manipuler et restituer le texte. Cette rubrique décrit les avantages et l’interopérabilité de ces composants distincts.

Cette rubrique contient les sections suivantes.

-   [Direct2D permet l’adoption incrémentielle](#direct2d-enables-incremental-adoption)
-   [Services de texte et rendu de texte](#text-services-versus-text-rendering)
-   [Glyphes et texte](#glyphs-versus-text)
-   [DirectWrite et Direct2D](#directwrite-and-direct2d)
    -   [DrawText](#drawtextlayout)
    -   [DrawTextLayout](#drawtextlayout)
    -   [DrawGlyphRun](#drawglyphrun)
-   [Rendu de glyphe](#glyph-rendering)
-   [Conclusion](#conclusion)

## <a name="direct2d-enables-incremental-adoption"></a>Direct2D permet l’adoption incrémentielle

Le déplacement d’une application d’une API Graphics vers une autre peut être difficile ou pas ce que vous souhaitez pour diverses raisons. Cela peut être dû au fait que vous devez prendre en charge les plug-ins qui utilisent toujours les interfaces plus anciennes, car l’application elle-même est trop volumineuse pour porter vers une nouvelle API dans une version ou parce qu’une partie de l’API plus récente est souhaitable mais que l’ancienne API fonctionne correctement pour d’autres parties de l’application.

Étant donné que [Direct2D](./direct2d-portal.md) et [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) sont implémentés en tant que composants distincts, vous pouvez mettre à niveau l’ensemble du système graphique 2D ou uniquement la partie texte de celui-ci. Par exemple, vous pouvez mettre à jour une application pour qu’elle utilise DirectWrite pour le texte tout en continuant à utiliser [GDI](/windows/desktop/gdi/windows-gdi) ou GDI+ pour le rendu.

## <a name="text-services-versus-text-rendering"></a>Services de texte et rendu de texte

À mesure que les applications ont évolué, leurs exigences en matière de traitement du texte ont augmenté de plus en plus complexe. À première vue, le texte était généralement confiné à l’interface utilisateur disposée statiquement, et le texte était rendu dans une zone bien définie, telle qu’un bouton. À mesure que les applications commençaient à être disponibles dans un nombre croissant de langages, cette approche est devenue plus difficile à supporter, car la largeur et la hauteur du texte traduit peuvent varier considérablement d’un langage à l’autre. Pour s’adapter, les applications ont commencé à disposer de manière dynamique de leur interface utilisateur pour dépendre de la taille de rendu réelle du texte, plutôt que de l’inverse.

Pour aider les applications à effectuer cette tâche, [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) fournit l’interface [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) . Cette API permet à une application de spécifier une partie de texte avec des caractéristiques complexes, telles que des polices et des tailles de police différentes, des soulignements, des strikethroughs, du texte bidirectionnel, des effets, des points de suspension et même des caractères non-glyphes incorporés (tels qu’une émoticône bitmap ou une icône). L’application peut ensuite modifier différentes caractéristiques du texte, car il détermine de manière itérative sa disposition d’interface utilisateur. L' [exemple de Hello World DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples), qui est présenté dans l’illustration suivante et dans la rubrique [Didacticiel : prise en main avec DirectWrite](/windows/desktop/DirectWrite/getting-started-with-directwrite) , présente un grand nombre de ces effets.

![capture d’écran de l’exemple « Hello World ».](images/dwrite-hello-world.png)

La disposition peut positionner les glyphes idéalement en fonction de leurs largeurs (comme le fait WPF), ou il peut aligner les glyphes sur les positions de pixel les plus proches (comme le fait [GDI](/windows/desktop/gdi/windows-gdi) ).

En plus d’obtenir des mesures de texte, l’application peut effectuer un test de positionnement dans différentes parties du texte. Par exemple, il peut être utile de savoir qu’un clic a été effectué sur un lien hypertexte dans le texte. (Pour plus d’informations sur le test de positionnement, consultez la rubrique [Comment effectuer un test de positionnement sur une disposition de texte](/windows/desktop/DirectWrite/how-to-perform-hit-testing-on-a-text-layout) .)

L’interface de disposition du texte est dissociée de l’API de rendu utilisée par l’application, comme le montre le diagramme suivant :

![diagramme de disposition du texte et de l’API graphique.](images/direct2d-directwrite1.png)

Cette séparation est possible car DirectWrite fournit une interface de rendu ([**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer)) que les applications peuvent implémenter pour afficher du texte à l’aide de l’API graphique de votre choix. L’application implémentée [**IDWriteTextRenderer ::D rawglyphrun**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) méthode de rappel est appelée par DirectWrite lors du rendu d’une disposition de texte. Il incombe à cette méthode d’effectuer les opérations de dessin ou de les passer.

Pour dessiner des glyphes, [Direct2D](./direct2d-portal.md) fournit [**ID2D1RenderTarget ::D rawglyphrun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) pour le dessin sur une surface Direct2D et [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) fournit [**IDWriteBitmapRenderTarget ::D RAWGLYPHRUN**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) pour le dessin sur une surface GDI qui peut ensuite être transférée à une fenêtre à l’aide de GDI. En pratique, les **DrawGlyphRun** dans Direct2D et DirectWrite ont des paramètres compatibles avec la méthode [**DrawGlyphRun**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) que l’application implémente sur [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer).

À la suite d’une séparation similaire, les fonctionnalités spécifiques au texte (telles que l’énumération et la gestion des polices, l’analyse des glyphes, etc.) sont gérées par [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) au lieu de [Direct2D](./direct2d-portal.md). Les objets DirectWrite sont acceptés directement par Direct2D. Pour aider les applications GDI existantes à tirer parti de DirectWrite, il fournit l’interface de méthode [**IDWriteGdiInterop**](/windows/desktop/api/dwrite/nn-dwrite-idwritegdiinterop) avec des méthodes pour effectuer les opérations suivantes :

-   Créez une police [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) à partir d’une police logique [GDI](/windows/desktop/gdi/windows-gdi) ([**CreateFontFromLOGFONT**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)).
-   Conversion d’un type de police [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) en une police logique [GDI](/windows/desktop/gdi/windows-gdi) ([**ConvertFontFaceToLOGFONT**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)).
-   Récupérez le type de police [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) à partir de celui qui est sélectionné dans un HDC. ([**CreateFontFaceFromHdc**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc))
-   Créez une [](/windows/desktop/DirectWrite/direct-write-portal) [**cible de rendu de bitmap**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) DirectWrite dans la mémoire système ([**CreateBitmapRenderTarget**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget)).

## <a name="glyphs-versus-text"></a>Glyphes et texte

Le texte est un ensemble de points de code Unicode (caractères), avec différents modificateurs stylistiques (polices, poids, soulignements, strikethroughs, etc.) disposés dans un rectangle. Un glyphe, en revanche, est un index particulier dans un fichier de police particulier. Un glyphe définit un ensemble de courbes qui peuvent être rendues, mais il n’a aucune signification textuelle. Il peut y avoir un mappage plusieurs-à-plusieurs entre des glyphes et des caractères. Une séquence de glyphes qui proviennent du même type de police et qui sont disposés de façon séquentielle sur une ligne de base est appelée [GlyphRun](/windows/desktop/DirectWrite/glyphs-and-glyph-runs). [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) et [DIRECT2D](./direct2d-portal.md) appellent leurs API de rendu de glyphes les plus précises [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) et leurs signatures sont très similaires. Les éléments suivants proviennent de [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) dans Direct2D :


```
STDMETHOD_(void, DrawGlyphRun)(
        D2D1_POINT_2F baselineOrigin,
        __in CONST DWRITE_GLYPH_RUN *glyphRun,
        __in ID2D1Brush *foregroundBrush,
        DWRITE_MEASURING_MODE measuringMode = DWRITE_MEASURING_MODE_NATURAL 
        ) PURE;
```



Et cette méthode provient de [**IDWriteBitmapRenderTarget**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) dans [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal):


```
STDMETHOD(DrawGlyphRun)(
        FLOAT baselineOriginX,
        FLOAT baselineOriginY,
        DWRITE_MEASURING_MODE measuringMode,
        __in DWRITE_GLYPH_RUN const* glyphRun,
        IDWriteRenderingParams* renderingParams,
        COLORREF textColor,
        __out_opt RECT* blackBoxRect = NULL
        ) PURE;
```



La version [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) conserve l’origine de la ligne de base, le mode de mesure et les paramètres d’exécution du glyphe et comprend des paramètres supplémentaires.

[DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) vous permet également d’utiliser un convertisseur personnalisé pour les glyphes en implémentant l’interface [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) . Cette interface a également une méthode **DrawGlyphRun** , comme le montre l’exemple de code suivant.


```
STDMETHOD(DrawGlyphRun)(
        __maybenull void* clientDrawingContext,
        FLOAT baselineOriginX,
        FLOAT baselineOriginY,
        DWRITE_MEASURING_MODE measuringMode,
        __in DWRITE_GLYPH_RUN const* glyphRun,
        __in DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription,
        __maybenull IUnknown* clientDrawingEffect
        ) PURE;
```



Cette version comprend davantage de paramètres qui sont utiles quand vous implémentez un [convertisseur de texte personnalisé](/windows/desktop/DirectWrite/how-to-implement-a-custom-text-renderer). Le paramètre final est utilisé pour les effets de dessin personnalisés implémentés par l’application. (Pour plus d’informations sur les effets de dessin client, consultez [comment ajouter des effets de dessin client à une disposition de texte](/windows/desktop/DirectWrite/how-to-add-custom-drawing-efffects-to-a-text-layout).

Chaque exécution de glyphe commence à une origine et est placée sur une ligne à partir de cette origine. Les glyphes sont modifiés par la transformation universelle active et les paramètres de rendu de texte sélectionnés sur la cible de rendu associée. Cette API est généralement appelée directement uniquement par les applications qui ont leur propre disposition (par exemple, un traitement de texte) ou par une application qui a implémenté l’interface [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) .

## <a name="directwrite-and-direct2d"></a>DirectWrite et Direct2D

[Direct2D](./direct2d-portal.md) fournit des services de rendu de niveau glyphe par le biais de [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun). Toutefois, cela nécessite que l’application implémente les détails du rendu, ce qui reproduit fondamentalement les fonctionnalités de l’API [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) de GDI.

Par conséquent, [Direct2D](./direct2d-portal.md) fournit des API qui acceptent du texte au lieu de glyphes : [**ID2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) et [**ID2D1RenderTarget ::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)). Les deux méthodes sont rendues sur une surface Direct2D. Pour effectuer un rendu sur une surface GDI, [**IDWriteBitmapRenderTarget ::D rawglyphrun**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) est fourni. Toutefois, cette méthode requiert l’implémentation d’un convertisseur de texte personnalisé par l’application. (Pour plus d’informations, consultez la rubrique [rendu dans une surface GDI](/windows/desktop/DirectWrite/render-to-a-gdi-surface) .)

L’utilisation d’une application de texte commence généralement par simple : put **OK** ou **Cancel** sur un bouton de disposition fixe, par exemple. Toutefois, au fil du temps, il devient plus complexe en tant qu’internationalisation et d’autres fonctionnalités sont ajoutées. Finalement, de nombreuses applications devront utiliser les objets de mise en page [de texte de DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) et implémenter le convertisseur de texte.

Par conséquent, [Direct2D](./direct2d-portal.md) fournit des API en couches qui permettent à une application de démarrer simplement et de croître plus sophistiquées sans devoir suivre ou abandonner son code de travail. Un affichage simplifié est illustré dans le diagramme suivant :

![diagramme d’application DirectWrite et Direct2D.](images/direct2d-directwrite2.png)

### <a name="drawtext"></a>DrawText

[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) est le plus simple des API à utiliser. Elle prend une chaîne Unicode, un pinceau de premier plan, un objet de format unique et un rectangle de destination. Elle disposera et effectuera le rendu de la chaîne entière dans le rectangle de disposition, et la décomposera éventuellement. Cela est utile lorsque vous placez un élément de texte simple dans une partie de l’interface utilisateur de disposition fixe.

### <a name="drawtextlayout"></a>DrawTextLayout

En créant un objet [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) , une application peut commencer à mesurer et à réorganiser le texte et d’autres éléments d’interface utilisateur, et à prendre en charge plusieurs polices, styles, soulignements et strikethroughs. [Direct2D](./direct2d-portal.md) fournit l’API [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) qui accepte directement cet objet et restitue le texte à un point donné. (La largeur et la hauteur sont fournies par l’objet Layout). En plus d’implémenter toutes les fonctionnalités de disposition du texte attendues, Direct2D interprète tout objet Effect comme un pinceau et applique ce pinceau à la plage de glyphes sélectionnée. Il appelle également tous les objets Inline. Une application peut ensuite insérer des caractères non-glyphes (icônes) dans le texte si elle le souhaite. Un autre avantage de l’utilisation d’un objet de disposition de texte est que les positions de glyphe sont mises en cache dans celui-ci. Par conséquent, un gain de performances important est possible en réutilisant le même objet de disposition pour plusieurs appels de dessin et en évitant le recalcul des positions de glyphes pour chaque appel. Cette fonctionnalité n’est pas présente pour la [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))de GDI.

### <a name="drawglyphrun"></a>DrawGlyphRun

Enfin, l’application peut implémenter l’interface [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) elle-même et appeler [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) et [**FILLRECTANGLE**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f_id2d1brush)) , ou toute autre API de rendu. Toute l’interaction existante avec l’objet de mise en page de texte reste inchangée.

Pour obtenir un exemple d’implémentation d’un convertisseur de texte personnalisé, consultez la rubrique [rendu à l’aide d’un convertisseur de texte personnalisé](/windows/desktop/DirectWrite/how-to-implement-a-custom-text-renderer) .

## <a name="glyph-rendering"></a>Rendu de glyphe

L’ajout de [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) à une application GDI existante permet à l’application d’utiliser l’API [**IDWriteBitmapRenderTarget**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) pour afficher les glyphes. La méthode [**IDWriteBitmapRenderTarget ::D rawglyphrun**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) fournie par DirectWrite s’affiche en couleur unie sur un contrôleur de périphérique de mémoire sans nécessiter d’API supplémentaires, telles que [Direct2D](./direct2d-portal.md).

Cela permet à l’application d’obtenir des fonctionnalités de rendu de texte avancées, telles que les suivantes :

-   La fonction ClearType sous-pixel permet à une application de placer des glyphes sur des positions de sous-pixel pour permettre le rendu des glyphes nets et la disposition des glyphes.
-   L’anticrénelage de direction Y permet un rendu plus lisse des courbes sur les glyphes plus grands.

Une application qui se déplace vers [Direct2D](./direct2d-portal.md) obtiendra également les fonctionnalités suivantes :

-   Accélération matérielle.
-   Capacité de remplir du texte à l’aide d’un pinceau [Direct2D](./direct2d-portal.md) arbitraire, tel que les dégradés radiaux, les dégradés linéaires et les bitmaps.
-   Prise en charge supplémentaire de la superposition et du découpage via les API [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)), [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) et [**CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) .
-   La possibilité de prendre en charge le rendu de texte en nuances de gris. Cela remplit correctement le canal alpha de destination en fonction de l’opacité du pinceau de texte et de l’anticrénelage du texte.

Pour prendre en charge efficacement l’accélération matérielle, [Direct2D](./direct2d-portal.md) utilise une approximation légèrement différente de la correction gamma appelée *Correction alpha*. Cela ne requiert pas Direct2D pour inspecter le pixel de couleur de la cible de rendu lors du rendu du texte.

## <a name="conclusion"></a>Conclusion

Cette rubrique explique les différences et similarités entre [Direct2D](./direct2d-portal.md) et [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) et les motivations architecturales pour les fournir comme API coopératives distinctes.

 

 