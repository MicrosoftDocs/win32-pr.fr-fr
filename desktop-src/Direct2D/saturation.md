---
title: Effet de saturation
description: Utilisez cet effet pour modifier la saturation d’une image.
ms.assetid: 03A374D9-BED4-49ED-B90E-21193909C8AB
keywords:
- effet de saturation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6912e64c9297a3554b4785128e1282a3974d36
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112554"
---
# <a name="saturation-effect"></a>Effet de saturation

Utilisez cet effet pour modifier la saturation d’une image. L’effet de saturation est une spécialisation de l’effet de [matrice de couleurs](color-matrix.md) .

Le CLSID de cet effet est CLSID \_ D2D1Saturation.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

L’exemple ci-dessous montre les images d’entrée et de sortie de l’effet de saturation avec une saturation de 0%.



| Avant                                                      |
|-------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)  |
| After                                                       |
| ![image après la transformation.](images/16-saturation.png) |



 


```C++
ComPtr<ID2D1Effect> saturationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Saturation, &saturationEffect);

saturationEffect->SetInput(0, bitmap);

saturationEffect->SetValue(D2D1_SATURATION_PROP_SATURATION, 0.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(saturationEffect.Get());
m_d2dContext->EndDraw();
```



L’effet calcule une *matrice de couleurs* en fonction de la valeur de saturation (dans l’équation ici) que vous spécifiez avec la propriété saturation d2d1 \_ saturation \_ \_ . L’équation de matrice est présentée ici.

![formule permettant de calculer une matrice de saturation.](images/saturation-formula.png)

La matrice créée dépend uniquement de la valeur de saturation. Vous pouvez utiliser l’effet [matrice de couleurs](color-matrix.md) si vous avez besoin d’une matrice spécifique.

Cet effet consomme et génère des images alpha prémultipliées. L’effet ne fonctionne pas sur les images alpha directes, sauf si elles sont entièrement opaques.

## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                  | Type et valeur par défaut           | Description                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Saturation<br/> Saturation de la \_ saturation d2d1 \_ \_<br/> | FLOAT<br/> 0,5 f<br/> | Saturation de l’image. Vous pouvez définir la saturation sur une valeur comprise entre 0 et 1. Si vous lui affectez la valeur 1, l’image de sortie est entièrement saturée. Si vous lui affectez la valeur 0, l’image de sortie est monochrome. La valeur de saturation est sans unité. |



 

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

 

