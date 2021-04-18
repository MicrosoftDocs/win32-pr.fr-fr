---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. ExposureBias.
ms.assetid: 00ebe037-0116-4d75-868b-d75b3e58a84d
title: Stratégie de métadonnées de photo System. photo. ExposureBias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709aa21da7cec56d36b5de643681a592873717bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526145"
---
# <a name="systemphotoexposurebias-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. ExposureBias

Stratégie de métadonnées de la photo pour la propriété [System. photo. ExposureBias](../properties/props-system-photo-exposurebias.md) .

### <a name="pkey"></a>A-la

\_Photo \_ ExposureBias

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur est générée à partir de System. photo. ExposureBiasNumerator et de System. photo. ExposureBiasDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37380} |             |
| 2     | /xmp/exif:ExposureBiasValue   |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37380} |             |
| 2     | /xmp/exif:ExposureBiasValue   |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37380} |
| 2     | /xmp/exif:exposurebiasvalue   |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                            | Format de disque |
|-------|---------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37380}        |             |
| 2     | /ifd/xmp/exif:ExposureBiasValue |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                            | Format de disque |
|-------|---------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37380}        |             |
| 2     | /ifd/xmp/exif:ExposureBiasValue |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                            |
|-------|---------------------------------|
| 1     | /IFD/EXIF/{UShort = 37380}        |
| 2     | /ifd/xmp/exif:exposurebiasvalue |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. ExposureBias](../properties/props-system-photo-exposurebias.md)
</dt> </dl>

 

 
