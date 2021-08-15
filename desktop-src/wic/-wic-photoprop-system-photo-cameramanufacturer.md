---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. CameraManufacturer.
ms.assetid: 6710161c-4835-4385-9d4c-566acc000925
title: Stratégie de métadonnées de photo System. photo. CameraManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37744420babedf6b398cdf3ab9007c3895c09d33b9254221b5ba4760ab917a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087085"
---
# <a name="systemphotocameramanufacturer-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. CameraManufacturer

Stratégie de métadonnées de la photo pour la propriété [System. photo. CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md) .

### <a name="pkey"></a>A-la

\_Photo \_ CameraManufacturer

### <a name="containers"></a>Containers

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



| Commande | Chemin                   | Format de disque |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{UShort = 271} | ascii       |
| 2     | /XMP/TIFF : Make         | unicode     |
| 3     | /XMP/TIFF : Make         | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                   | Format de disque |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{UShort = 271} | ascii       |
| 2     | /XMP/TIFF : Make         | unicode     |
| 3     | /XMP/TIFF : Make         | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                   |
|-------|------------------------|
| 1     | /App1/IFD/{UShort = 271} |
| 2     | /XMP/TIFF : Make         |
| 3     | /XMP/TIFF : Make         |



 

### <a name="tiff-policy"></a>Stratégie TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin               | Format de disque |
|-------|--------------------|-------------|
| 1     | /IFD/{UShort = 271}  | ascii       |
| 2     | /IFD/XMP/TIFF : Make | unicode     |
| 3     | /IFD/XMP/TIFF : Make | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin               | Format de disque |
|-------|--------------------|-------------|
| 1     | /IFD/{UShort = 271}  | ascii       |
| 2     | /IFD/XMP/TIFF : Make | unicode     |
| 3     | /IFD/XMP/TIFF : Make | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin               |
|-------|--------------------|
| 1     | /IFD/{UShort = 271}  |
| 2     | /IFD/XMP/TIFF : Make |
| 3     | /IFD/XMP/TIFF : Make |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md)
</dt> </dl>

 

 
