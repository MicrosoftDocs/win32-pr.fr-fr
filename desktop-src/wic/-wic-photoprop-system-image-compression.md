---
description: Stratégie de métadonnées de la photo pour la propriété System. image. compression.
ms.assetid: 0fada41f-f6f8-43b3-ad65-79785e859c9c
title: Stratégie de métadonnées de photo System. image. compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32fdc55e2a6a962b1a3dfd9057ef25c89d942f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519734"
---
# <a name="systemimagecompression-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. image. compression

Stratégie de métadonnées de la photo pour la propriété [System. image. compression](../properties/props-system-image-compression.md) .

### <a name="pkey"></a>A-la

Compression d’image de la \_ \_ prime

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

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
| 1     | /App1/IFD/{UShort = 259} | ushort      |
| 2     | /XMP/TIFF : compression  | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                   | Format de disque |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{UShort = 259} | ushort      |
| 2     | /XMP/TIFF : compression  | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                   |
|-------|------------------------|
| 1     | /App1/IFD/{UShort = 259} |
| 2     | /XMP/TIFF : compression  |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/{UShort = 259}         | ushort      |
| 2     | /IFD/XMP/TIFF : compression | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/{UShort = 259}         | ushort      |
| 2     | /IFD/XMP/TIFF : compression | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                      |
|-------|---------------------------|
| 1     | /IFD/{UShort = 259}         |
| 2     | /IFD/XMP/TIFF : compression |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. image. compression](../properties/props-system-image-compression.md)
</dt> </dl>

 

 
