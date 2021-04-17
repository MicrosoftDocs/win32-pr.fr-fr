---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. LightSource.
ms.assetid: 051a49ad-bb4c-459f-ae52-dc359a03a14a
title: Stratégie de métadonnées de photo System. photo. LightSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9b3d31f01cdd2bea8d3fabbbc730a41f1fb0da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529937"
---
# <a name="systemphotolightsource-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. LightSource

Stratégie de métadonnées de la photo pour la propriété [System. photo. lightsource](../properties/props-system-photo-lightsource.md) .

### <a name="pkey"></a>A-la

Photo de la \_ \_

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
| 1     | /App1/IFD/EXIF/{UShort = 37384} | ushort      |
| 2     | /XMP/EXIF : LightSource         | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37384} | ushort      |
| 2     | /XMP/EXIF : LightSource         | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37384} |
| 2     | /XMP/EXIF : lightsource         |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37384}  | ushort      |
| 2     | /IFD/XMP/EXIF : LightSource | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37384}  | ushort      |
| 2     | /IFD/XMP/EXIF : LightSource | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{UShort = 37384}  |
| 2     | /IFD/XMP/EXIF : lightsource |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. LightSource](../properties/props-system-photo-lightsource.md)
</dt> </dl>

 

 
