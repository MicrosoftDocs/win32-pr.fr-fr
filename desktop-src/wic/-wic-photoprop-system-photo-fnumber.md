---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. FNumber.
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: Stratégie de métadonnées de photo System. photo. FNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85443b849d9f810709f3e75c3082738e5377092f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443620"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. FNumber

Stratégie de métadonnées de la photo pour la propriété [System. photo. FNumber](../properties/props-system-photo-fnumber.md) .

### <a name="pkey"></a>A-la

\_Photo \_ FNumber

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur est générée à partir de System. photo. FNumberNumerator et de System. photo. FNumberDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 33437} |             |
| 2     | /xmp/exif:FNumber             |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 33437} |             |
| 2     | /xmp/exif:FNumber             |             | 
 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 33437} |
| 2     | /xmp/exif:fnumber             |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 33437} |             |
| 2     | /ifd/xmp/exif:FNumber    |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 33437} |             |
| 2     | /ifd/xmp/exif:FNumber    |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{UShort = 33437} |
| 2     | /ifd/xmp/exif:fnumber    |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. FNumber](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
