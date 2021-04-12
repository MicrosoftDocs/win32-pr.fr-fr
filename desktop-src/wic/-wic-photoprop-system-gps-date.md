---
description: La stratégie de métadonnées de la photo pour la propriété System. GPS. date.
ms.assetid: 75047658-b6f3-454e-961a-89016c244bf6
title: Stratégie de métadonnées de photo System. GPS. date
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c736c79cd76d2d070d727dc024925717b386cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210281"
---
# <a name="systemgpsdate-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. date

La stratégie de métadonnées de la photo pour la propriété [System. GPS. date](../properties/props-system-gps-date.md) .

### <a name="pkey"></a>A-la

Date de la \_ balise GPS \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="input-type"></a>Type d’entrée

Chaîne.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policies"></a>Stratégies JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 29} | ascii       |
| 2     | /xmp/exif:GPSTimeStamp    | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 29} | ascii       |
| 2     | /xmp/exif:GPSTimeStamp    | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{UShort = 29} |
| 2     | /xmp/exif:GPSTimeStamp    |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 29}       | ascii       |
| 2     | /ifd/xmp/exif:GPSTimeStamp | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 29}       | ascii       |
| 2     | /ifd/xmp/exif:GPSTimeStamp | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                       |
|-------|----------------------------|
| 1     | /IFD/GPS/{UShort = 29}       |
| 2     | /ifd/xmp/exif:GPSTimeStamp |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. date](../properties/props-system-gps-date.md)
</dt> </dl>

 

 
