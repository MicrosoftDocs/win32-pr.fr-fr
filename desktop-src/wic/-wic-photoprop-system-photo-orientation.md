---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. orientation.
ms.assetid: 27e6d4f5-39d5-4cb4-88bc-b0d61ccaa2f3
title: Stratégie de métadonnées de photo System. photo. orientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f9496942e6be971e0e047596125669fc9112cf82bce6eb02ec7e1cdbddc4de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087065"
---
# <a name="systemphotoorientation-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. orientation

Stratégie de métadonnées de la photo pour la propriété [System. photo. orientation](../properties/props-system-photo-meteringmode.md) .

### <a name="pkey"></a>A-la

Orientation de photo de l' \_ hypergraphique \_

### <a name="containers"></a>Containers

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



| Commande | Chemin                   | Format de disque |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{UShort = 274} | ushort      |
| 2     | /XMP/TIFF : orientation  | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                   | Format de disque |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{UShort = 274} | ushort      |
| 2     | /XMP/TIFF : orientation  | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                   |
|-------|------------------------|
| 1     | /App1/IFD/{UShort = 274} |
| 2     | /XMP/TIFF : orientation  |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/{UShort = 274}         | ushort      |
| 2     | /IFD/XMP/TIFF : orientation | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/{UShort = 274}         | ushort      |
| 2     | /IFD/XMP/TIFF : orientation | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                      |
|-------|---------------------------|
| 1     | /IFD/{UShort = 274}         |
| 2     | /IFD/XMP/TIFF : orientation |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. orientation](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
