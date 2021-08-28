---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. ISOSpeed.
ms.assetid: 22b5552c-41b1-4090-a827-b920dcbba5e9
title: Stratégie de métadonnées de photo System. photo. ISOSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6612bffdeaafb69ea1b1122a1d75c00214d366e9
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881637"
---
# <a name="systemphotoisospeed-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. ISOSpeed

Stratégie de métadonnées de la photo pour la propriété [System. photo. ISOSpeed](../properties/props-system-photo-focallengthinfilm.md) .

### <a name="pkey"></a>A-la

\_Photo \_ ISOSpeed

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



| JSON | Chemin d’accès                                    | Format de disque |
|-------|-----------------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 34855}           | ushort      |
| 2     | /XMP/ &lt; xmpseq &gt; EXIF : ISOSpeedRatings | unicode     |
| 3     | /xmp/exif:ISOSpeed                      | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                                    | Format de disque |
|-------|-----------------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 34855}           | ushort      |
| 2     | /XMP/ &lt; xmpseq &gt; EXIF : ISOSpeedRatings | unicode     |
| 3     | /xmp/exif:ISOSpeed                      | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                                    |
|-------|-----------------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 34855}           |
| 2     | /XMP/ &lt; xmpseq &gt; EXIF : ISOSpeedRatings |
| 3     | /xmp/exif:isospeed                      |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                                        | Format de disque |
|-------|---------------------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 34855}                    | ushort      |
| 2     | /IFD/XMP/ &lt; xmpseq &gt; EXIF : ISOSpeedRatings | unicode     |
| 3     | /ifd/xmp/exif:ISOSpeed                      | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                                        | Format de disque |
|-------|---------------------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 34855}                    | ushort      |
| 2     | /IFD/XMP/ &lt; xmpseq &gt; EXIF : ISOSpeedRatings | unicode     |
| 3     | /ifd/xmp/exif:ISOSpeed                      | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                                        |
|-------|---------------------------------------------|
| 1     | /IFD/EXIF/{UShort = 34855}                    |
| 2     | /IFD/XMP/ &lt; xmpseq &gt; EXIF : ISOSpeedRatings |
| 3     | /ifd/xmp/exif:isospeed                      |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. ISOSpeed](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
