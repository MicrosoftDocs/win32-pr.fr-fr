---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. LightSource.
ms.assetid: 051a49ad-bb4c-459f-ae52-dc359a03a14a
title: Stratégie de métadonnées de photo System. photo. LightSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195d165a6a929c8e0b4bf2dd165a5f22068a8b75e8ea4dfcddb5b8979900b035
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204721"
---
# <a name="systemphotolightsource-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. LightSource

Stratégie de métadonnées de la photo pour la propriété [System. photo. lightsource](../properties/props-system-photo-lightsource.md) .

### <a name="pkey"></a>A-la

Photo de la \_ \_

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
| 1     | /App1/IFD/EXIF/{UShort = 37384} | ushort      |
| 2     | /XMP/EXIF : LightSource         | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37384} | ushort      |
| 2     | /XMP/EXIF : LightSource         | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37384} |
| 2     | /XMP/EXIF : lightsource         |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37384}  | ushort      |
| 2     | /IFD/XMP/EXIF : LightSource | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37384}  | ushort      |
| 2     | /IFD/XMP/EXIF : LightSource | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{UShort = 37384}  |
| 2     | /IFD/XMP/EXIF : lightsource |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. LightSource](../properties/props-system-photo-lightsource.md)
</dt> </dl>

 

 
