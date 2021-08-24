---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. VersionID.
ms.assetid: d3c88243-8744-4bb3-ab47-38b5354f6f7e
title: Stratégie de métadonnées de photo System. GPS. VersionID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857ecb6b172dafa2a771d9e81f8b570a89f458c79b7630a2f231ce84dbec4f9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706359"
---
# <a name="systemgpsversionid-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. VersionID

Stratégie de métadonnées de la photo pour la propriété [System. GPS. VersionId](../properties/props-system-gps-versionid.md) .

### <a name="pkey"></a>A-la

La \_ \_ VersionId GPS

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_ \| interface utilisateur VT Vector VT \_

### <a name="input-type"></a>Type d’entrée

Buffer

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policies"></a>Stratégies JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 0} |             |
| 2     | /xmp/exif:GPSVersionID   | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 0} |             |
| 2     | /xmp/exif:GPSVersionID   | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{UShort = 0} |
| 2     | /xmp/exif:gpsversionid   |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 0}        |             |
| 2     | /ifd/xmp/exif:GPSVersionID | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 0}        |             |
| 2     | /ifd/xmp/exif:GPSVersionID | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                       |
|-------|----------------------------|
| 1     | /IFD/GPS/{UShort = 0}        |
| 2     | /ifd/xmp/exif:gpsversionid |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. VersionID](../properties/props-system-gps-versionid.md)
</dt> </dl>

 

 
