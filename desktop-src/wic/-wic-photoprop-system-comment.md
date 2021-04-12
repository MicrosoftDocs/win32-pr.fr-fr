---
description: Stratégie de métadonnées de la photo pour la propriété System. Comment.
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: Stratégie de métadonnées de la photo System. Comment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9d7526e05a72b073ac32bd8286a621b33ee62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320414"
---
# <a name="systemcomment-photo-metadata-policy"></a>Stratégie de métadonnées de la photo System. Comment

Stratégie de métadonnées de la photo pour la propriété [System. Comment](../properties/props-system-comment.md) .

### <a name="pkey"></a>A-la

Commentaire de la barre d’ajout \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-propvariant-type"></a>Type de PROPVARIANT d’entrée

VT \_ LPWStr ou VT \_ LPSTR

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                                | Format de disque    |
|-------|-------------------------------------|----------------|
| 1     | /App1/IFD/{UShort = 40092}            | \_octets Unicode |
| 2     | /App1/IFD/{UShort = 37510}            | unicode        |
| 3     | /XMP/ <xmpalt> EXIF : UserComment | unicode        |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                     | Format de disque    |
|-------|--------------------------|----------------|
| 1     | /App1/IFD/{UShort = 40092} | \_octets Unicode |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /App1/IFD/{UShort = 40092}      |
| 2     | /App1/IFD/EXIF/{UShort = 37510} |
| 3     | /xmp/exif:UserComment         |



 

### <a name="tiff-policy"></a>Stratégie TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                                    | Format de disque    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{UShort = 40092}                     | \_octets Unicode |
| 2     | /IFD/{UShort = 37510}                     | unicode        |
| 3     | /IFD/XMP/ <xmpalt> EXIF : UserComment | unicode        |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                | Format de disque    |
|-------|---------------------|----------------|
| 1     | /IFD/{UShort = 40092} | \_octets Unicode |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                      |
|-------|---------------------------|
| 1     | /IFD/{UShort = 40092}       |
| 2     | /IFD/{UShort = 37510}       |
| 3     | /ifd/xmp/exif:UserComment |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. Comment](../properties/props-system-comment.md)
</dt> </dl>

 

 
