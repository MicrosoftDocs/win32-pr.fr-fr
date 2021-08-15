---
description: Stratégie de métadonnées de la photo pour la propriété System. Comment.
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: Stratégie de métadonnées de la photo System. Comment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b3511e0a459a2b652b29828060be6f0a92a36639aef63d4fa087e54ec9d80b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205628"
---
# <a name="systemcomment-photo-metadata-policy"></a>Stratégie de métadonnées de la photo System. Comment

Stratégie de métadonnées de la photo pour la propriété [System. Comment](../properties/props-system-comment.md) .

### <a name="pkey"></a>A-la

Commentaire de la barre d’ajout \_

### <a name="containers"></a>Containers

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



| Commande | Chemin                                | Format de disque    |
|-------|-------------------------------------|----------------|
| 1     | /App1/IFD/{UShort = 40092}            | \_octets Unicode |
| 2     | /App1/IFD/{UShort = 37510}            | unicode        |
| 3     | /XMP/ <xmpalt> EXIF : UserComment | unicode        |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                     | Format de disque    |
|-------|--------------------------|----------------|
| 1     | /App1/IFD/{UShort = 40092} | \_octets Unicode |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                          |
|-------|-------------------------------|
| 1     | /App1/IFD/{UShort = 40092}      |
| 2     | /App1/IFD/EXIF/{UShort = 37510} |
| 3     | /xmp/exif:UserComment         |



 

### <a name="tiff-policy"></a>Stratégie TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                                    | Format de disque    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{UShort = 40092}                     | \_octets Unicode |
| 2     | /IFD/{UShort = 37510}                     | unicode        |
| 3     | /IFD/XMP/ <xmpalt> EXIF : UserComment | unicode        |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                | Format de disque    |
|-------|---------------------|----------------|
| 1     | /IFD/{UShort = 40092} | \_octets Unicode |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                      |
|-------|---------------------------|
| 1     | /IFD/{UShort = 40092}       |
| 2     | /IFD/{UShort = 37510}       |
| 3     | /ifd/xmp/exif:UserComment |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. Comment](../properties/props-system-comment.md)
</dt> </dl>

 

 
