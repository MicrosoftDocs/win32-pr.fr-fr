---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. CameraManufacturer.
ms.assetid: 6710161c-4835-4385-9d4c-566acc000925
title: Stratégie de métadonnées de photo System. photo. CameraManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1d2765b6c787b7d7ad421300f1c3492669830b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530723"
---
# <a name="systemphotocameramanufacturer-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. CameraManufacturer

Stratégie de métadonnées de la photo pour la propriété [System. photo. CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md) .

### <a name="pkey"></a>A-la

\_Photo \_ CameraManufacturer

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-type"></a>Type d’entrée

Chaîne.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                   | Format de disque |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{UShort = 271} | ascii       |
| 2     | /XMP/TIFF : Make         | unicode     |
| 3     | /XMP/TIFF : Make         | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                   | Format de disque |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{UShort = 271} | ascii       |
| 2     | /XMP/TIFF : Make         | unicode     |
| 3     | /XMP/TIFF : Make         | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                   |
|-------|------------------------|
| 1     | /App1/IFD/{UShort = 271} |
| 2     | /XMP/TIFF : Make         |
| 3     | /XMP/TIFF : Make         |



 

### <a name="tiff-policy"></a>Stratégie TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès               | Format de disque |
|-------|--------------------|-------------|
| 1     | /IFD/{UShort = 271}  | ascii       |
| 2     | /IFD/XMP/TIFF : Make | unicode     |
| 3     | /IFD/XMP/TIFF : Make | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès               | Format de disque |
|-------|--------------------|-------------|
| 1     | /IFD/{UShort = 271}  | ascii       |
| 2     | /IFD/XMP/TIFF : Make | unicode     |
| 3     | /IFD/XMP/TIFF : Make | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès               |
|-------|--------------------|
| 1     | /IFD/{UShort = 271}  |
| 2     | /IFD/XMP/TIFF : Make |
| 3     | /IFD/XMP/TIFF : Make |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md)
</dt> </dl>

 

 
