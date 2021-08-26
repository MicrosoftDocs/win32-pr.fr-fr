---
title: Effet de compensation DPI
description: Utilisez l’effet compensation DPI pour ajuster automatiquement une image bitmap d’entrée afin qu’elle corresponde à la valeur PPP du contexte. Cela est utile dans les situations où une image bitmap est créée ou chargée à une résolution différente de celle de l’écran.
ms.assetid: EA8AD89B-A710-468F-A6F3-474DA29586F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38f1390825087cabb9ee1bec65f2708990757ff25f08e71140be5be0fc6ae11e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967112"
---
# <a name="dpi-compensation-effect"></a>Effet de compensation DPI

Utilisez l’effet compensation DPI pour ajuster automatiquement une image bitmap d’entrée afin qu’elle corresponde à la valeur PPP du contexte. Cela est utile dans les situations où une image bitmap est créée ou chargée à une résolution différente de celle de l’écran.

Le CLSID de cet effet est CLSID \_ D2D1DpiCompensation.

## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                                       | Description                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InterpolationMode<br/> \_Mode d’interpolation d2d1 DPICOMPENSATION \_ prop \_ \_<br/> | Mode d’interpolation utilisé par l’effet pour mettre l’image à l’échelle.<br/> Le type est D2D1 \_ DPICOMPENSATION \_ interpolation \_ mode.<br/> La valeur par défaut est D2D1 \_ DPICOMPENSATION \_ interpolation \_ mode \_ Linear.<br/>                  |
| BorderMode<br/> \_Mode de bordure d2d1 DPICOMPENSATION \_ prop \_ \_<br/>               | Le mode utilisé pour calculer la bordure de l’image, soft ou Hard. Pour plus d’informations, consultez [modes de bordure](https://www.bing.com/search?q=Border+modes) . <br/> Le type est D2D1 \_ Border \_ mode.<br/> La valeur par défaut est \_ d2d1 \_ en mode bordure \_ souple.<br/> |
| InputDpi<br/> D2D1 \_ DPICOMPENSATION \_ prop \_ entrée \_ PPP<br/>                   | PPP de l’image d’entrée.<br/> Le type est FLOAT.<br/> La valeur par défaut est 96.0 f.<br/>                                                                                                                                    |



 

## <a name="interpolation-modes"></a>Modes d’interpolation



| Énumération                                                       | Description                                                                                                                                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Mode d’interpolation d2d1 DPICOMPENSATION \_ \_ \_ le plus proche \_ voisin     | Échantillonne le point unique le plus proche et l’utilise. Ce mode utilise moins de temps de traitement, mais génère l’image de qualité la plus faible.                                                                           |
| D2D1 \_ \_ mode d’interpolation \_ DPICOMPENSATION \_ linéaire                | Utilise un échantillon à quatre points et une interpolation linéaire. Ce mode utilise plus de temps de traitement que le mode voisin le plus proche, mais génère une image de qualité supérieure.                                           |
| D2D1 \_ DPICOMPENSATION \_ mode d' \_ interpolation \_ cubique                 | Utilise un exemple de noyau cubique 16 pour l’interpolation. Ce mode utilise le plus de temps de traitement, mais génère une image de qualité supérieure.                                                                        |
| \_Mode d’interpolation d2d1 DPICOMPENSATION multi- \_ \_ \_ \_ exemple \_ linéaire | Utilise 4 échantillons linéaires au sein d’un même pixel pour une bonne anticrénelage. Ce mode est adapté à la réduction de la taille des images avec quelques pixels.                                              |
| D2D1 \_ \_ mode d’interpolation \_ DPICOMPENSATION \_ anisotrope           | Utilise le filtrage anisotrope pour échantillonner un modèle en fonction de la forme transformée de l’image bitmap.                                                                                                     |
| D2D1 \_ DPICOMPENSATION \_ mode d’interpolation de \_ \_ haute \_ qualité \_ cubique  | Utilise un noyau cubique de haute qualité variable pour effectuer une pré-réduire de l’image si downscaling est impliqué dans la matrice de transformation. Utilise ensuite le mode d’interpolation cubique pour la sortie finale. |



 

> [!Note]  
> Si vous ne sélectionnez pas de mode, l’effet par défaut est D2D1 \_ DPICOMPENSTION \_ interpolation \_ mode \_ Linear.

 

## <a name="border-modes"></a>Modes de bordure



| Nom                     | Description                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| \_Mode de bordure d2d1 \_ \_ | Les pixels en dehors des limites d’entrée sont générés par l' [effet de bordure de miroir](border.md). <br/> |
| D2D1 \_ mode de bordure \_ \_ difficile | Les pixels en dehors des limites d’entrée sont des noirs transparents.<br/>                                    |



 

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

 

