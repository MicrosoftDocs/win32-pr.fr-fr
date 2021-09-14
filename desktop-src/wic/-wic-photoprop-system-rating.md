---
description: Stratégie de métadonnées de la photo pour la propriété System. Rating.
ms.assetid: e4d2c12e-617a-431e-9062-62acf6ef21c8
title: Stratégie de métadonnées de photo System. Rating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4f7d89b1ff1ea8326c2d26fba0d331db1eab1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295959"
---
# <a name="systemrating-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. Rating

Stratégie de métadonnées de la photo pour la propriété [System. Rating](../properties/props-system-rating.md) .

### <a name="pkey"></a>A-la

Notation de la- \_ catégorie

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ UI4

### <a name="input-propvariant-type"></a>Type de PROPVARIANT d’entrée

Peut être VT \_ UI1, VT \_ UI2 ou VT \_ UI4. La valeur peut être comprise entre 0 et 99.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /App1/IFD/{UShort = 18249}   | ushort      |
| 2     | /xmp/MicrosoftPhoto : évaluation | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /App1/IFD/{UShort = 18249}   | ushort      |
| 2     | /xmp/MicrosoftPhoto : évaluation | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                       |
|-------|----------------------------|
| 1     | /App1/IFD/{UShort = 18249}   |
| 2     | /XMP/microsoftphoto : évaluation |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                           | Format de disque |
|-------|--------------------------------|-------------|
| 1     | /IFD/{UShort = 18249}            | ushort      |
| 2     | /ifd/xmp/MicrosoftPhoto : évaluation | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                           | Format de disque |
|-------|--------------------------------|-------------|
| 1     | /IFD/{UShort = 18249}            | ushort      |
| 2     | /ifd/xmp/MicrosoftPhoto : évaluation | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                           |
|-------|--------------------------------|
| 1     | /IFD/{UShort = 18249}            |
| 2     | /IFD/XMP/microsoftphoto : évaluation |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. Rating](../properties/props-system-rating.md)
</dt> </dl>

 

 
