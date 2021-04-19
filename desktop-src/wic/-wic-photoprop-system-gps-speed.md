---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. Speed.
ms.assetid: 278826c2-3057-4da2-8c86-0e44471ad7b0
title: Stratégie de métadonnées de photo System. GPS. Speed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26d89f755114a73ab17388a1718d5ad0cbdf5a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521103"
---
# <a name="systemgpsspeed-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. Speed

Stratégie de métadonnées de la photo pour la propriété [System. GPS. Speed](../properties/props-system-gps-speed.md) .

### <a name="pkey"></a>A-la

\_Vitesse GPS \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur est générée à partir de System. GPS. SpeedNumerator et de System. GPS. SpeedDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 13} |             |
| 2     | /xmp/exif:GPSSpeed        |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 13} |             |
| 2     | /xmp/exif:GPSSpeed        |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{UShort = 13} |
| 2     | /xmp/exif:gpsspeed        |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                   | Format de disque |
|-------|------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 13}   |             |
| 2     | /ifd/xmp/exif:GPSSpeed |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                   | Format de disque |
|-------|------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 13}   |             |
| 2     | /ifd/xmp/exif:GPSSpeed |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                   |
|-------|------------------------|
| 1     | /IFD/GPS/{UShort = 13}   |
| 2     | /ifd/xmp/exif:gpsspeed |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. Speed](../properties/props-system-gps-speed.md)
</dt> </dl>

 

 
