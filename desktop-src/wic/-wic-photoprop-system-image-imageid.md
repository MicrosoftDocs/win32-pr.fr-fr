---
description: Stratégie de métadonnées de la photo pour la propriété System. image. ImageID.
ms.assetid: 2a092d16-e7b9-4ffe-9bdb-01ed328ca26f
title: Stratégie de métadonnées de photo System. image. ImageID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab812a8719c905002c91d33a65cc2b570d37cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529271"
---
# <a name="systemimageimageid-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. image. ImageID

Stratégie de métadonnées de la photo pour la propriété [System. image. ImageID](../properties/props-system-image-imageid.md) .

### <a name="pkey"></a>A-la

Image de la \_ \_ ImageID

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-type"></a>Type d’entrée

Chaîne.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 42016} | ascii       |
| 2     | /XMP/EXIF : ImageUniqueID       | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 42016} | ascii       |
| 2     | /XMP/EXIF : ImageUniqueID       | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 42016} |
| 2     | /XMP/EXIF : ImageUniqueID       |



 

### <a name="tiff-policy"></a>Stratégie TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                        | Format de disque |
|-------|-----------------------------|-------------|
|       | /IFD/EXIF/{UShort = 42016}    | ascii       |
|       | /IFD/XMP/EXIF : ImageUniqueID | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                        | Format de disque |
|-------|-----------------------------|-------------|
|       | /IFD/EXIF/{UShort = 42016}    | ascii       |
|       | /IFD/XMP/EXIF : ImageUniqueID | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                        |
|-------|-----------------------------|
|       | /IFD/EXIF/{UShort = 42016}    |
|       | /IFD/XMP/EXIF : ImageUniqueID |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. image. ImageID](../properties/props-system-image-imageid.md)
</dt> </dl>

 

 
