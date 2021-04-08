---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. saturation.
ms.assetid: 1dbb7515-7022-404c-928a-9eb09e43e7a7
title: Stratégie de métadonnées de photo System. photo. saturation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb2b199458f063f2c28d7f6780a6ea907f76f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035028"
---
# <a name="systemphotosaturation-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. saturation

Stratégie de métadonnées de la photo pour la propriété [System. photo. saturation](../properties/props-system-photo-saturation.md) .

### <a name="pkey"></a>A-la

Saturation de la photo de la \_ \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ UI4

### <a name="input-type"></a>Type d’entrée

UShort

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41993} | ushort      |
| 2     | /XMP/EXIF : saturation          | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41993} | ushort      |
| 2     | /XMP/EXIF : saturation          | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 41993} |
| 2     | /XMP/EXIF : saturation          |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41993} | ushort      |
| 2     | /IFD/XMP/EXIF : saturation | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41993} | ushort      |
| 2     | /IFD/XMP/EXIF : saturation | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{UShort = 41993} |
| 2     | /IFD/XMP/EXIF : saturation |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. saturation](../properties/props-system-photo-saturation.md)
</dt> </dl>

 

 
