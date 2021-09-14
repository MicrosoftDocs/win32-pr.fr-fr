---
title: Effet de source bitmap
description: Utilisez l’effet de source bitmap pour générer un ID2D1Image à partir d’un IWICBitmapSource pour une utilisation en tant qu’entrée dans un graphique d’effet.
ms.assetid: 86646111-208A-4E6D-A28C-7B23A1742D24
keywords:
- effet de source bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a439c94f0f520b318b3cb3511775dbec58b6e139
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114197"
---
# <a name="bitmap-source-effect"></a>Effet de source bitmap

Utilisez l’effet de source bitmap pour générer un [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) à partir d’un [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) pour une utilisation en tant qu’entrée dans un graphique d’effet. Cet effet effectue une mise à l’échelle et une rotation sur le processeur. Il peut également générer un mipmap de mémoire système, qui peut être une optimisation des performances pour la mise à l’échelle active des images très volumineuses à différentes résolutions réduites.

> [!Note]  
> L’effet de la source bitmap prend son entrée comme une propriété, et non comme une entrée d’image. Vous devez utiliser la méthode [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) , et non la méthode [**SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) . La propriété *WicBitmapSource* est l’emplacement où vous spécifiez les données d’entrée de l’image.

 

Le CLSID de cet effet est CLSID \_ D2D1BitmapSource.

-   [Propriétés d’effet](#effect-properties)
-   [Modes d’interpolation](#interpolation-modes)
-   [Orientation](#orientation)
-   [Modes alpha](#alpha-modes)
-   [Remarques](#remarks)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                                          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WicBitmapSource<br/> \_Source de bitmap d2d1 BITMAPSOURCE \_ prop \_ WIC \_ \_<br/>         | [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) contenant les données d’image à charger.<br/> Le type est [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource).<br/> La valeur par défaut est NULL.<br/>                                                                                                                                                                                                                   |
| Scale<br/> \_Échelle d2d1 BITMAPSOURCE \_ prop \_<br/>                                 | Le montant de l’échelle sur les directions X et Y. L’effet multiplie la largeur par la valeur X et la hauteur par la valeur Y. Cette propriété est un \_ vecteur d2d1 \_ 2F défini comme suit : (échelle X, échelle Y). Les valeurs de mise à l’échelle sont FLOAT, sans unité, et doivent être positives ou égales à 0.<br/> Le type est D2D1 \_ Vector \_ 2F.<br/> La valeur par défaut est {1.0 f, 1.0 f}.<br/>                                                                           |
| InterpolationMode.<br/> \_Mode d’interpolation d2d1 BITMAPSOURCE \_ prop \_ \_<br/>      | Mode d’interpolation utilisé pour mettre à l’échelle l’image. Pour plus d’informations, consultez [modes d’interpolation](#interpolation-modes) .<br/> Si le mode désactive le mipmap, BitmapSouce met en cache l’image à la résolution déterminée par les propriétés Scale et EnableDPICorrection.<br/> Le type est D2D1 \_ \_ mode d’interpolation BITMAPSOURCE \_ .<br/> La valeur par défaut est D2D1 le \_ \_ mode d’interpolation BITMAPSOURCE \_ \_ linéaire.<br/> |
| EnableDPICorrection<br/> D2D1 \_ BITMAPSOURCE \_ prop \_ activer \_ la \_ Correction PPP<br/> | Si vous affectez la valeur TRUE à cette propriété, l’effet met à l’échelle l’image d’entrée pour convertir les PPP signalées par [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) en PPP du contexte de périphérique. L’effet utilise le mode d’interpolation que vous définissez avec la propriété InterpolationMode. Si vous définissez cette valeur sur FALSe, l’effet utilise une résolution de 96,0 pour l’image de sortie.<br/> Le type est BOOL.<br/> La valeur par défaut est FALSE.<br/>   |
| AlphaMode<br/> D2D1 \_ BITMAPSOURCE \_ prop \_ ( \_ mode Alpha)<br/>                       | Mode Alpha de la sortie. Cette valeur peut être prémultipliée ou directe. Pour plus d’informations, consultez [modes alpha](#alpha-modes) .<br/> Le type est D2D1 \_ le \_ mode Alpha BITMAPSOURCE \_ .<br/> La valeur par défaut est D2D1 le \_ \_ mode Alpha BITMAPSOURCE \_ \_ prémultiplié.<br/>                                                                                                                                                              |
| Orientation<br/> \_Orientation d2d1 BITMAPSOURCE \_ prop \_<br/>                     | Opération d’inversion et/ou de rotation à effectuer sur l’image. Pour plus d’informations, consultez [orientation](#orientation) .<br/> Le type est D2D1 \_ BITMAPSOURCE \_ orientation.<br/> La valeur par défaut est D2D1 l' \_ orientation de BITMAPSOURCE \_ \_ par défaut.<br/>                                                                                                                                                                                 |



 

## <a name="interpolation-modes"></a>Modes d’interpolation

L’effet est interpolé à l’aide de ce mode lorsqu’il met à l’échelle une image ou lorsqu’il corrige les PPP. Les modes d’interpolation utilisés par cet effet sont calculés par le processeur, et non par le GPU.



| Nom                                                       | Description                                                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Mode d' \_ interpolation BITMAPSOURCE \_ d2d1 \_ le plus proche \_ voisin | Échantillonne le point unique le plus proche et l’utilise. Ne génère pas de mipmap.                                                                                                                                                           |
| \_Mode d' \_ interpolation d2d1 BITMAPSOURCE \_ \_ linéaire            | Utilise un échantillon à quatre points et une interpolation linéaire. Ne génère pas de mipmap.                                                                                                                                                        |
| D2D1 \_ \_ mode d’interpolation \_ BITMAPSOURCE \_ cubique             | Utilise un exemple de noyau cubique 16 pour l’interpolation. Ne génère pas de mipmap.                                                                                                                                                          |
| D2D1 \_ \_ mode d’interpolation \_ BITMAPSOURCE \_ fant              | Utilise l’interpolation WIC fant, identique à l’interface [**IWICBitmapScaler**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapscaler) . Ne génère pas de mipmap.                                                                                       |
| D2D1 \_ de \_ MIPMAP mode d’interpolation BITMAPSOURCE \_ \_ \_ linéaire    | Génère une chaîne mipmap dans la mémoire système à l’aide de l’interpolation bilinéaire. Pour chaque mipmap, l’effet s’ajuste au multiple le plus proche de 0,5 à l’aide de l’interpolation bilinéaire, puis ajuste la quantité restante à l’aide d’une interpolation linéaire. |



 

## <a name="orientation"></a>Orientation

La propriété orientation peut être utilisée pour appliquer un indicateur d’orientation EXIF incorporé dans une image.



| Nom                                                                    | Description                                                        |
|-------------------------------------------------------------------------|--------------------------------------------------------------------|
| D2D1 de l' \_ \_ orientation BITMAPSOURCE \_ par défaut                                | Par défaut. L’effet ne change pas l’orientation de l’entrée.   |
| D2D1 l’orientation de BITMAPSOURCE de l' \_ \_ \_ \_ horizontale                       | Retourne l’image horizontalement.                                      |
| D2D1 \_ l' \_ orientation BITMAPSOURCE \_ pivoter \_ CLOCKWISE180                   | Fait pivoter l’image dans le sens des aiguilles d’une montre à 180 degrés.                           |
| D2D1 \_ l' \_ orientation BITMAPSOURCE \_ pivoter \_ CLOCKWISE180 \_ retourner \_ horizontalement | Fait pivoter l’image dans le sens des aiguilles d’une montre à 180 degrés et l’inverse horizontalement. |
| D2D1 \_ l' \_ orientation BITMAPSOURCE \_ pivoter \_ CLOCKWISE270 \_ retourner \_ horizontalement | Fait pivoter l’image dans le sens des aiguilles d’une montre à 270 degrés et l’inverse horizontalement. |
| D2D1 \_ l' \_ orientation BITMAPSOURCE \_ pivoter \_ CLOCKWISE90                    | Fait pivoter l’image dans le sens des aiguilles d’une montre à 90 degrés.                            |
| D2D1 \_ l' \_ orientation BITMAPSOURCE \_ pivoter \_ CLOCKWISE90 \_ retourner \_ horizontalement  | Fait pivoter l’image dans le sens des aiguilles d’une montre à 90 degrés et l’inverse horizontalement.  |
| D2D1 \_ l' \_ orientation BITMAPSOURCE \_ pivoter \_ CLOCKWISE270                   | Fait pivoter l’image dans le sens des aiguilles d’une montre à 270 degrés.                           |



 

Cet extrait de code montre comment convertir des valeurs d’orientation EXIF (définies dans propKey. h) en \_ valeurs d’orientation d2d1 BITMAPSOURCE \_ .


```C++
#include <propkey.h>
#include <d2d1effects.h>

D2D1_BITMAPSOURCE_ORIENTATION GetBitmapSourceOrientation(unsigned short PhotoOrientation)
{
       switch (PhotoOrientation)
       {
       case PHOTO_ORIENTATION_NORMAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_DEFAULT;
       case PHOTO_ORIENTATION_FLIPHORIZONTAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE180:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE180;
       case PHOTO_ORIENTATION_FLIPVERTICAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE180_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_TRANSPOSE: 
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE90_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE270:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE90;
       case PHOTO_ORIENTATION_TRANSVERSE:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE270_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE90:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE270;
       default:
              return D2D1_BITMAPSOURCE_ORIENTATION_DEFAULT;
       }
}
```



## <a name="alpha-modes"></a>Modes alpha



| Nom                                           | Description                                            |
|------------------------------------------------|--------------------------------------------------------|
| D2D1 \_ \_ mode Alpha \_ BITMAPSOURCE \_ prémultiplié | La sortie d’effet utilise une alpha prémultipliée.<br/> |
| \_ \_ Mode Alpha BITMAPSOURCE \_ d2d1 \_ simple      | La sortie d’effet utilise l’alpha simple.<br/>      |



 

## <a name="remarks"></a>Notes

Pour optimiser les performances lors de l’utilisation conjointe de WIC et de [Direct2D](./direct2d-portal.md) , vous devez utiliser [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) pour convertir au format de pixel approprié en fonction du scénario de votre application et de la précision native de l’image.

Dans la plupart des cas, le pipeline [Direct2D](./direct2d-portal.md) de votre application nécessite uniquement 8 bits par canal (BPC) de précision, ou l’image fournit uniquement une précision de 8 BPC. par conséquent, vous devez convertir en GUID \_ WICPixelFormat32bppPBGRA. Toutefois, si vous souhaitez tirer parti d’une précision supplémentaire fournie par une image (par exemple, un fichier JPEG-XR ou TIFF stocké avec une précision supérieure à 8 BPC), vous devez utiliser un format de pixel basé sur RVBA. Le tableau ci-dessous fournit plus de détails.



| Précision souhaitée   | Précision native de l’image | Format de pixel recommandé                |
|---------------------|-------------------------------|-----------------------------------------|
| 8 bits par canal  | <= 8 bits par canal      | GUID \_ WICPixelFormat32bppPBGRA          |
| Aussi élevée que possible | <= 8 bits par canal      | GUID \_ WICPixelFormat32bppPBGRA          |
| Aussi élevée que possible | > 8 bits par canal       | Ordre des canaux RVBA, alpha prémultiplié |



 

Étant donné que de nombreux formats d’image prennent en charge plusieurs niveaux de précision, vous devez utiliser [**IWICBitmapSource :: GetPixelFormat**](/windows/desktop/wic/-wic-codec-iwicbitmapsource-getpixelformat-proxy) pour obtenir le format de pixel d’image s natif, puis utiliser [**IWICPixelFormatInfo**](/windows/desktop/api/wincodec/nn-wincodec-iwicpixelformatinfo) pour déterminer le nombre de bits par canal de précision disponibles pour ce format. Notez également que tous les matériels ne prennent pas en charge les formats de pixel haute précision. Dans ce cas, votre application peut avoir besoin de revenir à l’appareil WARP pour prendre en charge la haute précision.

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

 

