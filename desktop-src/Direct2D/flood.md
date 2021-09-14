---
title: Effet de flux
description: Utilisez l’effet de flux pour générer une image bitmap basée sur la couleur spécifiée et la valeur alpha. Vous pouvez utiliser cet effet lorsque vous souhaitez qu’une couleur spécifique soit une entrée pour un effet, comme une couleur d’arrière-plan.
ms.assetid: F80A6DC0-E18C-4324-BE4A-FE40C5722988
keywords:
- effet de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92d34a41c0913a0d250fc24467b37b0d347b4ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113230"
---
# <a name="flood-effect"></a>Effet de flux

Utilisez l’effet de flux pour générer une image bitmap basée sur la couleur spécifiée et la valeur alpha. Vous pouvez utiliser cet effet lorsque vous souhaitez qu’une couleur spécifique soit une entrée pour un effet, comme une couleur d’arrière-plan.

> [!Note]  
> L’effet passe le long de la valeur de couleur spécifiée comme spécifié. Vous devez prémultiplier manuellement les valeurs si vous envisagez de passer la sortie aux effets qui attendent une entrée prémultipliée.

 

Le CLSID de cet effet est CLSID \_ D2D1Flood.

L’effet de flux n’a aucune image d’entrée.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Bitmap de sortie](#output-bitmap)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

![exemple d’image de l’effet de saturation en vert.](images/20-flood.png)


```C++
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(0.0f, 1.0f, 0.0f, 1.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(floodEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                   | Description                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Couleur<br/> Couleur de la \_ prop d2d1 Flood \_ \_<br/> | Couleur et opacité de l’image bitmap. Cette propriété est un \_ vecteur d2d1 \_ 4F. Les valeurs individuelles de chaque canal sont de type flottant, illimité et sans unité. L’effet ne modifie pas les valeurs des canaux.<br/> Les valeurs RVBA pour chaque canal sont comprises entre 0 et 1.<br/> Le type est D2D1 \_ Vector \_ 4F.<br/> La valeur par défaut est {0.0 f, 0.0 f, 0.0 f, 1.0 f}.<br/> |



 

## <a name="output-bitmap"></a>Bitmap de sortie

Cet effet génère une image bitmap de taille infinie logiquement.

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

 

