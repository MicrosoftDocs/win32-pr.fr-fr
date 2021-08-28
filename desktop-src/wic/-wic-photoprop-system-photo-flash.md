---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. Flash.
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: Stratégie de métadonnées de photo System. photo. Flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7798e88c40193cac5c577f1960eee96fc2d868
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880081"
---
# <a name="systemphotoflash-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. Flash

Stratégie de métadonnées de la photo pour la propriété [System. photo. Flash](../properties/props-system-photo-exposuretime.md) .

### <a name="pkey"></a>A-la

Flash de la \_ photo \_

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ UI1 (si le schéma source était XMP) ou VT \_ UI2 (si le schéma source était EXIF)

\\lang1036

### <a name="input-type"></a>Type d’entrée

VT \_ UI1, VTUI2, VT \_ UI4

\\lang1033

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                             | Format de disque |
|-------|----------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37385}    | ushort      |
| 2     | /XMP/ &lt; xmpstruct &gt; EXIF : Flash |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                             | Format de disque |
|-------|----------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37385}    | ushort      |
| 2     | /XMP/ &lt; xmpstruct &gt; EXIF : Flash |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                             |
|-------|----------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37385}    |
| 2     | /XMP/ &lt; xmpstruct &gt; EXIF : Flash |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                                 | Format de disque |
|-------|--------------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37385}             | ushort      |
| 2     | /IFD/XMP/ &lt; xmpstruct &gt; EXIF : Flash |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                                 | Format de disque |
|-------|--------------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37385}             | ushort      |
| 2     | /IFD/XMP/ &lt; xmpstruct &gt; EXIF : Flash |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                                 |
|-------|--------------------------------------|
| 1     | /IFD/EXIF/{UShort = 37385}             |
| 2     | /IFD/XMP/ &lt; xmpstruct &gt; EXIF : Flash |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. Flash](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
