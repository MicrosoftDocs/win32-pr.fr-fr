---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. CameraModel.
ms.assetid: ff85e6ee-dc75-45bc-a406-2290b012c22d
title: Stratégie de métadonnées de photo System. photo. CameraModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e205d4d886d050e45b958f2ba0f06c6411584c4a96a717378f243e5d1dd4fae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882049"
---
# <a name="systemphotocameramodel-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. CameraModel

Stratégie de métadonnées de la photo pour la propriété [System. photo. CameraModel](../properties/props-system-photo-cameramodel.md) .

### <a name="pkey"></a>A-la

\_Photo \_ CameraModel

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
| 1     | /App1/IFD/{UShort = 272} | ascii       |
| 2     | /XMP/TIFF : modèle        | unicode     |
| 3     | /XMP/TIFF : modèle        | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                   | Format de disque |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{UShort = 272} | ascii       |
| 2     | /XMP/TIFF : modèle        | unicode     |
| 3     | /XMP/TIFF : modèle        | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                   |
|-------|------------------------|
| 1     | /App1/IFD/{UShort = 272} |
| 2     | /XMP/TIFF : modèle        |
| 3     | /XMP/TIFF : modèle        |



 

### <a name="tiff-policy"></a>Stratégie TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                | Format de disque |
|-------|---------------------|-------------|
| 1     | /IFD/{UShort = 272}   | ascii       |
| 2     | /IFD/XMP/TIFF : modèle | unicode     |
| 3     | /IFD/XMP/TIFF : modèle | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                | Format de disque |
|-------|---------------------|-------------|
| 1     | /IFD/{UShort = 272}   | ascii       |
| 2     | /IFD/XMP/TIFF : modèle | unicode     |
| 3     | /IFD/XMP/TIFF : modèle | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                |
|-------|---------------------|
| 1     | /IFD/{UShort = 272}   |
| 2     | /IFD/XMP/TIFF : modèle |
| 3     | /IFD/XMP/TIFF : modèle |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. CameraModel](../properties/props-system-photo-cameramodel.md)
</dt> </dl>

 

 
