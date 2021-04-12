---
title: Nouveautés de Direct2D
description: Voici quelques-uns des nouveaux ajouts à Direct2D.
ms.assetid: BA459FF0-9457-4652-A97C-BD4EC57EC8E2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 9208ded926bda197baf41d9195c13cacd8f7079b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315653"
---
# <a name="whats-new-in-direct2d"></a>Nouveautés de Direct2D

Voici quelques-uns des nouveaux ajouts à Direct2D.

## <a name="whats-new-for-windows-10-creators-update"></a>Nouveautés de Windows 10 Creators Update

Les fonctionnalités et les API suivantes ont été ajoutées ou mises à jour pour Windows 10 Creators Update.

### <a name="support-for-svg-image-rendering"></a>Prise en charge du rendu d’images SVG

À compter de Windows 10 Creators Update, Direct2D assure la prise en charge de l’analyse et du dessin d’images SVG, ce qui permet aux développeurs d’afficher les ressources produites dans leurs outils d’art vectoriels préférés sans les convertir en images raster. Utilisez cette fonctionnalité pour améliorer l’encombrement du disque et le comportement de mise à l’échelle de votre iconographie dans l’application et utilisez les nouvelles API du modèle d’objet SVG Direct2d pour apporter des modifications par programmation au SVG de votre application. Notez que Direct2D ne prend en charge qu’un sous-ensemble limité de SVG adapté aux images et ne prend pas en charge toutes les fonctionnalités de dessin SVG. Si vous avez besoin d’une compatibilité SVG de niveau navigateur ou des fonctionnalités orientées Web de SVG, envisagez d’utiliser le [contrôle XAML WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView) à la place. Pour plus d'informations, voir les rubriques suivantes :

-   [Exemple de rendu d’image SVG Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DSvgImage)
-   [Prise en charge SVG](svg-support.md)
-   [**ID2D1DeviceContext5 :: CreateSvgDocument**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createsvgdocument) , méthode
-   [**ID2D1DeviceContext5 ::D méthode rawsvgdocument**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-drawsvgdocument)
-   Interface [**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)

### <a name="improved-support-for-color-management"></a>Prise en charge améliorée de la gestion des couleurs

À compter de Windows 10 Creators Update, Direct2D offre des fonctionnalités de gestion des couleurs améliorées. Les développeurs n’ont plus besoin d’un profil ICC pour utiliser l’effet de gestion des couleurs Direct2d. ils peuvent désormais utiliser des espaces de couleurs DXGI ou construire leur propre définition d’espace colorimétrique paramétré. Pour plus d'informations, voir les rubriques suivantes :

-   [Effet de gestion des couleurs](color-management.md)
-   [**ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace)
-   [**ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile_id2d1colorcontext1))

## <a name="whats-new-for-windows-10-anniversary-update"></a>Nouveautés de la mise à jour anniversaire de Windows 10

Les fonctionnalités et les API suivantes ont été ajoutées ou mises à jour pour la mise à jour anniversaire Windows 10.

### <a name="improved-support-for-color-fonts"></a>Prise en charge améliorée des polices en couleur

À compter de la mise à jour anniversaire de Windows 10, Direct2D prend désormais en charge le rendu d’une plus grande variété de formats de police de couleur, ce qui permet aux développeurs d’utiliser plus de types de polices dans leurs applications basées sur Direct2D que jamais auparavant. Cela inclut la prise en charge des éléments suivants :

-   La table OpenType « COLR », qui active le contenu vectoriel compact dans les polices. (Pris en charge depuis Windows 8.1.)
-   La table OpenType « SVG », qui active le contenu SVG dans les polices.
-   La table OpenType « CBDT », qui permet de coloriser le contenu de la bitmap dans les polices.
-   La table OpenType « sbix », qui permet de coloriser le contenu de la bitmap dans les polices.

Direct2D prend en charge automatiquement ces formats de police de couleur lorsque les [**options de dessin d2d1 activer l’indicateur de \_ \_ \_ \_ \_ \_ police de couleur**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_draw_text_options) sont activées. Pour plus d'informations, voir les rubriques suivantes :

-   [Polices de couleur](/windows/desktop/DirectWrite/color-fonts)
-   [Exemple de glyphe de couleurs DirectWrite](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)

### <a name="new-image-effects"></a>Nouveaux effets d’images

À compter de la mise à jour anniversaire Windows 10, Direct2D comprend les effets de AlphaMask, de fondu enchaîné, d’opacité et de teinte. Cette fonctionnalité était précédemment disponible à partir de configurations spécifiques d’effets composites, ArithmeticComposite et ColorMatrix, mais les nouveaux effets intégrés facilitent les opérations courantes.

## <a name="whats-new-for-windows-10"></a>Nouveautés de Windows 10

Les fonctionnalités et les API suivantes ont été ajoutées ou mises à jour pour Windows 10.

### <a name="sprite-batches"></a>Lots de sprites

À compter de Windows 10, Direct2D assure la prise en charge de la création et du rendu des lots Sprite. Par rapport à la méthode [**DrawImage**](id2d1devicecontext-drawimage-overload.md) à usage général, les lots Sprite entraînent une charge de processeur par image moins importante. Cela les rend idéales pour les scénarios impliquant des centaines ou des milliers d’images simultanées, telles que des sprites de jeux ou des systèmes de particule. Pour plus d'informations, voir les rubriques suivantes :

-   [**ID2D1DeviceContext3 :: CreateSpriteBatch**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-createspritebatch) , méthode
-   [**ID2D1DeviceContext3 ::D méthodes rawspritebatch**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-drawspritebatch(id2d1spritebatch_id2d1bitmap_d2d1_bitmap_interpolation_mode_d2d1_sprite_options))
-   Interface [**ID2D1SpriteBatch**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1spritebatch)

### <a name="gradient-meshes"></a>Maillages dégradés

À partir de Windows 10, Direct2D fournit une nouvelle primitive pour les maillages de dégradé. Les maillages dégradés sont souvent utilisés par des Illustrators professionnels dans des logiciels de conception graphique, et ils permettent aux artistes d’afficher des formes complexes (même des couleurs réalistes) avec tous les avantages de la mémoire et de l’évolutivité des vecteurs. Pour plus d’informations, consultez les rubriques suivantes :

-   [Exemple de maillage dégradé Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DGradientMesh)
-   [**D2d1 \_ Structure \_ de \_ patch du maillage dégradé**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch)
-   [**ID2D1DeviceContext2 ::D méthode rawgradientmesh**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawgradientmesh)

### <a name="improved-image-loading-apis"></a>Amélioration des API de chargement d’image

À compter de Windows 10, Direct2D offre une nouvelle API pour le chargement d’images, ID2D1ImageSource. La source d’image améliore les API de chargement d’image existantes, y compris CreateBitmapFromWicBitmap, l’effet de source bitmap et l’effet YCbCr. La source d’image Direct2D combine les fonctionnalités de ces API avec la prise en charge des images arbitraires de grande taille, une intégration facile avec l’impression et les effets, ainsi que de nombreuses optimisations, notamment le JPEG YCbCr et l’index JPEG indexé. Pour plus d’informations, consultez les rubriques suivantes :

-   [Exemple de kit de développement logiciel de l’ajustement de photos Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)
-   [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource)
-   [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)
-   [IWICJpegFrameDecode::SetIndexing](/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-setindexing)

### <a name="improved-support-for-ink-rendering"></a>Prise en charge améliorée du rendu de l’encre

À compter de Windows 10, Direct2D fournit une nouvelle primitive pour représenter les traits d’encre. Les traits d’encre de Direct2D sont définis par des courbes de Bézier, prennent en charge différentes formes et transformations de stylo et peuvent avoir une épaisseur fixe ou variable. La prise en charge intégrée de Direct2d pour les traits d’encre permet aux applications d’effectuer facilement un rendu plus rapide et plus beau que les approches précédentes, ce qui nécessite généralement que les applications gèrent l’encre proprement dit, comme une série de ellipses et de quadrilatères. Pour plus d'informations, voir les rubriques suivantes :

-   [**Interface ID2D1Ink**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1ink)
-   [**ID2D1DeviceContext2 ::D méthode rawInk**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawink)
-   [**Interface ID2D1InkStyle**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1inkstyle)

### <a name="effect-shader-linking"></a>Liaison d’effet nuanceur

Les effets Direct2D sont implémentés à l’aide des nuanceurs de calcul, de vertex et de pixels HLSL. À partir de Windows 10, Direct2D analyse désormais automatiquement les graphiques d’effet pour les opportunités de combiner et d’exécuter des nuanceurs individuels. Cela peut augmenter considérablement le débit d’effet. Les consommateurs d’effets intégrés n’ont rien à faire pour tirer parti de la liaison de nuanceur d’effets, mais les développeurs qui créent leurs propres effets personnalisés doivent suivre les meilleures pratiques mises à jour pour tirer parti de la liaison de nuanceur d’effets. Pour plus d'informations, voir les rubriques suivantes :

-   [Liaison de nuanceurs d’effet](effect-shader-linking.md)
-   [Applications auxiliaires HLSL Direct2D](hlsl-helpers.md)
-   [Exemple de kit de développement logiciel des effets personnalisés Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)

La liaison effet du nuanceur est conçue pour ne pas affecter la sortie visuelle des effets. Toutefois, cela n’est pas toujours possible en raison d’un comportement spécifique autour de la précision de l’effet et du découpage numérique. Pour plus d’informations sur la façon de contrôler ces comportements, consultez :

-   [Contrôle de la précision et du découpage numérique dans les graphiques d’effet](precision-and-clipping-in-effect-graphs.md)

### <a name="new-built-in-effects"></a>Nouveaux effets intégrés

À compter de Windows 10, Direct2D comprend un ensemble complet de nouveaux effets intégrés qui répondent aux principales demandes des développeurs et permettent de nouveaux types de scénarios visuels. Les nouveaux effets sont les suivants :

### <a name="color"></a>Couleur :

-   [Effet RVB/teinte](rgb-to-hue-effect.md)
-   [Effet teinte à RVB](hue-to-rgb-effect.md)
-   [effet de table de recherche 3D](3d-lookup-table-effect.md)

### <a name="photo"></a>Photos

-   [Effet de contraste](contrast-effect.md)
-   [Effet d’exposition](exposure-effect.md)
-   [Effet de nuances de gris](grayscale-effect.md)
-   [Effets des tons clairs et des ombres](highlights-and-shadows-effect.md)
-   [Effet négatif](invert-effect.md)
-   [Effet sépia](sepia-effect.md)
-   [Effet de la netteté](sharpen-effect.md)
-   [Effet de redresser](straighten-effect.md)
-   [Effet de température et de teinte](temperature-and-tint-effect.md)
-   [Effet vignette](vignette-effect.md)

### <a name="filter"></a>Filtre :

-   [Effet de détection de périphérie](edge-detection-effect.md)

### <a name="stylize"></a>Stylisez

-   [Effet de relief](emboss-effect.md)
-   [Effet Postérisation](posterize-effect.md)

### <a name="transparency"></a>Transparence :

-   [Effet clé Chroma](chromakey-effect.md)

Les effets de redressement, de saturation, de contraste, de surbrillances et d’ombres, ainsi que les effets de température et de teinte sont illustrés dans l' [exemple du kit de développement logiciel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)

## <a name="whats-new-for-windows-81"></a>Nouveautés de Windows 8.1

Les fonctionnalités et les API suivantes ont été ajoutées ou mises à jour pour Windows 8.1.

À partir de Windows 8.1, Direct2D s’appuie sur Direct3D 11,2.

### <a name="geometry-realizations"></a>Réalisations géométriques

À partir de Windows 8.1, Direct2D offre des réalisations géométriques. Les réalisations géométriques permettent aux applications d’améliorer les performances de rendu géométrique dans certaines situations, sans avoir certains des inconvénients de la pixellisation d’une géométrie en bitmap. Pour plus d'informations, voir les rubriques suivantes :

-   Interface [**ID2D1Device1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1device1)
-   [**ID2D1DeviceContext1 ::D méthode rawgeometryrealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization)

### <a name="support-for-jpeg-ycbcr-images"></a>Prise en charge des images JPEG YCbCr

À partir de Windows 8.1, Direct2D prend en charge le rendu des données d’image au format JPEG Y’CbCr. Les applications peuvent afficher le contenu JPEG dans sa représentation Y’CbCr Native au lieu de la décompresser dans BGRA. Cela peut réduire considérablement la consommation de mémoire graphique et l’heure de création des ressources. Pour plus d'informations, voir les rubriques suivantes :

-   [Effet YCbCr](ycbcr-effect.md) de Direct2D
-   Interface [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)

### <a name="support-for-block-compressed-formats-dds-files"></a>Prise en charge des formats compressés par blocs (fichiers DDS)

À partir de Windows 8.1, Direct2D assure la prise en charge des bitmaps qui contiennent les formats DXGI \_ \_ BC1 \_ UNORM, DXGI \_ format \_ BC2 \_ UNORM et dxgi BC3 UNORM \_ \_ \_ pixels. Les applications peuvent remplacer leurs ressources d’image par des images DDS compressées par blocs. Cela peut réduire considérablement la consommation de mémoire graphique et l’heure de création des ressources. Pour plus d'informations, voir les rubriques suivantes :

-   [**ID2D1DeviceContext :: CreateBitmapFromWicBitmap**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md) , méthode
-   Interface [**IWICDdsFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode)

### <a name="rendering-priority"></a>Priorité de rendu

À partir de Windows 8.1, Direct2D assure la prise en charge de la priorité de rendu par appareil. Cette nouvelle fonctionnalité permet aux applications de basculer un appareil entre une priorité de rendu normale (valeur par défaut) et une priorité de rendu faible (dans laquelle l’appareil n’empêchera pas d’autres tâches de rendu sur le système). Il est recommandé que les applications utilisent une priorité de rendu faible pour les tâches qui ne sont pas critiques pour la réactivité de l’utilisateur, telles que le contenu de prérendu, le rendu, et les autres opérations généralement effectuées en arrière-plan. Pour plus d'informations, voir les rubriques suivantes :

-   [**ID2D1Device1 :: SetRenderingPriority**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1device1-setrenderingpriority) , méthode
-   [**D2d1 \_ \_**](/windows/desktop/api/D2D1_2/ne-d2d1_2-d2d1_rendering_priority) Énumération des priorités de rendu

## <a name="whats-new-for-windows-8"></a>Nouveautés de Windows 8

Les fonctionnalités et les API suivantes ont été ajoutées ou mises à jour pour Windows 8.

Les nouvelles interfaces Direct2D sont prises en charge sur Windows 7 avec la [mise à jour de plateforme pour Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7) installée.

La sémantique Direct2d pour les appareils et les contextes de périphérique a été mise à jour pour ressembler plus précisément à la sémantique utilisée par Direct3D et pour fournir une opération concise sur les applications du Windows Store. Pour plus d’informations, consultez [contextes d’appareils et](devices-and-device-contexts.md) de périphériques.

API associées sélectionnées :

-   [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)
-   [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)

L’API de liste de commandes vous permet de partager le chemin de rendu pour l’impression et le rendu à l’écran. Elle vous permet également d’utiliser des primitives pour créer un pinceau d’image afin de remplir des primitives.

API associées sélectionnées :

-   [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)
-   [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)
-   [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush)

[Direct2D Effects](effects-overview.md) est un ensemble d’API, nouveauté de Windows 8, qui permet d’appliquer des effets de haute qualité aux images. Il comprend également des API qui vous permettent de créer vos propres effets personnalisés.

API associées sélectionnées :

-   [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
-   [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl)
-   [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext)

À compter de Windows 8, Direct2D comprend des API supplémentaires pour la création d’applications multithread. Pour plus d’informations, consultez [applications Direct2D multithread](multi-threaded-direct2d-apps.md) .

API associées sélectionnées :

-   [**ID2D1MultiThread**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1multithread)
-   [**\_Type de \_ fabrique \_ d2d1 \_ multithread**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type)

 

 