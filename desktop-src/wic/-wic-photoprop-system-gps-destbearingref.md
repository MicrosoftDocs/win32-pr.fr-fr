---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. DestBearingRef.
ms.assetid: d1c8b3cc-ed52-43ca-a0ba-045a2c5fe274
title: Stratégie de métadonnées de photo System. GPS. DestBearingRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f00d3083459fe365fc54e81dc485ddd26887a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203652"
---
# <a name="systemgpsdestbearingref-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. DestBearingRef

Stratégie de métadonnées de la photo pour la propriété [System. GPS. DestBearingRef](../properties/props-system-gps-destbearingref.md) .

### <a name="pkey"></a>A-la

\_DestBearingRef GPS \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-type"></a>Type d’entrée

Chaîne.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policies"></a>Stratégies JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                        | Format de disque |
|-------|-----------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 23}   | ascii       |
| 2     | /xmp/exif:GPSDestBearingRef | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                        | Format de disque |
|-------|-----------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 23}   | ascii       |
| 2     | /xmp/exif:GPSDestBearingRef | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                        |
|-------|-----------------------------|
| 1     | /App1/IFD/GPS/{UShort = 23}   |
| 2     | /xmp/exif:gpsdestbearingref |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                            | Format de disque |
|-------|---------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 23}            | ascii       |
| 2     | /ifd/xmp/exif:GPSDestBearingRef | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                            | Format de disque |
|-------|---------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 23}            | ascii       |
| 2     | /ifd/xmp/exif:GPSDestBearingRef | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| order | path                            |
|-------|---------------------------------|
| 1     | /IFD/GPS/{UShort = 23}            |
| 2     | /ifd/xmp/exif:gpsdestbearingref |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. DestBearingRef](../properties/props-system-gps-destbearingref.md)
</dt> </dl>

 

 
