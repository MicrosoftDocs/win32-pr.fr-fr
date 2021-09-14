---
title: Effet de mappage de déplacement
description: Utilisez l’effet de mappage de déplacement pour déplacer les pixels de l’image d’entrée selon les valeurs d’intensité d’une deuxième image d’entrée.
ms.assetid: 07AA64B1-B570-428E-924F-D7DF3E4DB3F8
keywords:
- effet de mappage de déplacement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ad2deb0c584ccc9c55faebd60f803d66efa42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113269"
---
# <a name="displacement-map-effect"></a>Effet de mappage de déplacement

Utilisez l’effet de mappage de déplacement pour déplacer les pixels de l’image d’entrée selon les valeurs d’intensité d’une deuxième image d’entrée.

Le CLSID de cet effet est CLSID \_ D2D1DisplacementMap.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Canaux de couleur](#color-channels)
-   [Bitmap de sortie](#output-bitmap)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image



| Avant                                                           |
|------------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)       |
| After                                                            |
| ![image après la transformation.](images/19-displacementmap.png) |



 


```C++
ComPtr<ID2D1Effect> displacementMapEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DisplacementMap, &displacementMapEffect);

displacementMapEffect->SetInput(0, bitmap);
displacementMapEffect->SetValue(D2D1_DISPLACEMENTMAP_PROP_SCALE, 100.0f);

// The second input of the displacement effect determines how the input image is transformed.
// For this example, we will use a turbulence effect as the second input to randomly distort the image.
ComPtr<ID2D1Effect> turbulenceEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Turbulence, &turbulenceEffect);
displacementMapEffect->SetInputEffect(1, turbulenceEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(displacementMapEffect.Get());
m_d2dContext->EndDraw();
```



Les emplacements des pixels de la sortie sont déterminés à l’aide de la formule suivante :

C' (x, y) = C (x + Scale \* (XChannelSelector (bitmap de déplacement (x, y))-0.5), o + Scale \* (YChannelSelector (bitmap de déplacement (x, y))-0,5))

Où :<dl> *C (x, y)* est le pixel de sortie à (x, y).  
*C (x, y)* est le pixel d’entrée à (x, y).  
*Bitmap de déplacement (x, y)* est l’intensité de pixel de déplacement aux coordonnées spécifiées  
*XChannelSelector* l’intensité du canal RVBA sélectionné à partir de l’image bitmap de déplacement qui place l’image d’entrée dans l’axe X.  
*YChannelSelector* l’intensité du canal RVBA sélectionné à partir de l’image bitmap de déplacement qui place l’image d’entrée dans l’axe Y.  
</dl>

L’effet rééchantillonne l’image d’entrée en fonction de la propriété Scale et de l’intensité de l’image de déplacement. Il utilise l’interpolation bilinéaire en cas d’échantillonnage entre les pixels de l’image d’entrée.

Cet effet fonctionne sur les images alpha directes et prémultipliées. Le format alpha de sortie est le même que le format d’entrée.

## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                                   | Type et valeur par défaut                                                   | Description                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Scale<br/> \_Échelle d2d1 DISPLACEMENTMAP \_ prop \_<br/>                       | FLOAT<br/> 0.0f<br/>                                         | Multiplie l’intensité du canal sélectionné à partir de l’image de déplacement. Plus vous définissez cette propriété, plus l’effet déplace les pixels<br/>                       |
| XChannelSelect<br/> D2D1 \_ DISPLACEMENTMAP \_ prop \_ X \_ canal \_ Select<br/> | \_Sélecteur de canal d2d1 \_<br/> \_ \_ Sélecteur de canal d2d1 \_ A<br/> | L’effet extrait l’intensité de ce canal de couleur et l’utilise pour déplacer spatialement l’image dans la direction X. Pour plus d’informations, consultez [canaux de couleurs](#color-channels) .<br/> |
| YChannelSelect<br/> D2D1 \_ DISPLACEMENTMAP \_ prop \_ Y \_ canal \_ Select<br/> | \_Sélecteur de canal d2d1 \_<br/> \_ \_ Sélecteur de canal d2d1 \_ A<br/> | L’effet extrait l’intensité de ce canal de couleur et l’utilise pour déplacer spatialement l’image dans la direction Y. Pour plus d’informations, consultez [canaux de couleurs](#color-channels) .<br/> |



 

## <a name="color-channels"></a>Canaux de couleur



| Énumération                | Description                                                      |
|----------------------------|------------------------------------------------------------------|
| \_Sélecteur de canal d2d1 \_ \_ R | L’effet extrait la sortie d’intensité à partir du canal rouge.   |
| \_Sélecteur de canal d2d1 \_ \_ G | L’effet extrait la sortie d’intensité à partir du canal vert. |
| \_Sélecteur de canal d2d1 \_ \_ B | L’effet extrait la sortie d’intensité à partir du canal bleu.  |
| \_ \_ Sélecteur de canal d2d1 \_ A | L’effet extrait la sortie d’intensité à partir du canal alpha. |



 

## <a name="output-bitmap"></a>Bitmap de sortie

Vous pouvez déterminer la taille maximale de l’image bitmap de sortie avec les équations suivantes :

Bitmap de sortie ? Pixels = (taille de l’image bitmap en entrée ? ( DIP) + échelle) \* (dpi utilisateur/96)

Bitmap de sortie<sub>y</sub> pixels = (taille de la bitmap d’entrée<sub>y</sub>(DIP) + échelle) \* (dpi utilisateur/96)

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 Windows les applications du windows \[ \| Store\] |
| Serveur minimal pris en charge | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 Windows les applications du windows \[ \| Store\] |
| En-tête                   | d2d1effects. h                                                                      |
| Bibliothèque                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

