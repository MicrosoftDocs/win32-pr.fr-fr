---
title: Effet de rognage
description: Utilisez l’effet rognage pour sortir une région spécifiée d’une image.
ms.assetid: DFB7DE20-F202-4E7F-AE63-94BF817B6E30
keywords:
- effet de rognage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 653ceaf4cf8b5922fe05e151c1639269f3169b57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843533"
---
# <a name="crop-effect"></a>Effet de rognage

Utilisez l’effet rognage pour sortir une région spécifiée d’une image.

Le CLSID de cet effet est CLSID \_ D2D1Crop.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Bitmap de sortie](#output-bitmap)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image



| Avant                                                     |
|------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg) |
| After                                                      |
| ![image après la transformation.](images/8-crop.png)       |



 


```C++
ComPtr<ID2D1Effect> cropEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Crop, &cropEffect);

cropEffect->SetInput(0, bitmap);
cropEffect->SetValue(D2D1_CROP_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(cropEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriétés d’effet



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nom complet et énumération d’index</th>
<th>Type et valeur par défaut</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Rect<br/></td>
<td>D2D1_VECTOR_4F<br/></td>
<td>Région à rogner spécifiée comme vecteur au format (gauche, haut, largeur, hauteur).<br/></td>
</tr>
<tr class="even">
<td>D2D1_CROP_PROP_RECT<br/></td>
<td>{-FLT_MAX,-FLT_MAX, FLT_MAX, FLT_MAX}<br/></td>
<td>Les unités sont en DIP. <br/>
<blockquote>
<p>[!Note]</p>
<p>Le Rect sera tronqué s’il chevauche les limites de bord de l’image d’entrée.<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>D2D1_CROP_PROP_BORDER_MODE<br/></td>
<td>D2D1_BORDER_MODE <br/> D2D1_BORDER_MODE_SOFT <br/></td>
<td><ul>
<li>D2D1_BORDER_MODE_SOFT : si le rectangle de rognage tombe sur des coordonnées de pixels fractionnaires, l’effet applique l’anticrénelage qui produit une bordure douce.</li>
<li>D2D1_BORDER_MODE_HARD : si le rectangle de rognage se trouve sur des coordonnées de pixels fractionnaires, il s’agit d’un effet de serre qui produit un bord dur.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="output-bitmap"></a>Bitmap de sortie

La sortie de cet effet est la taille de la propriété Rect. La longueur et la largeur sont calculées

ulated à l’aide des équations ici : <dl> Longueur de sortie en pixels = (Rect. Right-Rect. Left) \* (dpi/96 de l’utilisateur)  
Hauteur de sortie en pixels = (Rect. Bottom-Rect.Top) \* (dpi/96 de l’utilisateur)  
</dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge | Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\] |
| Serveur minimal pris en charge | Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\] |
| En-tête                   | d2d1effects. h                                                                      |
| Bibliothèque                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

