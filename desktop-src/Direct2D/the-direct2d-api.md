---
title: Vue d’ensemble de l’API Direct2D.
description: Fournit une vue d’ensemble du modèle objet Direct2D.
ms.assetid: b1362ef6-40fc-4fa5-ba5b-22c622c39f04
keywords:
- Direct2D, à propos de
- Direct2D, fichiers d’en-tête
- Direct2D, modèle objet
- Direct2D, interfaces
- Interface ID2D1Factory
- Direct2D, cibles de rendu
- cibles de rendu, à propos de
- Direct2D, commandes de dessin
- cibles de rendu, commandes de dessin
- Direct2D, gestion des erreurs
- cibles de rendu, gestion des erreurs
- gestion des erreurs
- pinceaux
- cibles de rendu, pinceaux
- geometries
- Direct2D, géométries
- bitmaps pour Direct2D
- Direct2D, bitmaps
- Primitives
- Direct2D, Primitives
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858d03f626fe337b174f074d7725dcb1a636b463
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106530794"
---
# <a name="direct2d-api-overview"></a>Vue d’ensemble de l’API Direct2D.

Direct2D fournit une API, similaire à Direct3D, à utiliser avec C ou C++. L’API expose une variété de fonctionnalités liées au dessin :

-   Rendez les cibles pour l’affichage et le rendu hors écran à l’aide de Direct2D, Direct3D ou GDI.
-   Objets pour gérer l’état du dessin, tels que les transformations d’espace de coordonnées et les modes d’anticrénelage.
-   Représentations des données géométriques et des fonctions de traitement de géométrie.
-   Fonctionnalités de rendu pour les bitmaps, les géométries et le texte.
-   Provisions pour l’utilisation de contenu graphique créé à l’aide de GDI ou Direct3D.

Cette rubrique fournit une vue d’ensemble des objets qui composent l’API Direct2D. Il contient les sections suivantes :

-   [Fichiers d’en-tête Direct2D](#direct2d-header-files)
-   [Interfaces Direct2D](#direct2d-interfaces)
-   [Interface ID2D1Factory](#the-id2d1factory-interface)
-   [Cibles de rendu](#render-targets)
    -   [Fonctionnalités de la cible de rendu](#render-target-features)
    -   [Afficher les ressources cibles](#render-target-resources)
    -   [Commandes de dessin](#drawing-commands)
    -   [Gestion des erreurs](#error-handling)
-   [Ressources de dessin](#drawing-resources)
    -   [Pinceaux](#brushes)
    -   [Géométries](#geometries)
    -   [Images bitmap](#bitmaps)
-   [Dessiner du texte](#drawing-text)
-   [Primitives Direct2D](#direct2d-primitives)
-   [Rubriques connexes](#related-topics)

## <a name="direct2d-header-files"></a>Fichiers d’en-tête Direct2D

L’API Direct2D est définie par les fichiers d’en-tête suivants.

| Fichier d’en-tête         | Description                                                                                                                  |
|---------------------|------------------------------------------------------------------------------------------------------------------------------|
| d2d1. h              | Définit les versions C et C++ de l’API Direct2D principale.                                                                      |
| d2d1helper. h        | Définit des fonctions, des classes et des structures d’assistance C++.                                                                       |
| d2dbasetypes. h      | Définit des primitives de dessin pour Direct2D, telles que des points et des rectangles. Cet en-tête est inclus dans d2d1. h.                 |
| d2derr. h            | Définit les codes d’erreur pour Direct2D. Cet en-tête est inclus dans d2d1. h.                                                   |
| d2d1 \_ 1. h           | Définit les versions C et C++ de l’API Direct2D principale pour Windows 8 et versions ultérieures.                                              |
| d2d1 \_ 1helper. h     | Définit des fonctions, des classes et des structures d’assistance C++ pour Windows 8 et versions ultérieures.                                               |
| d2d1effects. h       | Définit les versions C et C++ de la partie effets d’image de l’API Direct2D pour Windows 8 et versions ultérieures.                            |
| d2d1effecthelpers. h | Définit les fonctions, les classes et les structures d’assistance C++ de la partie effets d’image de l’API Direct2D pour Windows 8 et versions ultérieures. |



 

Pour utiliser Direct2D, votre application doit inclure le fichier d’en-tête d2d1. h.

Pour compiler une application Direct2D, ajoutez d2d1. lib à la liste des bibliothèques. Vous pouvez trouver d2d1. h et d2d1. lib dans le [Kit de développement logiciel (SDK) Windows pour Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).

Les sections suivantes décrivent certaines des interfaces courantes fournies par l’API Direct2D.

## <a name="direct2d-interfaces"></a>Interfaces Direct2D

À la racine de l’API Direct2D se trouvent les interfaces [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) et [**ID2D1Resource**](/windows/win32/api/d2d1/nn-d2d1-id2d1resource) . Un objet **ID2D1Factory** crée des objets **ID2D1Resource** et sert de point de départ pour l’utilisation de Direct2D. Tous les autres objets Direct2D héritent de l’interface **ID2D1Resource** . Il existe deux types de ressources Direct2D : les ressources indépendantes du périphérique et les ressources dépendantes du périphérique.

-   Les ressources indépendantes du périphérique ne sont pas associées à un périphérique de rendu particulier et peuvent être conservées pendant toute la durée de vie d’une application.
-   Les ressources dépendantes de l’appareil sont associées à un appareil de rendu particulier et cessent de fonctionner si l’appareil est supprimé.

(Pour plus d’informations sur les ressources et le partage de ressources, consultez la [vue d’ensemble des ressources](resources-and-resource-domains.md).)

## <a name="the-id2d1factory-interface"></a>Interface ID2D1Factory

L’interface [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) est le point de départ pour l’utilisation de Direct2D. Vous utilisez un **ID2D1Factory** pour instancier des ressources Direct2D. Pour créer un ID2D1Factory, vous utilisez l’une des méthodes [**CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) .

Une fabrique définit un ensemble de méthodes Create *Resource* qui peuvent produire les ressources de dessin suivantes :

-   Les cibles de rendu sont des objets qui restituent les commandes de dessin.
-   Les blocs d’état de dessin sont des objets qui stockent des informations d’état de dessin, telles que la transformation actuelle et le mode d’anticrénelage.
-   Les géométries sont des objets qui représentent des formes simples et potentiellement complexes.

L’un des objets les plus utiles qu’une fabrique peut créer est le [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), décrit dans la section suivante.

## <a name="render-targets"></a>Cibles de rendu

Une cible de rendu est une ressource qui hérite de l’interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) . Une cible de rendu crée des ressources pour dessiner et effectuer des opérations de dessin. Il existe plusieurs types de cibles de rendu qui peuvent être utilisées pour restituer des graphiques des manières suivantes :

-   Les objets [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) affichent le contenu dans une fenêtre.
-   Les objets [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) sont rendus dans un contexte de périphérique GDI.
-   Les objets cibles de rendu bitmap affichent le contenu dans une image bitmap hors écran.
-   Les objets cibles de rendu DXGI sont rendus sur une surface DXGI pour une utilisation avec Direct3D.

Étant donné qu’une cible de rendu est associée à un appareil de rendu particulier, il s’agit d’une ressource dépendante de l’appareil qui cesse de fonctionner si l’appareil est supprimé.

### <a name="render-target-features"></a>Fonctionnalités de la cible de rendu

Vous pouvez spécifier si une cible de rendu doit utiliser l’accélération matérielle et si l’affichage à distance doit être rendu par l’ordinateur local ou distant. Les cibles de rendu peuvent être configurées pour le rendu avec ou sans alias. Pour le rendu des scènes avec un grand nombre de primitives, un développeur peut également restituer des graphiques 2D en mode alias et utiliser l’anticrénelage à plusieurs échantillons D3D pour obtenir une plus grande évolutivité.

Les cibles de rendu peuvent également regrouper des opérations de dessin dans des couches qui sont représentées par l’interface [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) . Les couches sont utiles pour la collecte des opérations de dessin à combiner lors du rendu d’un frame. Pour certains scénarios, il peut s’agir d’une alternative utile au rendu d’une cible de rendu bitmap, puis de la réutilisation du contenu de l’image bitmap, car les coûts d’allocation pour la superposition sont inférieurs à ceux d’un [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).

Les cibles de rendu peuvent créer de nouvelles cibles de rendu qui sont compatibles avec elles-mêmes, ce qui est utile pour le rendu non-écran intermédiaire tout en conservant les diverses propriétés de cible de rendu qui ont été définies sur le d’origine.

Il est également possible d’effectuer un rendu à l’aide de GDI sur une cible de rendu Direct2D en appelant [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur une cible de rendu pour [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), qui contient des méthodes [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) et [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) qui peuvent être utilisées pour récupérer un contexte de périphérique GDI. Le rendu via GDI est possible uniquement si la cible de rendu a été créée avec l’indicateur de [**\_ \_ \_ \_ \_ compatibilité GDI**](/windows/win32/api/d2d1/ne-d2d1-d2d1_render_target_usage) de l’utilisation de la cible de rendu d2d1 définie. Cela est utile pour les applications qui s’affichent principalement avec Direct2D, mais qui ont un modèle d’extensibilité ou tout autre contenu hérité qui requiert la possibilité d’effectuer un rendu avec GDI. Pour plus d’informations, consultez [vue d’ensemble de l’interopérabilité de Direct2D et GDI](direct2d-and-gdi-interoperation-overview.md).

### <a name="render-target-resources"></a>Afficher les ressources cibles

À l’instar d’une fabrique, une cible de rendu peut créer des ressources de dessin. Toutes les ressources créées par une cible de rendu sont des ressources dépendantes de l’appareil (tout comme la cible de rendu). Une cible de rendu peut créer les types de ressources suivants :

-   Images bitmap
-   Pinceaux
-   Calques
-   Maillages

### <a name="drawing-commands"></a>Commandes de dessin

Pour afficher le contenu, vous utilisez les méthodes de dessin de la cible de rendu. Avant de commencer à dessiner, vous appelez la méthode [**ID2D1RenderTarget :: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) . Une fois que vous avez terminé le dessin, vous appelez la méthode [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Entre ces appels, vous utilisez des méthodes de dessin et de remplissage pour restituer les ressources de dessin. La plupart des méthodes de dessin et de remplissage prennent une forme (une primitive ou une géométrie) et un pinceau pour remplir ou mettre en relief la forme.

Les cibles de rendu fournissent également des méthodes pour le découpage, l’application de masques d’opacité et la transformation de l’espace de coordonnées.

Direct2D utilise un système de coordonnées gauche : les valeurs positives de l’axe des x continuent à droite et les valeurs positives de l’axe des y s’effectuent vers le bas.

### <a name="error-handling"></a>Gestion des erreurs

Les commandes de dessin de la cible de rendu n’indiquent pas si l’opération demandée a réussi. Pour déterminer s’il y a eu des erreurs de dessin, appelez la méthode de [**vidage**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) de la cible de rendu ou la méthode [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) pour obtenir un **HRESULT**.

## <a name="drawing-resources"></a>Ressources de dessin

Les sections suivantes décrivent certaines des ressources qui peuvent être créées par la cible de rendu et les interfaces de fabrique.

### <a name="brushes"></a>Pinceaux

Un pinceau, représenté par l’interface [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) , est une ressource dépendante de l’appareil, créée par une cible de rendu, qui peint une zone avec sa sortie. Des pinceaux différents ont différents types de sortie. Certains pinceaux peignent une zone avec une couleur unie, d’autres avec un dégradé ou une image. Direct2D fournit quatre types de pinceaux :

-   [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) peint une zone avec une couleur unie.
-   [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) peint une zone avec un dégradé linéaire qui fusionne deux couleurs ou plus sur une ligne, l’axe du dégradé.
-   [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) peint une zone avec un dégradé radial qui fusionne deux couleurs ou plus autour d’une ellipse.
-   [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) peint une zone avec une image bitmap.

Pour créer un pinceau, vous utilisez l’une des méthodes de pinceau [**ID2D1RenderTarget ::**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)Create *<Type>* , telles que [**CreateRadialGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)). Les pinceaux peuvent être utilisés avec les méthodes de dessin et de remplissage d’une cible de rendu, soit pour peindre un trait ou un contour de forme, soit comme masque d’opacité.

Pour plus d’informations sur les pinceaux, consultez [vue d’ensemble des pinceaux](direct2d-brushes-overview.md).

### <a name="geometries"></a>Géométries

En plus des primitives de dessin de base telles que les points, rectangles et ellipses, Direct2D fournit l’interface [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) pour décrire des formes simples et complexes. Les interfaces qui héritent de **ID2D1Geometry** définissent différents types de formes, telles que [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) pour représenter des rectangles, [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) pour représenter des rectangles arrondis, et [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) pour représenter des ellipses.

Des formes plus complexes peuvent être créées à l’aide de l’interface [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) pour spécifier une série de figures composée de lignes, de courbes et d’arcs. Le **ID2D1GeometrySink** est passé à la méthode Open d’un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) pour générer une géométrie complexe. [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) peut également être utilisé avec l’API DirectWrite pour extraire des contours de chemin du texte mis en forme pour un rendu artistique.

Les interfaces Geometry fournissent des méthodes pour manipuler des formes en élargissant ou en simplifiant les géométries existantes, ou en générant l’intersection ou l’Union de plusieurs géométries. Elles fournissent également des méthodes pour déterminer si les géométries se croisent ou se chevauchent, récupèrent les informations relatives aux limites, calculent la zone ou la longueur d’une géométrie et interpolent des emplacements le long d’une géométrie. Direct2D offre également la possibilité de créer un maillage de triangles qui est fractionné à partir d’une géométrie.

Pour créer une géométrie, vous utilisez l’une des méthodes [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory):: Create *<Type>* Geometry, telles que [**CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry). Une géométrie est une ressource indépendante du périphérique.

Pour afficher une géométrie, vous utilisez les méthodes [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) et [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) d’une cible de rendu.

Pour plus d’informations sur les géométries, consultez [vue d’ensemble des géométries](direct2d-geometries-overview.md).

### <a name="bitmaps"></a>Images bitmap

Direct2D ne fournit pas de méthodes pour charger ou stocker des bitmaps ; au lieu de cela, il vous permet de créer des bitmaps à l’aide du [WIC (Windows Imaging Component)](../wic/-wic-about-windows-imaging-codec.md). Les ressources bitmap peuvent être chargées à l’aide de WIC, puis utilisées pour créer un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) via la méthode [**ID2D1RenderTarget :: CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties_id2d1bitmap)) .

Les bitmaps peuvent également être créées à partir de données en mémoire qui ont été configurées par d’autres moyens. Une fois qu’une bitmap a été créée, elle peut être dessinée par la méthode [**DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) de la cible de rendu ou par un pinceau bitmap.

Étant donné que la création de ressources bitmap sur des cibles de rendu matériel est souvent une opération coûteuse, Direct2D peut mettre à jour le contenu d’une bitmap (ou d’une partie de la bitmap) à l’aide des méthodes [**CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap), [**CopyFromRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget)et [**CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory) . L’utilisation de ces méthodes peut potentiellement enregistrer les coûts associés aux allocations de texture GPU supplémentaires.

## <a name="drawing-text"></a>Dessiner du texte

Direct2D a été conçu pour fonctionner avec les opérations de texte de la nouvelle API Text, DirectWrite. Pour faciliter l’utilisation de l’API DirectWrite, les cibles de rendu fournissent trois méthodes pour le rendu des ressources de texte DirectWrite : [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)et [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun). Étant donné que Direct2D utilise le GPU pour le processus de rendu de texte ClearType, Direct2D fournit une utilisation de l’UC inférieure à GDI pour les opérations de texte et une meilleure évolutivité à mesure que la puissance de traitement GPU est disponible.

[**ID2D1RenderTarget ::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) est conçu pour les scénarios les plus simples impliquant le rendu d’une chaîne de texte Unicode avec une mise en forme minimale. Une disposition plus complexe et une flexibilité typographique sont fournies par le biais de la méthode [**ID2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , qui utilise un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) pour spécifier le contenu et la mise en forme à restituer. **IDWriteTextLayout** vous permet de spécifier une mise en forme individuelle pour les sous-chaînes de texte et d’autres options typographiques avancées.

Pour les scénarios où un contrôle précis de la disposition au niveau du glyphe est requis, la méthode [**ID2D1RenderTarget ::D rawglyphrun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) peut être utilisée conjointement avec les fonctionnalités de mesure fournies par [DirectWrite](../directwrite/direct-write-portal.md).

Pour utiliser l’API DirectWrite, incluez l’en-tête DWrite. h. À l’instar de Direct2D, DirectWrite utilise une fabrique, [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) pour créer des objets de texte. Utilisez la fonction [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) pour créer une fabrique, puis utilisez ses méthodes Create pour créer des ressources DirectWrite (telles que [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))).

Pour plus d’informations sur DirectWrite, consultez la rubrique [Présentation de DirectWrite](../directwrite/introducing-directwrite.md) .

## <a name="direct2d-primitives"></a>Primitives Direct2D

Direct2D définit un ensemble de primitives similaires à celles fournies par d’autres API de dessin. Il fournit une structure de couleur, une structure de matrice pour effectuer des transformations, ainsi que des versions à virgule flottante et entières de points, de rectangles, de points de suspension et de structures de taille. En général, vous utilisez les versions à virgule flottante de ces structures.

Vous n’utilisez pas une fabrique ou une cible de rendu pour instancier des primitives Direct2D. Vous pouvez les créer directement ou utiliser les méthodes d’assistance définies dans d2d1helper. h pour les créer.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence Direct2D](reference.md)
</dt> <dt>

[Exemple de Hello World DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples)
</dt> <dt>

[Présentation de DirectWrite](../directwrite/introducing-directwrite.md)
</dt> <dt>

[Vue d’ensemble des ressources](resources-and-resource-domains.md)
</dt> <dt>

[Composant Imagerie Windows (WIC)](../wic/-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 