---
title: Présentation des pinceaux
description: Décrit les différents types de pinceaux fournis par Direct2D.
ms.assetid: 7a31d9e7-0521-40ee-b2c1-592dfaf5301e
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 7c8b4c4762a03650f150a74d3207d12767e1fb4e
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104383207"
---
# <a name="brushes-overview"></a>Présentation des pinceaux

Cette vue d’ensemble décrit comment créer et utiliser des objets [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)et [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) pour peindre des zones avec des couleurs unies, des dégradés et des bitmaps. Elle contient les sections suivantes.

## <a name="prerequisites"></a>Prérequis

Cette vue d’ensemble suppose que vous êtes familiarisé avec la structure d’une application Direct2D de base, comme décrit dans [création d’une application Direct2d simple](direct2d-quickstart.md).

## <a name="brush-types"></a>Types de pinceau

Un pinceau « peint » une zone avec sa sortie. Des pinceaux différents ont différents types de sortie. Direct2D fournit quatre types de pinceau : [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) peint une zone avec une couleur unie, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) avec un dégradé linéaire, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) avec un dégradé radial et [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) avec une bitmap.

> [!NOTE]  
> À compter de Windows 8, vous pouvez également utiliser [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush), qui est similaire à un pinceau bitmap, mais vous pouvez également utiliser des primitives.

Tous les pinceaux héritent de [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) et partagent un ensemble de fonctionnalités communes (définition et obtention d’opacité, et transformation de pinceaux). ils sont créés par [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) et sont des ressources dépendantes de l’appareil : votre application doit créer des pinceaux après avoir initialisé la cible de rendu avec laquelle les pinceaux seront utilisés, puis recréer les pinceaux chaque fois que la cible de rendu doit être recréée. (Pour plus d’informations sur les ressources, consultez [vue d’ensemble des ressources](resources-and-resource-domains.md).)

L’illustration suivante montre des exemples de chacun des différents types de pinceau.

![illustration des effets visuels à partir des pinceaux de couleur unie, des pinceaux de dégradé linéaires, des pinceaux de dégradé radiaux et des pinceaux bitmap](images/brushes-ovw-brushes.png)

## <a name="color-basics"></a>Notions de base des couleurs

Avant de peindre avec un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) ou un pinceau de dégradé, vous devez choisir des couleurs. Dans Direct2D, les couleurs sont représentées par la structure de [**\_ couleur d2d1 \_ F**](d2d1-color-f.md) (qui est en fait un nouveau nom pour la structure utilisée par Direct3D, [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)).

Avant Windows 8, [**d2d1 \_ Color \_ F**](d2d1-color-f.md) utilise l’encodage sRVB. l’encodage sRVB divise les couleurs en quatre composants : rouge, vert, bleu et alpha. Chaque composant est représenté par une valeur de virgule flottante comprise dans une plage standard de 0 à 1. La valeur 0 indique l’absence complète de cette couleur, tandis que la valeur 1 indique que cette couleur est entièrement présente. Pour le composant alpha, 0 représente une couleur totalement transparente, et 1 une couleur totalement opaque.

À partir de Windows 8, [**d2d1 \_ Color \_ F**](d2d1-color-f.md) accepte également l’encodage ScRVB. ScRVB est un sur-ensemble de qui autorise les valeurs de couleur supérieures à 1,0 et inférieures à 0,0.

Pour définir une couleur, vous pouvez utiliser la structure de [**\_ couleur d2d1 \_ F**](d2d1-color-f.md) et initialiser les champs vous-même, ou vous pouvez utiliser la classe [**d2d1 :: ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) pour vous aider à créer la couleur. La classe **ColorF** fournit plusieurs constructeurs pour définir des couleurs. Si la valeur alpha n’est pas spécifiée dans les constructeurs, la valeur par défaut est 1,0.

-   Utilisez le constructeur [**ColorF (enum, float)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) pour spécifier une couleur prédéfinie et une valeur de canal alpha. Une valeur de canal alpha est comprise entre 0,0 et 1,0, où 0,0 représente une couleur entièrement transparente et 1,0 représente une couleur entièrement opaque. L’illustration suivante montre plusieurs couleurs prédéfinies et leurs équivalents hexadécimaux. Pour obtenir la liste complète des couleurs prédéfinies, consultez la section constantes de couleur de la classe [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .

    ![illustration des couleurs prédéfinies](images/brushes-ovw-colors.png)

    L’exemple suivant crée une couleur prédéfinie et l’utilise pour spécifier la couleur d’un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).

```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```

-   Utilisez le constructeur [**ColorF (float, float, float, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) pour spécifier une couleur dans l’ordre des rouge, vert, bleu et alpha, où chaque élément a une valeur comprise entre 0,0 et 1,0.

    L’exemple suivant spécifie les valeurs rouge, vert, bleu et alpha pour une couleur.

```C++
    ID2D1SolidColorBrush *pGridBrush = NULL;
    hr = pCompatibleRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
        &pGridBrush
        );
```

-   Utilisez le constructeur [**ColorF (UInt32, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) pour spécifier la valeur hexadécimale d’une couleur et une valeur alpha, comme indiqué dans l’exemple suivant.
```C++
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
```

### <a name="alpha-modes"></a>Modes alpha

Quel que soit le mode Alpha de la cible de rendu avec lequel vous utilisez un pinceau, les valeurs de [**\_ couleur d2d1 \_ F**](d2d1-color-f.md) sont toujours interprétées comme des valeurs alpha directes.

## <a name="using-solid-color-brushes"></a>Utilisation de pinceaux de couleur unie

Pour créer un pinceau de couleur unie, appelez la méthode [**ID2D1RenderTarget :: CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) , qui retourne un HRESULT et un objet [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) . L’illustration suivante montre un carré qui est rayé avec un pinceau de couleur noir et peint avec un pinceau de couleur unie qui a la valeur de couleur de 0x9ACD32.

![illustration d’un carré peint avec un pinceau de couleur unie](images/brushes-ovw-solidcolor.png)

Le code suivant montre comment créer et utiliser un pinceau de couleur noire et un pinceau avec une valeur de couleur de 0x9ACD32 pour remplir et dessiner ce carré.


```C++
    ID2D1SolidColorBrush *m_pBlackBrush;
    ID2D1SolidColorBrush *m_pYellowGreenBrush;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
        &m_pBlackBrush
        );
}

// Create a solid color brush with its rgb value 0x9ACD32.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
}
```




```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
```



Contrairement à d’autres pinceaux, la création d’un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) est une opération relativement peu coûteuse. Vous pouvez créer des objets **ID2D1SolidColorBrush** chaque fois que vous affichez avec un faible impact sur les performances. Cette approche n’est pas recommandée pour les pinceaux de dégradé ou de bitmap.

## <a name="using-linear-gradient-brushes"></a>Utilisation de pinceaux de dégradé linéaire

Un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) peint une zone avec un dégradé linéaire défini le long d’une ligne, l’axe du dégradé. Vous spécifiez les couleurs du dégradé et leur emplacement le long de l’axe du dégradé à l’aide des objets [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) . Vous pouvez également modifier l’axe du dégradé, ce qui vous permet de créer des dégradés horizontaux et verticaux et d’inverser le sens du dégradé. Pour créer un pinceau de dégradé linéaire, appelez la méthode [**ID2D1RenderTarget :: CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) .

L’illustration suivante montre un carré qui est peint avec un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) avec deux couleurs prédéfinies, « jaune » et « ForestGreen ».

![illustration d’un carré peint avec un pinceau de dégradé linéaire jaune et de forêt vert](images/brushes-ovw-lineargradient.png)

Pour créer le dégradé présenté dans l’illustration précédente, procédez comme suit :

1.  Déclarez deux objets [**d2d1 \_ \_ Stop gradient**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) . Chaque point de dégradé spécifie une couleur et une position. Une position de 0,0 indique le début du dégradé, tandis qu’une position de 1,0 indique la fin du dégradé.

    Le code suivant crée un tableau de deux [**objets \_ d2d1 \_ Stop gradient**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) . La première étape spécifie la couleur « jaune » à la position 0, tandis que la deuxième Stop spécifie la couleur « ForestGreen » à la position 1.

```C++
    // Create an array of gradient stops to put in the gradient stop
    // collection that will be used in the gradient brush.
    ID2D1GradientStopCollection *pGradientStops = NULL;

    D2D1_GRADIENT_STOP gradientStops[2];
    gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
    gradientStops[0].position = 0.0f;
    gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
    gradientStops[1].position = 1.0f;
```

    

2.  Créez un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection). L’exemple suivant appelle [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)), en passant le tableau d’objets [**d2d1 \_ gradient \_ Stop**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) , le nombre de points de dégradé (2), le [**\_ gamma d2d1 \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) pour l’interpolation et le [**\_ \_ mode \_ d’extension d2d1**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) pour le mode Extend.

```C++
    // Create the ID2D1GradientStopCollection from a previously
    // declared array of D2D1_GRADIENT_STOP structs.
    hr = m_pRenderTarget->CreateGradientStopCollection(
        gradientStops,
        2,
        D2D1_GAMMA_2_2,
        D2D1_EXTEND_MODE_CLAMP,
        &pGradientStops
        );
```

    

3.  Créez le [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush). L’exemple suivant appelle la méthode [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) et lui transmet les propriétés de pinceau de dégradé linéaire qui contiennent le point de départ à (0, 0) et le point de terminaison à (150, 150), et les points de dégradé créés à l’étape précédente.
```C++
    // The line that determines the direction of the gradient starts at
    // the upper-left corner of the square and ends at the lower-right corner.

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(0, 0),
                D2D1::Point2F(150, 150)),
            pGradientStops,
            &m_pLinearGradientBrush
            );
    }
```

    

4.  Utilisez [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush). L’exemple de code suivant utilise le pinceau pour remplissage du un rectangle.
```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
```

    

## <a name="more-about-gradient-stops"></a>En savoir plus sur les arrêts de dégradé

Le [**\_ \_ point de dégradé d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) est le bloc de construction de base d’un pinceau de dégradé. Un point de dégradé spécifie la couleur et la position le long de l’axe du dégradé. La valeur de la position du dégradé est comprise entre 0,0 et 1,0. Plus il est proche de 0,0, plus la couleur est proche du début du dégradé. plus la valeur est proche de 1,0, plus la couleur est proche de la fin du dégradé.

L’illustration suivante met en évidence les points de dégradé. Le cercle marque la position des points de dégradé et une ligne en pointillés affiche l’axe du dégradé.

![illustration d’un pinceau de dégradé linéaire avec quatre arrêts le long de l’axe](images/4stoplineargradient.png)

Le premier point de dégradé spécifie la couleur jaune à une position de 0,0. Le deuxième point de dégradé spécifie la couleur rouge à une position de 0,25. De la gauche vers la droite le long de l’axe du dégradé, les couleurs entre ces deux arrêts passent progressivement du jaune au rouge. Le troisième point de dégradé spécifie la couleur bleue à une position de 0,75. Les couleurs entre les deuxième et troisième points de dégradé passent progressivement du rouge au bleu. Le quatrième point de dégradé spécifie vert citron vert à une position de 1,0. Les couleurs entre les troisième et quatrième points de dégradé passent progressivement du bleu au vert citron.

## <a name="the-gradient-axis"></a>Axe du dégradé

Comme mentionné précédemment, les points de dégradé d’un pinceau de dégradé linéaire sont positionnés le long d’une ligne, l’axe du dégradé. Vous pouvez spécifier l’orientation et la taille de la ligne à l’aide des champs **StartPoint** et **Endpoint** de la structure de [**Propriétés de \_ \_ \_ pinceau \_ de dégradé linéaire d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) lorsque vous créez un pinceau de dégradé linéaire. Une fois que vous avez créé un pinceau, vous pouvez ajuster l’axe du dégradé en appelant les méthodes [**SetStartPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) et [**SetEndPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) du pinceau. En manipulant le point de départ et le point de terminaison du pinceau, vous pouvez créer des dégradés horizontaux et verticaux, inverser le sens du dégradé et bien plus encore.

Par exemple, dans l’illustration suivante, le point de départ est défini sur (0, 0) et le point de terminaison sur (150, 50); Cela crée un dégradé Diagonal qui commence à l’angle supérieur gauche et s’étend jusqu’au coin inférieur droit de la zone qui est peinte. Lorsque vous définissez le point de départ sur (0, 25) et le point de terminaison sur (150, 25), un dégradé horizontal est créé. De même, la définition du point de départ sur (75, 0) et le point de terminaison sur (75, 50) crée un dégradé vertical. Le fait de définir le point de départ sur (0, 50) et le point de terminaison sur (150, 0) crée un dégradé Diagonal qui commence dans le coin inférieur gauche et s’étend jusqu’au coin supérieur droit de la zone qui est peinte.

![illustration de quatre axes de dégradé différents dans le même rectangle](images/linear-gradients.png)

## <a name="using-radial-gradient-brushes"></a>Utilisation de pinceaux de dégradé radiaux

Contrairement à un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), qui fusionne deux couleurs ou plus sur un axe de dégradé, un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) peint une zone avec un dégradé radial qui fusionne deux couleurs ou plus sur une ellipse. Tandis qu’un **ID2D1LinearGradientBrush** définit son axe de dégradé avec un point de départ et un point de terminaison, un **ID2D1RadialGradientBrush** définit son ellipse de dégradé en spécifiant un rayon centré, horizontal et vertical, ainsi qu’un décalage de l’origine du dégradé.

À l’instar d’un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) utilise un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) pour spécifier les couleurs et les positions dans le dégradé.

L’illustration suivante montre un cercle peint avec un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush). Le cercle comporte deux points de dégradé : le premier spécifie une couleur prédéfinie « jaune » à la position 0,0 et le second spécifie une couleur prédéfinie « ForestGreen » à une position de 1,0. Le dégradé a un centre de (75, 75), un décalage d’origine du dégradé (0, 0) et un rayon x et y de 75.

![illustration d’un cercle peint avec un pinceau dégradé radial](images/brushes-ovw-radials.png)

Les exemples de code suivants montrent comment peindre ce cercle avec un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) qui a deux arrêts de couleur : « jaune » à une position de 0,0 et « ForestGreen » à une position de 1,0. Comme pour la création d’un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), l’exemple appelle [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) pour créer un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) à partir d’un tableau de points de dégradé.


```C++
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );
```



Pour créer un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), utilisez la méthode [**ID2D1RenderTarget :: CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) . **CreateRadialGradientBrush** prend trois paramètres. Le premier paramètre, les [**\_ Propriétés de \_ \_ pinceau \_ de dégradé radial d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) spécifie le centre, le décalage d’origine du dégradé et les rayons horizontaux et verticaux du dégradé. Le deuxième paramètre est un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) qui décrit les couleurs et leurs positions dans le dégradé, tandis que le troisième paramètre est l’adresse du pointeur qui reçoit la nouvelle référence **ID2D1RadialGradientBrush** . Certaines surcharges prennent un paramètre supplémentaire, une structure de [**\_ \_ Propriétés de pinceau d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) qui spécifie une valeur d’opacité et une transformation à appliquer au nouveau pinceau.

L’exemple suivant appelle [**CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush), en passant le tableau de points de dégradé et les propriétés de pinceau de dégradé radial dont la valeur *Center* est définie sur (75, 75), le *gradientOriginOffset* défini sur (0, 0) *et* *RadiusX et RadiusY* ont tous les deux la valeur 75.


```C++
// The center of the gradient is in the center of the box.
// The gradient origin offset was set to zero(0, 0) or center in this case.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateRadialGradientBrush(
        D2D1::RadialGradientBrushProperties(
            D2D1::Point2F(75, 75),
            D2D1::Point2F(0, 0),
            75,
            75),
        pGradientStops,
        &m_pRadialGradientBrush
        );
}
```



L’exemple final utilise le pinceau pour remplir une ellipse.


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
```



### <a name="configuring-a-radial-gradient"></a>Configuration d’un dégradé radial

Les valeurs différentes pour *Center*, *gradientOriginOffset*, *RadiusX* et/ou *RadiusY* produisent différents dégradés. L’illustration suivante montre plusieurs dégradés radiaux qui ont des décalages d’origine du dégradé différents, créant ainsi l’apparence de la lumière éclairant les cercles à partir de différents angles.

![illustration du même cercle peint avec des pinceaux de dégradé radiaux avec des décalages d’origine différents](images/radialgradient.png)

## <a name="using-bitmap-brushes"></a>Utilisation de pinceaux bitmap

Un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) peint une zone avec une image bitmap (représentée par un objet [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) ).

L’illustration suivante montre un carré peint avec une image bitmap d’une usine.

![illustration d’un carré peint avec une image bitmap de plante](images/brushes-ovw-bitmap.png)

Les exemples qui suivent montrent comment peindre ce carré avec un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).

Le premier exemple Initialise un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) à utiliser avec le pinceau. Le **ID2D1Bitmap** est fourni par une méthode d’assistance, LoadResourceBitmap, définie ailleurs dans l’exemple.


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
}
```



Pour créer le pinceau bitmap, appelez la méthode [**ID2D1RenderTarget :: CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) et spécifiez le [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) à peindre. La méthode retourne un **HRESULT** et un objet [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) . Certaines surcharges de **CreateBitmapBrush** vous permettent de spécifier des options supplémentaires en acceptant des [**\_ \_ Propriétés de pinceau d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) et une structure de [**Propriétés de \_ \_ pinceau \_ de bitmap d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) .


```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}
```



L’exemple suivant utilise le pinceau pour remplir un rectangle.


```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pBitmapBrush);
```



## <a name="configuring-extend-modes"></a>Configuration des modes d’extension

Parfois, le dégradé d’un pinceau de dégradé ou de l’image bitmap pour un pinceau bitmap ne remplit pas complètement la zone qui est peinte.

-   Lorsque cela se produit pour un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), Direct2D utilise les paramètres du mode d’extension horizontal ([**SetExtendModeX**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)) et vertical ([**SetExtendModeY**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)) du pinceau pour déterminer comment remplir la zone restante.

-   Lorsque cela se produit pour un pinceau de dégradé, Direct2D détermine comment remplir la zone restante à l’aide de la valeur du paramètre du [**\_ \_ mode d’extension d2d1**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) que vous avez spécifié quand vous avez appelé le [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) pour créer le [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)du pinceau de dégradé.

L’illustration suivante montre les résultats de chaque combinaison possible des modes d’extension pour un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush): [**d2d1 \_ \_ en mode \_ extension**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) (clamp), **d2d1 \_ mode d’extension \_ \_ Wrap** (Wrap) et **d2d1 \_ étendre le \_ miroir** (miroir).

![illustration d’une image d’origine et des images obtenues à partir de différents modes d’extension](images/bitmapwrap-clamp-mirror.png)

L’exemple suivant montre comment définir les modes d’extension x et y du pinceau bitmap sur [**d2d1 étendre le \_ \_ miroir**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode). Il peint ensuite le rectangle avec le [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).


```C++
m_pBitmapBrush->SetExtendModeX(D2D1_EXTEND_MODE_MIRROR);
m_pBitmapBrush->SetExtendModeY(D2D1_EXTEND_MODE_MIRROR);

m_pRenderTarget->FillRectangle(exampleRectangle, m_pBitmapBrush);
```



Il produit une sortie comme indiqué dans l’illustration suivante.

![illustration d’une image d’origine et de l’image résultante après la mise en miroir de l’axe x et de l’axe y](images/brushes-ovw-bitmapmirrormirror.png)

## <a name="transforming-brushes"></a>Transformer des pinceaux

Quand vous peignez avec un pinceau, il peint l’espace de coordonnées de la cible de rendu. Les pinceaux ne se positionnent pas automatiquement pour s’aligner avec l’objet qui est peint ; par défaut, ils commencent à peindre à l’origine (0,0) de la cible de rendu.

Vous pouvez « déplacer » le dégradé défini par un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) vers une zone cible en définissant son point de départ et son point de terminaison. De même, vous pouvez déplacer le dégradé défini par un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) en modifiant son centre et ses rayons.

Pour aligner le contenu d’un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) sur la zone qui est peinte, vous pouvez utiliser la méthode [**setTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) pour convertir l’image bitmap à l’emplacement souhaité. Cette transformation affecte uniquement le pinceau ; elle n’affecte pas les autres contenus dessinés par la cible de rendu.

Les illustrations suivantes montrent l’effet de l’utilisation d’un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) pour remplir un rectangle situé à l’emplacement (100, 100). L’illustration de l’illustration de gauche montre le résultat du remplissage du rectangle sans transformer le pinceau : le bitmap est dessiné à l’origine de la cible de rendu. Par conséquent, seule une partie de la bitmap apparaît dans le rectangle. L’illustration à droite montre le résultat de la transformation du **ID2D1BitmapBrush** afin que son contenu soit décalé de 50 pixels vers la droite et de 50 pixels vers le dessous. Le bitmap remplit maintenant le rectangle.

![illustration d’un carré peint avec un pinceau bitmap sans transformer le pinceau et en transformant le pinceau](images/brushes-ovw-transform.png)

Le code suivant montre comment effectuer cette procédure. Tout d’abord, appliquez une translation à la [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), en déplaçant le pinceau 50 pixels vers la droite le long de l’axe x et 50 pixels vers le côté de l’axe y. Utilisez ensuite le **ID2D1BitmapBrush** pour remplir le rectangle qui a l’angle supérieur gauche à (100, 100) et le coin inférieur droit à (200, 200).


```cpp
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
   
}

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}

D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);

// Demonstrate the effect of transforming a bitmap brush.
m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

// To see the content of the rcTransformedBrushRect, comment
// out this statement.
m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

m_pRenderTarget->DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```

## <a name="related-topics"></a>Rubriques connexes

* [Référence Direct2D](reference.md)
* [Comment créer un pinceau de couleur unie](how-to-create-a-solid-color-brush.md)
* [Comment créer un pinceau de dégradé linéaire](how-to-create-a-linear-gradient-brush.md)
* [Comment créer un pinceau de dégradé radial](how-to-create-a-radial-gradient-brush.md)
* [Comment créer un pinceau bitmap](how-to-create-a-bitmap-brush.md)
