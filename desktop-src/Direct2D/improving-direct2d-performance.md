---
title: Amélioration des performances des applications Direct2D
description: Décrit les techniques d’amélioration des performances de Direct2D.
ms.assetid: e6b02925-4e75-42b0-b0c4-00f1ddb85e46
keywords:
- Direct2D, performances
- Direct2D, bitmaps
- Direct2D, utilisation des ressources
- Direct2D, méthode Flush
- Direct2D, contenu statique
- performances pour Direct2D
- bitmaps pour Direct2D
- Direct2D, interopérabilité GDI
- Direct2D, interopérabilité
- interopérabilité, Direct2D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- interopérabilité, Graphics Device Interface (GDI)
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 5a413b96e00514b64b3cf1b1ee451a84a9e9ff09
ms.sourcegitcommit: 6eb53540b8d882fd035d428567d7d1c5ec17042c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2020
ms.locfileid: "104463887"
---
# <a name="improving-the-performance-of-direct2d-apps"></a>Amélioration des performances des applications Direct2D

Bien que [Direct2D](./direct2d-portal.md) soit accéléré par le matériel et soit conçu pour des performances élevées, vous devez utiliser les fonctionnalités correctement pour maximiser le débit. Les techniques présentées ici sont dérivées de l’étude des scénarios courants et peuvent ne pas s’appliquer à tous les scénarios d’application. Par conséquent, une bonne compréhension du comportement de l’application et des objectifs de performances peut vous aider à obtenir les résultats souhaités.

-   [Utilisation des ressources](#resource-usage)
    -   [Réutiliser les ressources](#reuse-resources)
-   [Limiter l’utilisation du vidage](#restrict-the-use-of-flush)
-   [Images bitmap](#create-large-bitmaps)
    -   [Créer des bitmaps de grande taille](#create-large-bitmaps)
    -   [Créer un Atlas de bitmaps](#create-an-atlas-of-bitmaps)
    -   [Créer des bitmaps partagées](#create-shared-bitmaps)
    -   [Copier des bitmaps](#copying-bitmaps)
-   [Utiliser une image bitmap en mosaïque sur des tirets](#use-tiled-bitmap-over-dashing)
-   [Instructions générales pour le rendu de contenu statique complexe](#general-guidelines-for-rendering-complex-static-content)
    -   [Mise en cache de scène complète à l’aide d’une bitmap de couleur](#full-scene-caching-using-a-color-bitmap)
    -   [Par mise en cache primitive à l’aide d’une bitmap a8 et de la méthode FillOpacityMask](#per-primitive-caching-using-an-a8-bitmap-and-the-fillopacitymask-method)
-   [Mise en cache par primitive utilisant des réalisations géométriques](#per-primitive-caching-using-geometry-realizations)
-   [Rendu de géométrie](#geometry-rendering)
    -   [Utiliser une primitive de dessin spécifique sur la géométrie de dessin](#use-specific-draw-primitive-over-draw-geometry)
    -   [Rendu de Geometry statique](#rendering-static-geometry)
    -   [Utiliser un contexte de périphérique multithread](#use-a-multithreaded-device-context)
-   [Dessiner du texte avec Direct2D](#use-a-multithreaded-device-context)
    -   [DrawTextLayout et DrawText](#drawtextlayout-vs-drawtext)
    -   [Choix du mode de rendu de texte approprié](#choosing-the-right-text-rendering-mode)
    -   [Mise en cache](#full-scene-caching-using-a-color-bitmap)
-   [Découpage d’une forme arbitraire](#clipping-an-arbitrary-shape)
    -   [PushLayer dans Windows 8](#pushlayer-in-windows-8)
    -   [Clips alignés sur l’axe](#axis-aligned-clips)
-   [Interopérabilité des DXGI : Évitez les commutateurs fréquents](#dxgi-interoperability-avoid-frequent-switches)
-   [Connaître le format de pixel](#know-your-pixel-format)
-   [Complexité de la scène](#scene-complexity)
    -   [Comprendre la complexité des scènes](#understand-scene-complexity)
-   [Amélioration des performances pour les applications d’impression Direct2D](#improving-performance-for-direct2d-printing-apps)
    -   [Définir les valeurs de propriété appropriées lorsque vous créez le contrôle d’impression D2D](#set-the-right-property-values-when-you-create-the-d2d-print-control)
    -   [Évitez d’utiliser certains modèles de dessin Direct2D](#avoid-using-certain-direct2d-drawing-patterns)
    -   [Dessiner du texte de manière directe et simple](#draw-text-in-a-direct-and-plain-way)
    -   [Dessiner les bitmaps d’origine lorsque cela est possible](#draw-the-original-bitmaps-when-possible)
-   [Conclusion](#conclusion)

## <a name="resource-usage"></a>Utilisation des ressources

Une ressource est une allocation de quelque nature que ce soit dans la mémoire vidéo ou système. Les bitmaps et les pinceaux sont des exemples de ressources.

Dans Direct2D, les ressources peuvent être créées à la fois dans le logiciel et le matériel. La création et la suppression de ressources sur le matériel sont des opérations coûteuses, car elles nécessitent beaucoup de surcharge pour communiquer avec la carte vidéo. Voyons comment Direct2D rend le contenu dans une cible.

Dans Direct2D, toutes les commandes de rendu sont comprises entre un appel à [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) et un appel à [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw). Ces appels sont effectués sur une cible de rendu. Vous devez appeler la méthode **BeginDraw** avant d’appeler des opérations de rendu. Une fois que vous avez appelé **BeginDraw** , un contexte génère généralement un lot de commandes de rendu, mais retarde le traitement de ces commandes jusqu’à ce que l’une de ces instructions soit vraie :

-   [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) s’est produit. Quand **EndDraw** est appelé, toutes les opérations de dessin par lot sont effectuées et retourne l’état de l’opération.
-   Vous effectuez un appel explicite à [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush): la méthode **flush** provoque le traitement du lot et l’émission de toutes les commandes en attente.
-   La mémoire tampon contenant les commandes de rendu est pleine. Si cette mémoire tampon est saturée avant que les deux conditions précédentes soient remplies, les commandes de rendu sont vidées.

Tant que les primitives n’ont pas été vidées, Direct2D conserve les références internes aux ressources correspondantes, telles que les bitmaps et les pinceaux.

### <a name="reuse-resources"></a>Réutiliser les ressources

Comme mentionné précédemment, la création et la suppression de ressources sont onéreuses sur le matériel. Réutilisez les ressources lorsque cela est possible. Prenons l’exemple de création de bitmaps dans le développement de jeux. En règle générale, les bitmaps qui composent une scène dans un jeu sont tous créés en même temps avec toutes les différentes variations requises pour un rendu de trame à image ultérieur. Au moment du rendu et du rendu de la scène, ces bitmaps sont réutilisés au lieu d’être recréés.

> [!Note]  
> Vous ne pouvez pas réutiliser des ressources pour l’opération de redimensionnement de fenêtre. Quand une fenêtre est redimensionnée, certaines ressources dépendantes de l’échelle, telles que les cibles de rendu compatibles et éventuellement certaines ressources de couche, doivent être recréées, car le contenu de la fenêtre doit être redessiné. Cela peut être important pour maintenir la qualité globale de la scène rendue.

 

## <a name="restrict-the-use-of-flush"></a>Limiter l’utilisation du vidage

Étant donné que la méthode [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) entraîne le traitement des commandes de rendu par lot, nous vous recommandons de ne pas les utiliser. Pour les scénarios les plus courants, laissez la gestion des ressources à Direct2D.

## <a name="bitmaps"></a>Images bitmap

Comme mentionné précédemment, la création et la suppression de ressources sont des opérations très onéreuses dans le matériel. Une image bitmap est un type de ressource qui est souvent utilisé. La création de bitmaps sur la carte vidéo est coûteuse. Leur réutilisation peut aider à rendre l’application plus rapide.

### <a name="create-large-bitmaps"></a>Créer des bitmaps de grande taille

Les cartes vidéo ont généralement une taille d’allocation de mémoire minimale. Si une allocation demandée est inférieure à celle-ci, une ressource de cette taille minimale est allouée et l’excédent de mémoire est perdu et indisponible pour d’autres choses. Si vous avez besoin de plusieurs bitmaps de petite taille, une meilleure technique consiste à allouer une grande bitmap et à stocker tout le contenu de la petite bitmap dans cette grande bitmap. Les sous-zones de la plus grande bitmap peuvent être lues là où les plus petites bitmaps sont nécessaires. Souvent, vous devez inclure le remplissage (pixels noirs transparents) entre les petites bitmaps afin d’éviter toute interaction entre les petites images pendant les opérations. Il s’agit également d’un *Atlas*, et il présente l’avantage de réduire la surcharge liée à la création de bitmaps et les gaspillages de mémoire des petites allocations de bitmap. Nous vous recommandons de conserver la plupart des bitmaps à au moins 64 Ko et de limiter le nombre de bitmaps inférieurs à 4 Ko.

### <a name="create-an-atlas-of-bitmaps"></a>Créer un Atlas de bitmaps

Un Atlas des bitmaps peut être très bien utilisé dans certains scénarios courants. Les petites bitmaps peuvent être stockées dans une grande bitmap. Ces petites bitmaps peuvent être extraites de l’image bitmap la plus grande lorsque vous en avez besoin en spécifiant le rectangle de destination. Par exemple, une application doit dessiner plusieurs icônes. Toutes les bitmaps associées aux icônes peuvent être chargées en amont dans une grande bitmap. Et au moment du rendu, elles peuvent être récupérées à partir de la grande bitmap.

> [!Note]  
> Une bitmap Direct2D créée dans la mémoire vidéo est limitée à la taille maximale de bitmap prise en charge par l’adaptateur sur lequel elle est stockée. La création d’une bitmap plus grande peut entraîner une erreur.

 

> [!Note]  
> À partir de Windows 8, Direct2D comprend un [effet Atlas](atlas.md) qui peut faciliter ce processus.

 

### <a name="create-shared-bitmaps"></a>Créer des bitmaps partagées

La création de bitmaps partagées permet aux appelants avancés de créer des objets bitmap Direct2D qui sont sauvegardés directement par un objet existant, déjà compatible avec la cible de rendu. Cela évite de créer plusieurs surfaces et contribue à réduire la surcharge des performances.

> [!Note]  
> Les bitmaps partagées sont généralement limitées aux cibles logicielles ou aux cibles interopérables avec DXGI. Utilisez les méthodes [**CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)), [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1))et [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) pour créer des bitmaps partagées.

 

### <a name="copying-bitmaps"></a>Copier des bitmaps

La création d’une surface DXGI est une opération coûteuse, donc réutilisez des surfaces existantes lorsque vous le pouvez. Même dans les logiciels, si une bitmap est principalement sous la forme souhaitée, à l’exception d’une petite partie, il est préférable de mettre à jour cette partie plutôt que de lever l’intégralité de la bitmap et de recréer tout. Bien que vous puissiez utiliser [**CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) pour obtenir les mêmes résultats, le rendu est généralement une opération beaucoup plus coûteuse que la copie. Cela est dû au fait que, pour améliorer la localité de cache, le matériel ne stocke pas en fait une image bitmap dans le même ordre de mémoire que l’image bitmap. Au lieu de cela, la bitmap peut être swizzled. Le swizzling est masqué du processeur par le pilote (ce qui est lent et utilisé uniquement sur des parties inférieures) ou par le gestionnaire de mémoire sur le GPU. En raison de contraintes sur la façon dont les données sont écrites dans une cible de rendu lors du rendu, les cibles de rendu ne sont généralement pas swizzled ou swizzled d’une manière moins optimale que possible si vous savez que vous n’avez jamais besoin d’effectuer un rendu sur la surface. Par conséquent, les méthodes [CopyFrom](/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap) \* sont fournies pour copier des rectangles d’une source vers la bitmap Direct2D.

CopyFrom peut être utilisé dans l’une des trois formes suivantes :

-   [**CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)
-   [**CopyFromRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget)
-   [**CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory)

## <a name="use-tiled-bitmap-over-dashing"></a>Utiliser une image bitmap en mosaïque sur des tirets

Le rendu d’une ligne en pointillés est une opération très coûteuse en raison de la haute qualité et de la précision de l’algorithme sous-jacent. Pour la plupart des cas qui n’impliquent pas de géométries rectilignes, le même effet peut être généré plus rapidement à l’aide de bitmaps en mosaïque.

## <a name="general-guidelines-for-rendering-complex-static-content"></a>Instructions générales pour le rendu de contenu statique complexe

Mettez en cache le contenu si vous affichez le même frame de contenu sur le frame, en particulier lorsque la scène est complexe.

Vous pouvez utiliser trois techniques de mise en cache :

-   Mise en cache de scène complète à l’aide d’une bitmap de couleur.
-   Par mise en cache primitive à l’aide d’une bitmap a8 et de la méthode [**FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) .
-   Mise en cache par primitive utilisant des réalisations géométriques.

Examinons chacun de ces détails plus en détail.

### <a name="full-scene-caching-using-a-color-bitmap"></a>Mise en cache de scène complète à l’aide d’une bitmap de couleur

Lorsque vous affichez un contenu statique, dans des scénarios tels que l’animation, créez un autre bitmap de couleur complète au lieu d’écrire directement sur la bitmap d’écran. Enregistrez la cible actuelle, définissez la cible sur la bitmap intermédiaire et restituez le contenu statique. Ensuite, revenez à la bitmap d’écran d’origine et dessinez la bitmap intermédiaire dessus.

Voici un exemple :


```C++
// Create a bitmap.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_B8G8R8A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &sceneBitmap);

// Preserve the pre-existing target.
ComPtr<ID2D1Image> oldTarget;
m_d2dContext->GetTarget(&oldTarget);

// Render static content to the sceneBitmap.
m_d2dContext->SetTarget(sceneBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Render sceneBitmap to oldTarget.
m_d2dContext->SetTarget(oldTarget.Get());
m_d2dContext->DrawBitmap(sceneBitmap.Get());
```



Cet exemple utilise des bitmaps intermédiaires pour la mise en cache et change la bitmap vers laquelle le contexte de périphérique pointe lors du rendu. Cela évite d’avoir à créer une cible de rendu compatible dans le même but.

### <a name="per-primitive-caching-using-an-a8-bitmap-and-the-fillopacitymask-method"></a>Par mise en cache primitive à l’aide d’une bitmap a8 et de la méthode FillOpacityMask

Lorsque la scène complète n’est pas statique, mais se compose d’éléments tels que geometry ou Text qui sont statiques, vous pouvez utiliser une technique de mise en cache primitive. Cette technique conserve les caractéristiques d’anticrénelage de la primitive mise en cache et fonctionne avec les types de pinceau modifiés. Elle utilise une image bitmap A8, où a8 est un type de format de pixel qui représente un canal alpha avec 8 bits. Les bitmaps a8 sont utiles pour dessiner une géométrie/un texte en tant que masque. Lorsque vous devez manipuler l’opacité d’un contenu statique, au lieu de manipuler le contenu lui-même, vous pouvez translater, faire pivoter, incliner ou mettre à l’échelle l’opacité du masque.

Voici un exemple :


```C++
// Create an opacity bitmap.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

// Preserve the pre-existing target.
ComPtr<ID2D1Image> oldTarget;
m_d2dContext->GetTarget(&oldTarget);

// Render to the opacityBitmap.
m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Call the FillOpacityMask method
// Note: for this call to work correctly the anti alias mode must be D2D1_ANTIALIAS_MODE_ALIASED. 
m_d2dContext->SetTarget(oldTarget.Get());
m_d2dContext->FillOpacityMask(
    opacityBitmap.Get(),
    m_contentBrush().Get(),
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS);
```



## <a name="per-primitive-caching-using-geometry-realizations"></a>Mise en cache par primitive utilisant des réalisations géométriques

Une autre technique de mise en cache par primitive, appelée réalisation géométrique, offre une plus grande souplesse lors du traitement de Geometry. Lorsque vous souhaitez dessiner de manière répétée des géométries avec ou sans alias, il est plus rapide de les convertir en réalisations géométriques et de dessiner de manière répétée les mesures de réalisation qu’il ne faut dessiner à plusieurs reprises. Les proportions de géométrie consomment généralement moins de mémoire que les masques d’opacité (surtout pour les géométries volumineuses), et elles sont moins sensibles aux modifications de l’échelle. Pour plus d’informations, consultez [vue d’ensemble des réalisations géométriques](geometry-realizations-overview.md).

Voici un exemple :


```C++
    // Compute a flattening tolerance based on the scales at which the realization will be used.
    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(...);

    ComPtr<ID2D1GeometryRealization> geometryRealization;

    // Create realization of the filled interior of the geometry.
    m_d2dDeviceContext1->CreateFilledGeometryRealization(
        geometry.Get(),
        flatteningTolerance,
        &geometryRealization
        );

    // In your app's rendering code, draw the geometry realization with a brush.
    m_d2dDeviceContext1->BeginDraw();
    m_d2dDeviceContext1->DrawGeometryRealization(
        geometryRealization.Get(),
        m_brush.Get()
        );
    m_d2dDeviceContext1->EndDraw();
```



## <a name="geometry-rendering"></a>Rendu de géométrie

### <a name="use-specific-draw-primitive-over-draw-geometry"></a>Utiliser une primitive de dessin spécifique sur la géométrie de dessin

Utilisez des appels de dessin *primitif* plus spécifiques comme [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) sur les appels [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) génériques. En effet, avec **DrawRectangle**, la géométrie est déjà connue afin que le rendu soit plus rapide.

### <a name="rendering-static-geometry"></a>Rendu de Geometry statique

Dans les scénarios où la géométrie est statique, utilisez les techniques de mise en cache par primitive expliquées ci-dessus. Les masques d’opacité et les réalisations géométriques peuvent améliorer la vitesse de rendu des scènes qui contiennent une géométrie statique.

### <a name="use-a-multithreaded-device-context"></a>Utiliser un contexte de périphérique multithread

Les applications qui s’attendent à afficher des quantités significatives de contenu géométrique complexe doivent envisager de spécifier les [**options de contexte de périphérique d2d1 activer l’indicateur d' \_ \_ \_ \_ \_ \_ \_ optimisations**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_device_context_options) multithread lors de la création d’un contexte de périphérique [Direct2D](./direct2d-portal.md) . Lorsque cet indicateur est spécifié, Direct2D répartit le rendu sur tous les cœurs logiques présents sur le système, ce qui peut réduire considérablement le temps de rendu global.

Remarques :

-   À partir de Windows 8.1, cet indicateur affecte uniquement le rendu de la géométrie du chemin d’accès. Elle n’a aucun impact sur les scènes contenant uniquement d’autres types primitifs (tels que du texte, des bitmaps ou des réalisations géométriques).
-   En outre, cet indicateur n’a aucun impact lors du rendu dans le logiciel (par exemple, lors du rendu avec un périphérique Direct3D WARP). Pour contrôler le multithreading logiciel, les appelants doivent utiliser \_ l' \_ indicateur d3d11 créer \_ un appareil empêcher l' \_ \_ optimisation du Threading interne \_ lors de la création de l’appareil de distorsion Direct3D.
-   La spécification de cet indicateur peut augmenter le pic du jeu de travail pendant le rendu et peut également augmenter la contention des threads dans les applications qui tirent déjà parti du traitement multithread.

## <a name="drawing-text-with-direct2d"></a>Dessiner du texte avec Direct2D

La fonctionnalité de rendu de texte Direct2D est proposée en deux parties. La première partie, exposée comme la méthode [**ID2D1RenderTarget ::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) et [**ID2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , permet à un appelant de passer une chaîne et des paramètres de mise en forme ou un objet de disposition de texte DWrite pour plusieurs formats. Cela doit être adapté à la plupart des appelants. La deuxième façon de restituer du texte, exposé comme la méthode [**ID2D1RenderTarget ::D rawglyphrun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) , fournit la pixellisation pour les clients qui connaissent déjà la position des glyphes qu’ils souhaitent afficher. Les deux règles générales suivantes peuvent aider à améliorer les performances du texte lors du dessin dans Direct2D.

### <a name="drawtextlayout-vs-drawtext"></a>DrawTextLayout et DrawText

[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) et [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) permettent à une application de restituer facilement du texte mis en forme par l’API [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) . **DrawTextLayout** dessine un objet [**DWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) existant dans le [**renderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), et **DrawText** construit une disposition DirectWrite pour l’appelant, en fonction des paramètres transmis. Si le même texte doit être restitué plusieurs fois, utilisez **DrawTextLayout** au lieu de **DrawText**, car **DrawText** crée une disposition chaque fois qu’il est appelé.

### <a name="choosing-the-right-text-rendering-mode"></a>Choix du mode de rendu de texte approprié

Définissez le mode antialias du texte [**sur \_ d2d1 \_ mode antialias du texte \_ en \_ nuances de gris**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) explicitement. La qualité du rendu du texte en nuances de gris est comparable à ClearType mais est beaucoup plus rapide.

### <a name="caching"></a>Mise en cache

Utilisez une scène complète ou par mise en cache de bitmaps primitive comme pour le dessin d’autres Primitives.

## <a name="clipping-an-arbitrary-shape"></a>Découpage d’une forme arbitraire

La figure ci-dessous illustre le résultat de l’application d’un clip à une image.

![image qui montre un exemple d’image avant et après un clip.](images/clip.png)

Vous pouvez obtenir ce résultat en utilisant des couches avec un masque Geometry ou la méthode [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) avec un pinceau d’opacité.

Voici un exemple qui utilise une couche :


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



Voici un exemple qui utilise la méthode [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) :


```C++
// Create an opacity bitmap and render content.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Create an opacity brush from the opacity bitmap.
m_d2dContext->CreateBitmapBrush(opacityBitmap.Get(),
    D2D1::BitmapBrushProperties(),
    D2D1::BrushProperties(),
    &bitmapBrush);

// Call the FillGeometry method and pass in the clip geometry and the opacity brush
m_d2dContext->FillGeometry( 
    clipGeometry.Get(),
    brush.Get(),
    opacityBrush.Get()); 
```



Dans cet exemple de code, lorsque vous appelez la méthode PushLayer, vous ne transmettez pas de couche créée par une application. Direct2D crée une couche pour vous. Direct2D est en mesure de gérer l’allocation et la destruction de cette ressource sans aucune implication de l’application. Cela permet à Direct2D de réutiliser des couches en interne et d’appliquer des optimisations de gestion des ressources.

Dans Windows 8, de nombreuses optimisations ont été apportées à l’utilisation des couches et nous vous recommandons d’essayer d’utiliser les API de couche au lieu de [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) chaque fois que cela est possible.

### <a name="pushlayer-in-windows-8"></a>PushLayer dans Windows 8

L’interface [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) est dérivée de l’interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) et est la clé de l’affichage du contenu Direct2D dans Windows 8. pour plus d’informations sur cette interface, consultez [contextes de périphériques et](devices-and-device-contexts.md)de périphériques. Avec l’interface de contexte de périphérique, vous pouvez ignorer l’appel de la méthode [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) , puis passer la valeur null à la méthode [**ID2D1DeviceContext ::P ushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) . Direct2D gère automatiquement la ressource de couche et peut partager des ressources entre les couches et les graphiques d’effet.

### <a name="axis-aligned-clips"></a>Clips alignés sur l’axe

Si la région à découper est alignée sur l’axe de la surface de dessin, plutôt que arbitraire. Ce cas est adapté à l’utilisation d’un rectangle de découpage au lieu d’une couche. Le gain de performance est plus pour la géométrie avec alias que la géométrie avec anticrénelage. Pour plus d’informations sur les clips alignés sur l’axe, consultez la rubrique [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) .

## <a name="dxgi-interoperability-avoid-frequent-switches"></a>Interopérabilité des DXGI : Évitez les commutateurs fréquents

Direct2D peut interagir de façon transparente avec les surfaces Direct3D. Cela est très utile pour créer des applications qui restituent un mélange de contenu 2D et 3D. Mais chaque basculement entre le dessin du contenu Direct2D et Direct3D affecte les performances.

Lors du rendu sur une surface DXGI, Direct2D enregistre l’état des périphériques Direct3D lors du rendu et de sa restauration lorsque le rendu est terminé. À chaque fois qu’un lot de rendu Direct2D est terminé, le coût de l’enregistrement et de la restauration et le coût du vidage de toutes les opérations 2D sont payants, et pourtant, le périphérique Direct3D n’est pas vidé. Par conséquent, pour améliorer les performances, limitez le nombre de commutateurs de rendu entre Direct2D et Direct3D.

## <a name="know-your-pixel-format"></a>Connaître le format de pixel

Quand vous créez une cible de rendu, vous pouvez utiliser la structure de [**\_ \_ format de pixel d2d1**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) spécifiez le format de pixel et le mode Alpha utilisés par la cible de rendu. Un canal alpha fait partie du format de pixel qui spécifie la valeur de couverture ou les informations d’opacité. Si une cible de rendu n’utilise pas le canal alpha, elle doit être créée à l’aide du mode Alpha [**d2d1 \_ \_ \_ Ignorer**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) le mode Alpha. Cela réserve le temps consacré au rendu d’un canal alpha qui n’est pas nécessaire.

Pour plus d’informations sur les formats de pixel et les modes alpha, consultez [formats de pixel pris en charge et modes alpha](supported-pixel-formats-and-alpha-modes.md).

## <a name="scene-complexity"></a>Complexité de la scène

Lorsque vous analysez les zones réactives de performances dans une scène qui sera affichée, le fait de savoir si la scène est liée au taux de remplissage ou lié au sommet peut fournir des informations utiles.

-   Taux de remplissage : le taux de remplissage fait référence au nombre de pixels qu’une carte graphique peut afficher et à écrire dans la mémoire vidéo par seconde.
-   Limite de sommet : une scène est liée à un sommet lorsqu’elle contient un grand nombre de géométries complexes.

### <a name="understand-scene-complexity"></a>Comprendre la complexité des scènes

Vous pouvez analyser la complexité de votre scène en modifiant la taille de la cible de rendu. Si les gains de performances sont visibles pour une réduction proportionnelle de la taille de la cible de rendu, l’application est liée au taux de remplissage. Dans le cas contraire, la complexité de la scène est le goulot d’étranglement des performances.

Quand une scène est liée au taux de remplissage, la réduction de la taille de la cible de rendu peut améliorer les performances. Cela est dû au fait que le nombre de pixels à rendre est réduit proportionnellement à la taille de la cible de rendu.

Lorsqu’une scène est liée à un sommet, réduisez la complexité de la géométrie. Mais souvenez-vous que cette opération est effectuée au détriment de la qualité de l’image. Par conséquent, une décision prudente doit être prise entre la qualité souhaitée et les performances requises.

## <a name="improving-performance-for-direct2d-printing-apps"></a>Amélioration des performances pour les applications d’impression Direct2D

[Direct2D](./direct2d-portal.md) offre une compatibilité avec l’impression. Vous pouvez envoyer les mêmes commandes de dessin Direct2D (sous la forme de listes de commandes Direct2D) au contrôle d’impression Direct2D pour l’impression, si vous ne savez pas quels appareils vous dessinez, ou comment le dessin est converti en impression.

Vous pouvez affiner l’utilisation du contrôle d’impression [Direct2D](./direct2d-portal.md) et de vos commandes de dessin Direct2D pour fournir des résultats d’impression avec de meilleures performances.

Le contrôle d’impression [Direct2D](./direct2d-portal.md) génère des messages de débogage lorsqu’il voit un modèle de code Direct2D qui produit une qualité ou des performances d’impression plus faible (par exemple, des modèles de code listés plus loin dans cette rubrique) pour vous rappeler où vous pouvez éviter les problèmes de performances. Pour afficher ces messages de débogage, vous devez activer la [couche de débogage Direct2D](direct2ddebuglayer-portal.md) dans votre code. Pour obtenir des instructions sur l’activation de la sortie de message de débogage, consultez [messages de débogage](direct2ddebuglayer-debugmessages.md) .

### <a name="set-the-right-property-values-when-you-create-the-d2d-print-control"></a>Définir les valeurs de propriété appropriées lorsque vous créez le contrôle d’impression D2D

Vous pouvez définir trois propriétés lorsque vous créez le contrôle d’impression [Direct2D](./direct2d-portal.md) . Deux de ces propriétés ont un impact sur la façon dont le contrôle d’impression Direct2D gère certaines commandes Direct2D et, à leur tour, ont un impact sur les performances globales.

-   Mode de sous-ensemble de polices : le contrôle d’impression [Direct2D](./direct2d-portal.md) sous-définit les ressources de police utilisées dans chaque page avant d’envoyer la page à imprimer. Ce mode réduit la taille des ressources de page nécessaires à l’impression. En fonction de l’utilisation de la police dans la page, vous pouvez choisir différents modes de sous-ensemble de polices pour obtenir de meilleures performances.
    -   [**D2d1 \_ La \_ \_ \_ \_ valeur par défaut du mode imprimer le sous-ensemble de polices**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) fournit les meilleures performances d’impression dans la plupart des cas. Lorsqu’il est défini sur ce mode, le contrôle d’impression [Direct2D](./direct2d-portal.md) utilise une stratégie heuristique pour décider quand créer des sous-ensembles de polices.
    -   Pour les travaux d’impression courts avec 1 ou 2 pages, nous vous recommandons d’utiliser [**d2d1 \_ mode de \_ sous-ensemble de polices d’impression \_ \_ \_ EACHPAGE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) , où le contrôle d’impression [Direct2D](./direct2d-portal.md) sous-ensemble et incorpore les ressources de police dans chaque page, puis ignore ce sous-ensemble de police après l’impression de la page. Cette option permet de s’assurer que chaque page peut être imprimée immédiatement après sa génération, mais augmente légèrement la taille des ressources de page nécessaires à l’impression (avec généralement de grands sous-ensembles de polices).
    -   Pour les travaux d’impression comportant de nombreuses pages de texte et des tailles de police de petite taille (par exemple, des pages de texte 100 qui utilisent une police unique), nous vous recommandons d’utiliser le [**\_ mode de \_ \_ sous-ensemble de police d2d1 \_ \_ aucun**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode), où le contrôle d’impression [Direct2D](./direct2d-portal.md) ne fait pas partie des ressources de police ; à la place, il envoie les ressources de police d’origine, ainsi que la page qui utilise la police pour la première fois, et réutilise les ressources de police pour les pages ultérieures sans les renvoyer.
-   PPP de pixellisation : lorsque le contrôle d’impression [Direct2D](./direct2d-portal.md) doit pixelliser les commandes Direct2D pendant la conversion de DIRECT2D-XPS, il utilise cette PPP pour la pixellisation. En d’autres termes, si la page n’a pas de contenu pixellisé, la définition de n’importe quelle résolution ne modifiera pas les performances et la qualité. En fonction de l’utilisation de la pixellisation sur la page, vous pouvez choisir différentes dpi de pixellisation pour obtenir le meilleur équilibre entre la fidélité et les performances.
    -   150 est la valeur par défaut si vous ne spécifiez pas de valeur quand vous créez le contrôle d’impression [Direct2D](./direct2d-portal.md) , qui est le meilleur équilibre entre qualité d’impression et performances d’impression dans la plupart des cas.
    -   Les valeurs PPP supérieures produisent généralement une meilleure qualité d’impression (comme pour plus de détails), mais des performances inférieures en raison des bitmaps plus grandes générées. Nous ne recommandons aucune valeur DPI supérieure à 300, car cela n’introduira pas d’informations supplémentaires visuellement perceptibles par les yeux humains.
    -   Les PPP inférieurs peuvent entraîner de meilleures performances, mais peuvent également produire une qualité inférieure.

### <a name="avoid-using-certain-direct2d-drawing-patterns"></a>Évitez d’utiliser certains modèles de dessin Direct2D

Il existe des différences entre ce que [Direct2D](./direct2d-portal.md) peut représenter visuellement et ce que le sous-système d’impression peut conserver et transporter le long du pipeline d’impression entier. Le contrôle d’impression Direct2D fait combler ces lacunes en rapprochant ou en pixelliser les primitives Direct2D que le sous-système d’impression ne prend pas en charge en mode natif. Une telle approximation entraîne généralement une plus faible fidélité à l’impression, une baisse des performances d’impression, ou les deux. Par conséquent, même si un client peut utiliser les mêmes modèles de dessin pour le rendu à l’écran et à l’impression, il n’est pas idéal dans tous les cas. Il est préférable de ne pas utiliser autant de primitives et de modèles Direct2D que possible pour le chemin d’impression, ou de procéder à la pixellisation où vous disposez d’un contrôle total sur la qualité et la taille des images pixellisées.

La liste ci-dessous répertorie les cas où les performances et la qualité d’impression ne sont pas idéales et que vous pouvez envisager de faire varier le chemin de code pour optimiser les performances d’impression.

-   Évitez d’utiliser le mode de fusion primitif autre que [**d2d1 \_ primitive \_ Blend \_ SOURCEOVER**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend).
-   Évitez d’utiliser les modes de composition lors du dessin d’une image autre que la [**\_ \_ \_ source en \_**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_composite_mode) mode composite d2d1 sur la **\_ \_ destination en mode \_ \_ composite d2d1**.
-   Évitez de dessiner un méta-fichier GDI.
-   Évitez de pousser une ressource de couche qui copie l’arrière-plan source (en appelant [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-pushlayer) avec la transmission [**de la \_ couche d2d1 \_ options1 \_ Initialize de l' \_ \_ arrière-plan**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) vers le struct PARAMETERS1 de la **\_ couche \_ d2d1** ).
-   Évitez de créer un pinceau bitmap ou un pinceau d’image avec la \_ \_ pince en mode extension d2d1 \_ . Nous vous recommandons d’utiliser \_ le \_ mode \_ miroir du mode d2d1 Extend si vous ne vous souciez pas des pixels en dehors de l’image liée (par exemple, l’image attachée au pinceau est plus importante que la région cible remplie).
-   Évitez de dessiner des bitmaps avec des [transformations de perspective](3d-perspective-transform.md).

### <a name="draw-text-in-a-direct-and-plain-way"></a>Dessiner du texte de manière directe et simple

Direct2D propose plusieurs optimisations lors du rendu de textes à afficher pour de meilleures performances et/ou une meilleure qualité visuelle. Toutefois, toutes les optimisations améliorent les performances et la qualité d’impression puisque l’impression sur le papier est généralement plus élevée, et l’impression n’a pas besoin de prendre en charge des scénarios tels que l’animation. Nous vous recommandons donc de dessiner directement le texte ou les glyphes d’origine et d’éviter les optimisations suivantes lors de la création de la liste de commandes pour l’impression.

-   Évitez de dessiner du texte à l’aide de la méthode [**FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-fillopacitymask) .
-   Évitez de dessiner du texte en mode alias.

### <a name="draw-the-original-bitmaps-when-possible"></a>Dessiner les bitmaps d’origine lorsque cela est possible

Si la bitmap cible est un fichier JPEG, PNG, TIFF ou JPEG-XR, vous pouvez créer une bitmap WIC à partir d’un fichier de disque ou d’un flux en mémoire, puis créer une bitmap [Direct2D](./direct2d-portal.md) à partir de cette bitmap WIC à l’aide de [**ID2D1DeviceContext :: CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1)), puis passer directement cette bitmap Direct2D au contrôle d’impression Direct2D sans manipulation supplémentaire. En procédant ainsi, le contrôle d’impression Direct2D peut réutiliser le flux bitmap, ce qui entraîne généralement une meilleure impression des performances (en ignorant l’encodage et le décodage des bitmaps redondants) et une meilleure qualité d’impression (lorsque les métadonnées, telles que les profils de couleurs, dans le bitmap sont conservées).

Le dessin de la bitmap d’origine offre les avantages suivants pour les applications.

-   En règle générale, l’impression de [Direct2D](./direct2d-portal.md) conserve les informations d’origine (sans perte ou bruit) jusqu’à la fin du pipeline, en particulier lorsque les applications ne savent pas (ou ne souhaitent pas connaître) les détails du pipeline d’impression (comme l’imprimante sur laquelle il imprime, la résolution de l’imprimante cible, etc.).
-   Dans de nombreux cas, le retardement de la pixellisation des bitmaps permet d’améliorer les performances (par exemple, lors de l’impression d’une photo 96dpi sur une imprimante 600dpi).
-   Dans certains cas, passer les images d’origine est le seul moyen de respecter la haute fidélité (comme les profils de couleurs incorporés).

Toutefois, vous ne pouvez pas opter pour cette optimisation, car :

-   En interrogeant les informations d’imprimante et la pixellisation précoce, vous pouvez pixelliser le contenu lui-même avec le contrôle total de l’apparence finale sur le papier.
-   Dans certains cas, la première pixellisation peut en fait améliorer les performances de bout en bout d’une application (comme l’impression des photos de taille).
-   Dans certains cas, passer les bitmaps d’origine nécessite un changement important de l’architecture du code existant (comme le chargement différé des images et les chemins de mise à jour des ressources dans certaines applications).

## <a name="conclusion"></a>Conclusion

Bien que Direct2D soit accéléré par le matériel et soit conçu pour des performances élevées, vous devez utiliser les fonctionnalités correctement pour maximiser le débit. Les techniques que nous avons étudiées ici sont dérivées de l’étude des scénarios courants et peuvent ne pas s’appliquer à tous les scénarios d’application.

 

 
