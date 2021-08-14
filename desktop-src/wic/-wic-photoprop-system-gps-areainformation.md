---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. AreaInformation.
ms.assetid: d9ecb00b-1f97-4f53-909f-30231104d398
title: Stratégie de métadonnées de photo System. GPS. AreaInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4eee2cf4234902049241c833d1077814f5daf88187323c43bc1cb00f6f44aa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205520"
---
# <a name="systemgpsareainformation-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. AreaInformation

Stratégie de métadonnées de la photo pour la propriété [System. GPS. AreaInformation](../properties/props-system-gps-areainformation.md) .

### <a name="pkey"></a>A-la

\_AreaInformation GPS \_

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

### <a name="jpeg-policies"></a>Stratégies JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                         | Format de disque |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 28}    |             |
| 2     | /xmp/exif:GPSAreaInformation | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                         | Format de disque |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 28}    |             |
| 2     | /xmp/exif:GPSAreaInformation | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                         |
|-------|------------------------------|
| 1     | /App1/IFD/GPS/{UShort = 28}    |
| 2     | /xmp/exif:GPSAreaInformation |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                             | Format de disque |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 28}             |             |
| 2     | /ifd/xmp/exif:GPSAreaInformation | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                             | Format de disque |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 28}             |             |
| 2     | /ifd/xmp/exif:GPSAreaInformation | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                             |
|-------|----------------------------------|
| 1     | /IFD/GPS/{UShort = 28}             |
| 2     | /ifd/xmp/exif:GPSAreaInformation |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. AreaInformation](../properties/props-system-gps-areainformation.md)
</dt> </dl>

 

 
