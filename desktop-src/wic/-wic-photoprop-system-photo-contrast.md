---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. Contrast.
ms.assetid: c5e2589d-507c-4b92-9ada-7d64e7c45dd8
title: Stratégie de métadonnées de photo System. photo. Contrast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a9309ecab96a2244e08ebf05ff8896c792f7366c9db21d41072d2d94aacf47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087095"
---
# <a name="systemphotocontrast-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. Contrast

Stratégie de métadonnées de la photo pour la propriété [System. photo. Contrast](../properties/props-system-photo-contrast.md) .

### <a name="pkey"></a>A-la

\_Contraste de photo de la \_

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
| 1     | /App1/IFD/EXIF/{UShort = 41992} | ushort      |
| 2     | /XMP/EXIF : contraste            | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41992} | ushort      |
| 2     | /XMP/EXIF : contraste            | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 41992} |
| 2     | /XMP/EXIF : contraste            |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41992} | ushort      |
| 2     | /IFD/XMP/EXIF : contraste   | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41992} | ushort      |
| 2     | /IFD/XMP/EXIF : contraste   | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{UShort = 41992} |
| 2     | /IFD/XMP/EXIF : contraste   |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. Contrast](../properties/props-system-photo-contrast.md)
</dt> </dl>

 

 
