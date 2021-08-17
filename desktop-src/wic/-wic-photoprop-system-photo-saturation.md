---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. saturation.
ms.assetid: 1dbb7515-7022-404c-928a-9eb09e43e7a7
title: Stratégie de métadonnées de photo System. photo. saturation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1be1c5be7a0663d5f57823dcb704b843f56e6076713de3682e4b12d6b533ff48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087012"
---
# <a name="systemphotosaturation-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. saturation

Stratégie de métadonnées de la photo pour la propriété [System. photo. saturation](../properties/props-system-photo-saturation.md) .

### <a name="pkey"></a>A-la

Saturation de la photo de la \_ \_

### <a name="containers"></a>Containers

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



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41993} | ushort      |
| 2     | /XMP/EXIF : saturation          | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41993} | ushort      |
| 2     | /XMP/EXIF : saturation          | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 41993} |
| 2     | /XMP/EXIF : saturation          |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41993} | ushort      |
| 2     | /IFD/XMP/EXIF : saturation | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41993} | ushort      |
| 2     | /IFD/XMP/EXIF : saturation | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{UShort = 41993} |
| 2     | /IFD/XMP/EXIF : saturation |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. saturation](../properties/props-system-photo-saturation.md)
</dt> </dl>

 

 
