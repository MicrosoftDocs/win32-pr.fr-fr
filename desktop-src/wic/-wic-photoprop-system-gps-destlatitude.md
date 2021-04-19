---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. DestLatitude.
ms.assetid: 05284291-977d-49b8-ad92-365f68384960
title: Stratégie de métadonnées de photo System. GPS. DestLatitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192db0f8efc868e9457e86d283d9967e4692c95b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536854"
---
# <a name="systemgpsdestlatitude-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. DestLatitude

Stratégie de métadonnées de la photo pour la propriété [System. GPS. DestLatitude](../properties/props-system-gps-destlatitude.md) .

### <a name="pkey"></a>A-la

\_DestLatitude GPS \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ Vector \| VT \_ R8

### <a name="input-propvariant-type"></a>Type de PROPVARIANT d’entrée

VT \_ Vector \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur est générée à partir de System. GPS. DestLatitudeNumerator et de System. GPS. DestLatitudeDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 20} |             |
| 2     | /xmp/exif:GPSDestLatitude |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 20} |             |
| 2     | /xmp/exif:GPSDestLatitude |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{UShort = 20} |
| 2     | /xmp/exif:gpsdestlatitude |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 20}          |             |
| 2     | /ifd/xmp/exif:GPSDestLatitude |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 20}          |             |
| 2     | /ifd/xmp/exif:GPSDestLatitude |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /IFD/GPS/{UShort = 20}          |
| 2     | /ifd/xmp/exif:gpsdestlatitude |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. DestLatitude](../properties/props-system-gps-destlatitude.md)
</dt> </dl>

 

 
