---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. ShutterSpeed.
ms.assetid: f320944c-978d-4a3c-9bf8-5c5652123e29
title: Stratégie de métadonnées de photo System. photo. ShutterSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad11550a19cd043fd5d182b2cf508aec3e26c64a0dc2ee1d1c24576ebf18f8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710098"
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



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37377} |             |
| 2     | /xmp/exif:ShutterSpeedValue   |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37377} |             |
| 2     | /xmp/exif:ShutterSpeedValue   |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37377} |
| 2     | /xmp/exif:shutterspeedvalue   |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                            | Format de disque |
|-------|---------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37377}        |             |
| 2     | /ifd/xmp/exif:ShutterSpeedValue |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                            | Format de disque |
|-------|---------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37377}        |             |
| 2     | /ifd/xmp/exif:ShutterSpeedValue |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                            |
|-------|---------------------------------|
| 1     | /IFD/EXIF/{UShort = 37377}        |
| 2     | /ifd/xmp/exif:shutterspeedvalue |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. ShutterSpeed](../properties/props-system-photo-shutterspeed.md)
</dt> </dl>

 

 
