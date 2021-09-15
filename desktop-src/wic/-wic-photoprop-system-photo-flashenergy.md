---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. FlashEnergy.
ms.assetid: d10a4de9-16fe-4920-aa7f-b2f95fb23045
title: Stratégie de métadonnées de photo System. photo. FlashEnergy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c272b4d6d14bf2f2e81d0964a3dc4395ba62dc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411420"
---
# <a name="systemphotoflashenergy-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. FlashEnergy

Stratégie de métadonnées de la photo pour la propriété [System. photo. FlashEnergy](../properties/props-system-photo-flashenergy.md) .

### <a name="pkey"></a>A-la

\_Photo \_ FlashEnergy

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="input-type"></a>Type d’entrée

Double

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41483} |             |
| 2     | /xmp/exif:FlashEnergy         |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41483} |             |
| 2     | /xmp/exif:FlashEnergy         |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 41483} |
| 2     | /xmp/exif:flashenergy         |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41483}  |             |
| 2     | /ifd/xmp/exif:FlashEnergy |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41483}  |             |
| 2     | /ifd/xmp/exif:FlashEnergy |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{UShort = 41483}  |
| 2     | /ifd/xmp/exif:flashenergy |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. FlashEnergy](../properties/props-system-photo-flashenergy.md)
</dt> </dl>

 

 
