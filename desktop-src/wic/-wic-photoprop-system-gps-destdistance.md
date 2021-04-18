---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. DestDistance.
ms.assetid: 1bd72acb-f462-454d-aec2-72d5b4517de3
title: Stratégie de métadonnées de photo System. GPS. DestDistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc71c89ae6270f5babf08637f54baaf2cb57aae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520605"
---
# <a name="systemgpsdestdistance-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. DestDistance

Stratégie de métadonnées de la photo pour la propriété [System. GPS. DestDistance](../properties/props-system-gps-destdistance.md) .

### <a name="pkey"></a>A-la

\_DestDistance GPS \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur est générée à partir de System. GPS. DestDistanceNumerator et de System. GPS. DestDistanceDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 26} |             |
| 2     | /xmp/exif:GPSDestDistance |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 26} |             |
| 2     | /xmp/exif:GPSDestDistance |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{UShort = 26} |
| 2     | /xmp/exif:gpsdestdistance |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 26}          |             |
| 2     | /ifd/xmp/exif:GPSDestDistance |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 26}          |             |
| 2     | /ifd/xmp/exif:GPSDestDistance |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /IFD/GPS/{UShort = 26}          |
| 2     | /ifd/xmp/exif:gpsdestdistance |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. DestDistance](../properties/props-system-gps-destdistance.md)
</dt> </dl>

 

 
