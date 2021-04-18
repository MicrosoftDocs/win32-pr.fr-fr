---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. MakerNote.
ms.assetid: e1018bc6-3fd2-4212-afee-6811bfe99f14
title: Stratégie de métadonnées de photo System. photo. MakerNote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df1a16205d6a9d1229d3627e6b9cc8c746d8a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533919"
---
# <a name="systemphotomakernote-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. MakerNote

Stratégie de métadonnées de la photo pour la propriété [System. photo. MakerNote](../properties/props-system-photo-makernote.md) .

### <a name="pkey"></a>A-la

\_Photo \_ MakerNote

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_VTUI1 vecteur \| VT

### <a name="input-type"></a>Type d’entrée

Buffer

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37500} |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37500} |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37500} |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37500} |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37500} |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{UShort = 37500} |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. MakerNote](../properties/props-system-photo-makernote.md)
</dt> </dl>

 

 
