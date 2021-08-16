---
title: Effet composite
description: Utilisez l’effet composite pour combiner 2 images ou plus. Cet effet a 13 modes composites différents.
ms.assetid: 60b878e9-1bc6-40d4-ade3-4bbd5c822c55
keywords:
- effet composite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8cf326e5d0bfb33b3dc927ba7366eb6d2b343a1a50db462de58fac8ef648bef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826575"
---
# <a name="composite-effect"></a>Effet composite

Utilisez l’effet composite pour combiner 2 images ou plus. Cet effet a 13 modes composites différents. T

L’effet composite accepte au moins 2 entrées. Lorsque vous spécifiez 2 images, la destination est la première entrée (index 0) et la source est la deuxième entrée (index 1). Si vous spécifiez plus de 2 entrées, les images sont composées à partir de la première entrée, puis de la seconde, et ainsi de suite.

Cet effet implémente tous les modes à l’aide de l’unité de fusion de l’unité de traitement graphique (GPU).

Le CLSID de cet effet est CLSID \_ D2D1Composite.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Types de mode](#mode-types)
-   [Exemple de code](#sample-code)
-   [Requirements](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

L’image ici montre 2 rectangles arrondis de la même taille qui se chevauchent. Le rectangle bleu est la source et le rectangle rouge est la destination. Les images ont été composites avec le mode Source sur.

![exemple d’image indiquant 2 rectangles arrondis de la même taille qui se chevauchent à l’aide du mode Source sur.](images/composite-over.png)

Voici un autre exemple utilisant le mode par défaut.



| Avant image 1                                                          |
|-------------------------------------------------------------------------|
| ![première image source avant l’effet.](images/default-before.jpg) |
| Avant image 2                                                          |
| ![deuxième image avant l’effet.](images/3-composite(2of2).png)    |
| Après                                                                   |
| ![image après la transformation.](images/3-composite.png)               |



 


```C++
ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInput(0, bitmap);
compositeEffect->SetInput(1, bitmapTwo);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                     | Type et valeur par défaut                                                          | Description                   |
|--------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------|
| Mode<br/> \_Mode d2d1 composite \_ prop \_<br/> | D2D1 \_ mode composite \_<br/> \_ \_ Source en mode composite d2d1 \_ \_ sur<br/> | Mode utilisé pour l’effet. |



 

## <a name="mode-types"></a>Types de mode

Le tableau ci-dessous montre les modes de cet effet. Les équations figurant dans le tableau utilisent les éléments suivants :

-   O = sortie
-   S = source
-   SA = source alpha
-   D = destination
-   DA = alpha de destination



| Énumération                                  | Sommaire                          | Taille de la bitmap de sortie                                                                                      |
|----------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------|
| \_ \_ Source en mode composite d2d1 \_ \_ sur          | O = S + (1 SA) \* D             | Union des bitmaps sources et de destination                                                                 |
| \_Destination du mode composite d2d1 \_ \_ \_ sur     | O = (1 DA) \* S + D             | Union des bitmaps sources et de destination                                                                 |
| \_ \_ Source en mode composite d2d1 \_ \_ dans            | O = DA \* S                       | Intersection des bitmaps de source et de destination                                                          |
| \_ \_ Destination du mode composite d2d1 \_ \_ dans       | O = SA \* D                       | Intersection des bitmaps de source et de destination                                                          |
| \_ \_ Source en mode composite d2d1 \_ \_ out           | O = (1-DA) \* S                 | Région de la bitmap source                                                                             |
| D2D1 \_ \_ sortie de \_ destination en mode composite \_      | O = (1-SA) \* D                 | Région de la bitmap de destination                                                                        |
| D2D1 \_ \_ source en mode composite haut \_ \_          | O = DA \* S + (1-sa) \* D       | Région de la bitmap de destination                                                                        |
| D2D1 \_ de \_ destination en mode composite par- \_ \_ dessus     | O = (1-DA) \* S + sa \* D       | Région de la bitmap source                                                                             |
| D2D1 \_ mode composite \_ \_ Xor                   | O = (1-DA) \* S + (1-sa) \* D | Union des bitmaps sources et de destination                                                                 |
| D2D1 \_ mode composite \_ \_ plus                  | O = S + D                         | Union des bitmaps sources et de destination                                                                 |
| \_ \_ Copie source en mode COMPOSite d2d1 \_ \_          | O = S                             | Région de la bitmap source                                                                             |
| \_ \_ \_ Copie source délimitée en \_ mode composite d2d1 \_ | O = S (uniquement lorsque la source existe)  | Union des bitmaps sources et de destination. La destination n’est pas remplacée lorsque la source n’existe pas. |
| \_Masque d2d1 \_ mode composite \_ \_ inversé          | O = (1 D) \* S + (1 sa) \* D  | Union des bitmaps sources et de destination. Les valeurs alpha sont inchangées.                                 |



 

La figure ci-dessous montre un exemple de chacun des modes avec des images qui ont une opacité de 1,0 ou 0,5.

![exemple d’image de chacun des modes avec opacité défini sur 1,0 ou 0,5.](images/composite-types.png)

## <a name="sample-code"></a>Exemple de code

Pour obtenir un exemple de cet effet, téléchargez l' [exemple de modes d’effet composite de Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).

## <a name="requirements"></a>Configuration requise



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

 

