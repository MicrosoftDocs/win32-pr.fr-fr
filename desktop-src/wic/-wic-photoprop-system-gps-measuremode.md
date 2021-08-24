---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. MeasureMode.
ms.assetid: 911a0d81-bd12-4155-b45a-ae1a18f2dd07
title: Stratégie de métadonnées de photo System. GPS. MeasureMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827cd278a71b23934fb0475e78d98b25a9f2b72d413b70f9abc60ba3dbe2c3fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882319"
---
# <a name="systemgpsmeasuremode-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. MeasureMode

Stratégie de métadonnées de la photo pour la propriété [System. GPS. MeasureMode](../properties/props-system-gps-measuremode.md) .

### <a name="pkey"></a>A-la

\_MeasureMode GPS \_

### <a name="containers"></a>Containers

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



| Commande | Chemin                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 10} | ascii       |
| 2     | /xmp/exif:GPSMeasureMode  | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 10} | ascii       |
| 2     | /xmp/exif:GPSMeasureMode  | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{UShort = 10} |
| 2     | /xmp/exif:gpsmeasuremode  |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                         | Format de disque |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 10}         | ascii       |
| 2     | /ifd/xmp/exif:GPSMeasureMode | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                         | Format de disque |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 10}         | ascii       |
| 2     | /ifd/xmp/exif:GPSMeasureMode | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                         |
|-------|------------------------------|
| 1     | /IFD/GPS/{UShort = 10}         |
| 2     | /ifd/xmp/exif:gpsmeasuremode |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. MeasureMode](../properties/props-system-gps-measuremode.md)
</dt> </dl>

 

 
