---
description: La stratégie de métadonnées de la photo pour la propriété System. GPS. Status.
ms.assetid: 74ea0384-3b1f-4d5e-8713-7b3936813a3a
title: Stratégie de métadonnées de photo System. GPS. Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a99237b9fe14d9adbc97dd5de95158a8aa714caaa4a0a8440d9f3798a2155d20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710514"
---
# <a name="systemgpsstatus-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. Status

La stratégie de métadonnées de la photo pour la propriété [System. GPS. Status](../properties/props-system-gps-status.md) .

### <a name="pkey"></a>A-la

\_État du GPS \_

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-propvariant-type"></a>Type de PROPVARIANT d’entrée

VT \_ LPWStr est préféré, mais VT \_ LPSTR est également accepté.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policies"></a>Stratégies JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 9} | ascii       |
| 2     | /xmp/exif:GPSStatus      | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 9} | ascii       |
| 2     | /xmp/exif:GPSStatus      | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{UShort = 9} |
| 2     | /xmp/exif:gpsstatus      |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                    | Format de disque |
|-------|-------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 9}     | ascii       |
| 2     | /ifd/xmp/exif:GPSStatus | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                    | Format de disque |
|-------|-------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 9}     | ascii       |
| 2     | /ifd/xmp/exif:GPSStatus | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                    |
|-------|-------------------------|
| 1     | /IFD/GPS/{UShort = 9}     |
| 2     | /ifd/xmp/exif:gpsstatus |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. Status](../properties/props-system-gps-status.md)
</dt> </dl>

 

 
