---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. DestBearingRef.
ms.assetid: d1c8b3cc-ed52-43ca-a0ba-045a2c5fe274
title: Stratégie de métadonnées de photo System. GPS. DestBearingRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ee4b984d0a759769b80be76b53499690673c7ec630c759aa0371b53ea9368f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087850"
---
# <a name="systemgpsdestbearingref-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. DestBearingRef

Stratégie de métadonnées de la photo pour la propriété [System. GPS. DestBearingRef](../properties/props-system-gps-destbearingref.md) .

### <a name="pkey"></a>A-la

\_DestBearingRef GPS \_

### <a name="containers"></a>Containers

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



| Commande | Chemin                        | Format de disque |
|-------|-----------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 23}   | ascii       |
| 2     | /xmp/exif:GPSDestBearingRef | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                        | Format de disque |
|-------|-----------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 23}   | ascii       |
| 2     | /xmp/exif:GPSDestBearingRef | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                        |
|-------|-----------------------------|
| 1     | /App1/IFD/GPS/{UShort = 23}   |
| 2     | /xmp/exif:gpsdestbearingref |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                            | Format de disque |
|-------|---------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 23}            | ascii       |
| 2     | /ifd/xmp/exif:GPSDestBearingRef | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                            | Format de disque |
|-------|---------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 23}            | ascii       |
| 2     | /ifd/xmp/exif:GPSDestBearingRef | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| order | path                            |
|-------|---------------------------------|
| 1     | /IFD/GPS/{UShort = 23}            |
| 2     | /ifd/xmp/exif:gpsdestbearingref |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. DestBearingRef](../properties/props-system-gps-destbearingref.md)
</dt> </dl>

 

 
