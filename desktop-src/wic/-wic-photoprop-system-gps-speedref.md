---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. SpeedRef.
ms.assetid: 45fea6be-1e63-4244-a93d-d446e315ddd4
title: Stratégie de métadonnées de photo System. GPS. SpeedRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c454a016dd77345c0a85e0ca3df1ae52694bd81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527679"
---
# <a name="systemgpsspeedref-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. SpeedRef

Stratégie de métadonnées de la photo pour la propriété [System. GPS. SpeedRef](../properties/props-system-gps-speedref.md) .

### <a name="pkey"></a>A-la

\_SpeedRef GPS \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-propvariant-type"></a>Type de PROPVARIANT d’entrée

VT \_ LPWStr est préféré, mais VT \_ LPSTR est également accepté.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policies"></a>Stratégies JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 12} | ascii       |
| 2     | /xmp/exif:GPSSpeedRef     | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 12} | ascii       |
| 2     | /xmp/exif:GPSSpeedRef     | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 12} |             |
| 2     | /xmp/exif:gpsspeedref     |             |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                      |         |
|-------|---------------------------|---------|
| 1     | /IFD/GPS/{UShort = 12}      | ascii   |
| 2     | /ifd/xmp/exif:GPSSpeedRef | unicode |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 12}      | ascii       |
| 2     | /ifd/xmp/exif:GPSSpeedRef | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                      |
|-------|---------------------------|
| 1     | /IFD/GPS/{UShort = 12}      |
| 2     | /ifd/xmp/exif:gpsspeedref |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. SpeedRef](../properties/props-system-gps-speedref.md)
</dt> </dl>

 

 
