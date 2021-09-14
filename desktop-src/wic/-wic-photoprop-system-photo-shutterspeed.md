---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. ShutterSpeed.
ms.assetid: f320944c-978d-4a3c-9bf8-5c5652123e29
title: Stratégie de métadonnées de photo System. photo. ShutterSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8df8c9e7fda5643fed022f67c3b6b7846e7a72f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196112"
---
# <a name="systemphotoshutterspeed-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. ShutterSpeed

Stratégie de métadonnées de la photo pour la propriété [System. photo. ShutterSpeed](../properties/props-system-photo-shutterspeed.md) .

### <a name="pkey"></a>A-la

\_Photo \_ ShutterSpeed

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur est générée à partir de System. photo. ShutterSpeedNumerator et de System. photo. ShutterSpeedDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37377} |             |
| 2     | /xmp/exif:ShutterSpeedValue   |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37377} |             |
| 2     | /xmp/exif:ShutterSpeedValue   |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37377} |
| 2     | /xmp/exif:shutterspeedvalue   |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                            | Format de disque |
|-------|---------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37377}        |             |
| 2     | /ifd/xmp/exif:ShutterSpeedValue |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                            | Format de disque |
|-------|---------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37377}        |             |
| 2     | /ifd/xmp/exif:ShutterSpeedValue |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                            |
|-------|---------------------------------|
| 1     | /IFD/EXIF/{UShort = 37377}        |
| 2     | /ifd/xmp/exif:shutterspeedvalue |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. ShutterSpeed](../properties/props-system-photo-shutterspeed.md)
</dt> </dl>

 

 
