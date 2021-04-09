---
title: Effet morphologique
description: Utilisez l’effet morphologique pour les limites d’arête fine ou Epaissir dans une image.
ms.assetid: 4B3CFC51-D556-4729-B433-7307C80291F4
keywords:
- effets morphologiques
- effet d’Universion
- effet d’érosion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f43cf41810ae0b16c9bc96dd37473a0231fc132c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104728"
---
# <a name="morphology-effect"></a>Effet morphologique

Utilisez l’effet morphologique pour les limites d’arête fine ou Epaissir dans une image. Cet effet crée un noyau qui est de 2 fois la largeur et la hauteur que vous spécifiez. Cet effet centre le noyau sur le pixel qu’il calcule et retourne la valeur maximale dans le noyau (en cas de dilatation) ou la valeur minimale dans le noyau (en cas d’érosion).

Le CLSID de cet effet est CLSID \_ D2D1Morphology.

## <a name="example-images"></a>Exemples d’images

Cet exemple montre la sortie de l’effet lors de l’utilisation du mode ÉROD.



| Avant                                                     |
|------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg) |
| After                                                      |
| ![image après la transformation.](images/7-morphology.png) |



 


```C++
ComPtr<ID2D1Effect> morphologyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Morphology, &morphologyEffect);

morphologyEffect->SetInput(0, bitmap);

morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_MODE, D2D1_MORPHOLOGY_MODE_ERODE);
morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_WIDTH, 14);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(morphologyEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                          | Type et valeur par défaut                                                     | Description                                                                                                                                                       |
|-------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mode<br/> \_Mode d2d1 morphologique \_ prop \_<br/>     | \_Mode morphologique \_ d2d1<br/> \_Mode morphologique \_ d2d1 \_ ÉROD<br/> | Mode morphologique. Les modes disponibles sont ÉROD (aplatir) et dilate (Epaissir).<br/> Pour plus d’informations, consultez [modes morphologique](#morphology-modes) .<br/> |
| Largeur<br/> Largeur de la D2D1 de la \_ morphologie \_ \_<br/>   | UINT<br/> 1<br/>                                               | Taille du noyau sur l’axe X. Les unités sont en DIP. Les valeurs doivent être comprises entre 1 et 100 inclus.                                                         |
| Hauteur<br/> Hauteur de la D2D1 de la \_ morphologie \_ \_<br/> | UINT<br/> 1<br/>                                               | Taille du noyau sur l’axe Y. Les unités sont en DIP. Les valeurs doivent être comprises entre 1 et 100 inclus.                                                         |



 

## <a name="morphology-modes"></a>Modes morphologiques



| Nom                           | Description                                                    |
|--------------------------------|----------------------------------------------------------------|
| \_Mode morphologique \_ d2d1 \_ ÉROD  | La valeur maximale de chaque canal RVB dans le noyau est utilisée. |
| \_Mode morphologique d2d1 \_ en \_ retard | La valeur minimale de chaque canal RVB dans le noyau est utilisée. |



 

## <a name="output-bitmap"></a>Bitmap de sortie

Pour le mode de sortie, la taille de la bitmap de sortie augmente : 

| Condition requise | Valeur |
|--------------------------|-----------------------------------------|
| Croissance des bitmaps de sortie X = | INT (FLOAT (Width) \* ((dpi utilisateur)/96))  |
| Croissance de la bitmap de sortie Y = | INT (FLOAT (hauteur) \* ((dpi utilisateur)/96)) |



 

Pour le mode ÉROD, la taille de la bitmap de sortie diminue :

| Condition requise | Valeur |
|--------------------------|------------------------------------------|
| Croissance des bitmaps de sortie X = | INT (FLOAT (-Width) \* ((dpi utilisateur)/96))  |
| Croissance de la bitmap de sortie Y = | INT (FLOAT (-Height) \* ((dpi utilisateur)/96)) |



 

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

 

