---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. ExposureBias.
ms.assetid: 00ebe037-0116-4d75-868b-d75b3e58a84d
title: Stratégie de métadonnées de photo System. photo. ExposureBias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5692876182dfc200ea6b89d022d97c8dfc5b518157593ec9f79de9cf0d043564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032586"
---
# <a name="systemphotoexposurebias-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. ExposureBias

Stratégie de métadonnées de la photo pour la propriété [System. photo. ExposureBias](../properties/props-system-photo-exposurebias.md) .

### <a name="pkey"></a>A-la

\_Photo \_ ExposureBias

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur est générée à partir de System. photo. ExposureBiasNumerator et de System. photo. ExposureBiasDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37380} |             |
| 2     | /xmp/exif:ExposureBiasValue   |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37380} |             |
| 2     | /xmp/exif:ExposureBiasValue   |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37380} |
| 2     | /xmp/exif:exposurebiasvalue   |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                            | Format de disque |
|-------|---------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37380}        |             |
| 2     | /ifd/xmp/exif:ExposureBiasValue |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                            | Format de disque |
|-------|---------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37380}        |             |
| 2     | /ifd/xmp/exif:ExposureBiasValue |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                            |
|-------|---------------------------------|
| 1     | /IFD/EXIF/{UShort = 37380}        |
| 2     | /ifd/xmp/exif:exposurebiasvalue |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. ExposureBias](../properties/props-system-photo-exposurebias.md)
</dt> </dl>

 

 
