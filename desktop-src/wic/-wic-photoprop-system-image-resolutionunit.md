---
description: Stratégie de métadonnées de la photo pour la propriété System. image. ResolutionUnit.
ms.assetid: b8b744bd-976b-4648-a04b-33607467d6ac
title: Stratégie de métadonnées de photo System. image. ResolutionUnit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d954df0b7efe9501cf25c33a54cd4296fb03f3c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521213"
---
# <a name="systemimageresolutionunit-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. image. ResolutionUnit

Stratégie de métadonnées de la photo pour la propriété [System. image. ResolutionUnit](../properties/props-system-image-resolutionunit.md) .

### <a name="pkey"></a>A-la

Image de la \_ \_ ResolutionUnit

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui.

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ I2

### <a name="input-type"></a>Type d’entrée

UShort

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/{UShort = 296}   | ushort      |
| 2     | /xmp/tiff:ResolutionUnit | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/{UShort = 296}   | ushort      |
| 2     | /xmp/tiff:ResolutionUnit | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                     |
|-------|--------------------------|
| 1     | /App1/IFD/{UShort = 296}   |
| 2     | /xmp/tiff:resolutionunit |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                         | Format de disque |
|-------|------------------------------|-------------|
| 1     | /IFD/{UShort = 296}            | ushort      |
| 2     | /ifd/xmp/tiff:ResolutionUnit | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                         | Format de disque |
|-------|------------------------------|-------------|
| 1     | /IFD/{UShort = 296}            | ushort      |
| 2     | /ifd/xmp/tiff:ResolutionUnit | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                         |
|-------|------------------------------|
| 1     | /IFD/{UShort = 296}            |
| 2     | /ifd/xmp/tiff:resolutionunit |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. image. ResolutionUnit](../properties/props-system-image-resolutionunit.md)
</dt> </dl>

 

 
