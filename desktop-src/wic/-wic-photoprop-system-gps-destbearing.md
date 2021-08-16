---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. DestBearing.
ms.assetid: ccc31b3d-27fd-4a8c-a304-852cf6114ec5
title: Stratégie de métadonnées de photo System. GPS. DestBearing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 598ef1e759f75dfb4851f2f3f435b53db1f875421c3d21446ae3de33f688cefd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205510"
---
# <a name="systemgpsdestbearing-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. DestBearing

Stratégie de métadonnées de la photo pour la propriété [System. GPS. DestBearing](../properties/props-system-gps-destbearing.md) .

### <a name="pkey"></a>A-la

\_DestBearing GPS \_

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur peut être écrite en écrivant dans System. GPS. DestBearingNumerator et System. GPS. DestBearingDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 24} |             |
| 2     | /xmp/exif:GPSDestBearing  |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 24} |             |
| 2     | /xmp/exif:GPSDestBearing  |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 24} |             |
| 2     | /xmp/exif:gpsdestbearing  |             |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                         | Format de disque |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 24}         |             |
| 2     | /ifd/xmp/exif:GPSDestBearing |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                         | Format de disque |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 24}         |             |
| 2     | /ifd/xmp/exif:GPSDestBearing |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                         |
|-------|------------------------------|
| 1     | /IFD/GPS/{UShort = 24}         |
| 2     | /ifd/xmp/exif:gpsdestbearing |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. DestBearing](../properties/props-system-gps-destbearing.md)
</dt> </dl>

 

 
