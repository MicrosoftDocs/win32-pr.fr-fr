---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. orientation.
ms.assetid: 27e6d4f5-39d5-4cb4-88bc-b0d61ccaa2f3
title: Stratégie de métadonnées de photo System. photo. orientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28f4f350cd1a4c24d71ec737b4679aea2f7cab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035029"
---
# <a name="systemphotoorientation-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. orientation

Stratégie de métadonnées de la photo pour la propriété [System. photo. orientation](../properties/props-system-photo-meteringmode.md) .

### <a name="pkey"></a>A-la

Orientation de photo de l' \_ hypergraphique \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_UI2 VT

### <a name="input-type"></a>Type d’entrée

UShort

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                   | Format de disque |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{UShort = 274} | ushort      |
| 2     | /XMP/TIFF : orientation  | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                   | Format de disque |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{UShort = 274} | ushort      |
| 2     | /XMP/TIFF : orientation  | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                   |
|-------|------------------------|
| 1     | /App1/IFD/{UShort = 274} |
| 2     | /XMP/TIFF : orientation  |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/{UShort = 274}         | ushort      |
| 2     | /IFD/XMP/TIFF : orientation | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/{UShort = 274}         | ushort      |
| 2     | /IFD/XMP/TIFF : orientation | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                      |
|-------|---------------------------|
| 1     | /IFD/{UShort = 274}         |
| 2     | /IFD/XMP/TIFF : orientation |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. orientation](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
