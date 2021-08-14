---
description: Stratégie de métadonnées de la photo pour la propriété System. image. ColorSpace.
ms.assetid: 10770f16-8db2-4719-bce3-452f578002ec
title: Stratégie de métadonnées de photo System. image. ColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c7d7c9134a8bd93a12ba6cfb6bd8605e228cb6b745ad4401a94f91a2ba9ff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710419"
---
# <a name="systemimagecolorspace-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. image. ColorSpace

Stratégie de métadonnées de la photo pour la propriété [System. image. colorspace](../properties/props-system-image-colorspace.md) .

### <a name="pkey"></a>A-la

Image de la \_ \_ ColorSpace

### <a name="containers"></a>Containers

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



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 40961} | ushort      |
| 2     | /xmp/exif:ColorSpace          | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 40961} | ushort      |
| 2     | /xmp/exif:ColorSpace          | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 40961} |
| 2     | /xmp/exif:colorspace          |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 40961} | ushort      |
| 2     | /ifd/xmp/exif:ColorSpace | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 40961} | ushort      |
| 2     | /ifd/xmp/exif:ColorSpace | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{UShort = 40961} |
| 2     | /ifd/xmp/exif:colorspace |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. image. ColorSpace](../properties/props-system-image-colorspace.md)
</dt> </dl>

 

 
