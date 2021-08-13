---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. altitude.
ms.assetid: 63d59aa3-52a6-4b6f-b6ec-a1c4abcee83f
title: Stratégie de métadonnées de photo System. GPS. altitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40a9209bfb0bbc1a4c6f95ce4a995d32d3f532c293dd2295c335eea61c22df89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441999"
---
# <a name="systemgpsaltitude-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. altitude

Stratégie de métadonnées de la photo pour la propriété [System. GPS. altitude](../properties/props-system-gps-altitude.md) .

### <a name="pkey"></a>A-la

\_Altitude GPS \_

### <a name="description"></a>Description

L’altitude est indiquée sous la forme d’une valeur absolue référencée en mètres.

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ R8

### <a name="input-propvariant-type"></a>Type de PROPVARIANT d’entrée

VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur peut être écrite en écrivant dans System. GPS. altitude. numérateur et System. GPS. altitude. dénominateur. Il ne peut pas être écrit directement. Les chemins d’accès en écriture dans les tableaux suivants indiquent où la valeur peut être enregistrée lors de sa génération, et non lors de son écriture directe. Lorsque la valeur est lue, les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 6} |             |
| 2     | /xmp/exif:GPSAltitude    |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 6} |             |
| 2     | /xmp/exif:GPSAltitude    |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{UShort = 6} |
| 2     | /xmp/exif:gpsaltitude    |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 6}       |             |
| 2     | /ifd/xmp/exif:GPSAltitude |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 6}       |             |
| 2     | /ifd/xmp/exif:GPSAltitude |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                      |     |
|-------|---------------------------|-----|
| 1     | /IFD/GPS/{UShort = 6}       |     |
| 2     | /ifd/xmp/exif:gpsaltitude |     |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. altitude](../properties/props-system-gps-altitude.md)
</dt> </dl>

 

 
