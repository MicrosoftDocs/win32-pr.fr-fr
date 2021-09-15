---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. Differential.
ms.assetid: 330d1f88-5f54-4e29-b57f-eb7112203e04
title: Stratégie de métadonnées de photos System. GPS. Differential
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc3f114683d324a067fe4ce4034e2de5cfc88da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127526473"
---
# <a name="systemgpsdifferential-photo-metadata-policy"></a>Stratégie de métadonnées de photos System. GPS. Differential

Stratégie de métadonnées de la photo pour la propriété [System. GPS. Differential](../properties/props-system-gps-differential.md) .

### <a name="pkey"></a>A-la

\_Différentielle GPS \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_UI2 VT

### <a name="input-propvariant-type"></a>Type de PROPVARIANT d’entrée

VT \_ UI1, VT \_ UI2 et VT \_ UI4 sont tous acceptés.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policies"></a>Stratégies JPEG

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 30} | ushort      |
| 2     | /xmp/exif:GPSDifferential | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 30} | ushort      |
| 2     | /xmp/exif:GPSDifferential | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{UShort = 30} |
| 2     | /xmp/exif:gpsdifferential |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 30}          | ushort      |
| 2     | /ifd/xmp/exif:GPSDifferential | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 30}          | ushort      |
| 2     | /ifd/xmp/exif:GPSDifferential | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /IFD/GPS/{UShort = 30}          |
| 2     | /ifd/xmp/exif:gpsdifferential |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. Differential](../properties/props-system-gps-differential.md)
</dt> </dl>

 

 
