---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. VersionID.
ms.assetid: d3c88243-8744-4bb3-ab47-38b5354f6f7e
title: Stratégie de métadonnées de photo System. GPS. VersionID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ca5bd1885f0ac5c3dc14dbb5e859de3f8a26cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536375"
---
# <a name="systemgpsversionid-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. VersionID

Stratégie de métadonnées de la photo pour la propriété [System. GPS. VersionId](../properties/props-system-gps-versionid.md) .

### <a name="pkey"></a>A-la

La \_ \_ VersionId GPS

### <a name="containers"></a>Conteneurs

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



| Commande | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 0} |             |
| 2     | /xmp/exif:GPSVersionID   | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 0} |             |
| 2     | /xmp/exif:GPSVersionID   | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{UShort = 0} |
| 2     | /xmp/exif:gpsversionid   |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 0}        |             |
| 2     | /ifd/xmp/exif:GPSVersionID | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 0}        |             |
| 2     | /ifd/xmp/exif:GPSVersionID | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                       |
|-------|----------------------------|
| 1     | /IFD/GPS/{UShort = 0}        |
| 2     | /ifd/xmp/exif:gpsversionid |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. VersionID](../properties/props-system-gps-versionid.md)
</dt> </dl>

 

 
