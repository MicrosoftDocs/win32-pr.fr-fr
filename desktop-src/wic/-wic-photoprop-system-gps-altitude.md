---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. altitude.
ms.assetid: 63d59aa3-52a6-4b6f-b6ec-a1c4abcee83f
title: Stratégie de métadonnées de photo System. GPS. altitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003d39d135c625a01035c023b5d7dc8d890b3b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520747"
---
# <a name="systemgpsaltitude-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. altitude

Stratégie de métadonnées de la photo pour la propriété [System. GPS. altitude](../properties/props-system-gps-altitude.md) .

### <a name="pkey"></a>A-la

\_Altitude GPS \_

### <a name="description"></a>Description

L’altitude est indiquée sous la forme d’une valeur absolue référencée en mètres.

### <a name="containers"></a>Conteneurs

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



| Commande | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 6} |             |
| 2     | /xmp/exif:GPSAltitude    |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 6} |             |
| 2     | /xmp/exif:GPSAltitude    |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{UShort = 6} |
| 2     | /xmp/exif:gpsaltitude    |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 6}       |             |
| 2     | /ifd/xmp/exif:GPSAltitude |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 6}       |             |
| 2     | /ifd/xmp/exif:GPSAltitude |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                      |     |
|-------|---------------------------|-----|
| 1     | /IFD/GPS/{UShort = 6}       |     |
| 2     | /ifd/xmp/exif:gpsaltitude |     |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. altitude](../properties/props-system-gps-altitude.md)
</dt> </dl>

 

 
