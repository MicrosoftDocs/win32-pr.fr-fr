---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. PhotometricInterpretation.
ms.assetid: ff36b2c3-8763-4640-a049-b5880fd26929
title: Stratégie de métadonnées de photo System. photo. PhotometricInterpretation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b371ce9257d526f941f3fdb33949e8788a7112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523338"
---
# <a name="systemphotophotometricinterpretation-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. PhotometricInterpretation

Stratégie de métadonnées de la photo pour la propriété [System. photo. PhotometricInterpretation](../properties/props-system-photo-photometricinterpretation.md) .

### <a name="pkey"></a>A-la

\_Photo \_ PhotometricInterpretation

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_UI2 VT

### <a name="input-type"></a>Type d’entrée

UShort

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                                | Format de disque |
|-------|-------------------------------------|-------------|
| 1     | /App1/IFD/{UShort = 262}              | ushort      |
| 2     | /xmp/tiff:PhotometricInterpretation | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                                | Format de disque |
|-------|-------------------------------------|-------------|
| 1     | /App1/IFD/{UShort = 262}              | ushort      |
| 2     | /xmp/tiff:PhotometricInterpretation | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                                |
|-------|-------------------------------------|
| 1     | /App1/IFD/{UShort = 262}              |
| 2     | /xmp/tiff:photometricinterpretation |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                                    | Format de disque |
|-------|-----------------------------------------|-------------|
| 1     | /IFD/{UShort = 262}                       | ushort      |
| 2     | /ifd/xmp/tiff:PhotometricInterpretation | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                                    | Format de disque |
|-------|-----------------------------------------|-------------|
| 1     | /IFD/{UShort = 262}                       | ushort      |
| 2     | /ifd/xmp/tiff:PhotometricInterpretation | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                                    |
|-------|-----------------------------------------|
| 1     | /IFD/{UShort = 262}                       |
| 2     | /ifd/xmp/tiff:photometricinterpretation |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. PhotometricInterpretation](../properties/props-system-photo-photometricinterpretation.md)
</dt> </dl>

 

 
