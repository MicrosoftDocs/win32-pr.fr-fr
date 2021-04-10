---
description: Stratégie de métadonnées de la photo pour la propriété System. SimpleRating.
ms.assetid: d932a251-f238-4582-a1c4-cf4855f26fb3
title: Stratégie de métadonnées de photo System. SimpleRating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b91e41a0684c8e395992683e0a1d4fe43306a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035024"
---
# <a name="systemsimplerating-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. SimpleRating

Stratégie de métadonnées de la photo pour la propriété [System. SimpleRating](../properties/props-system-simplerating.md) .

### <a name="pkey"></a>A-la

SimpleRating de la \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ UI4

### <a name="input-propvariant-type"></a>Type de PROPVARIANT d’entrée

Peut être VT \_ UI1, VT \_ UI2 ou VT \_ UI4. La valeur entière peut être comprise entre 0 et 5.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/{UShort = 18246} | ushort      |
| 2     | /XMP/XMP : évaluation          | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/{UShort = 18246} | ushort      |
| 2     | /XMP/XMP : évaluation          | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                     |
|-------|--------------------------|
| 1     | /App1/IFD/{UShort = 18246} |
| 2     | /XMP/XMP : évaluation          |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                | Format de disque |
|-------|---------------------|-------------|
| 1     | /IFD/{UShort = 18246} | ushort      |
| 2     | /IFD/XMP/XMP : évaluation | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                | Format de disque |
|-------|---------------------|-------------|
| 1     | /IFD/{UShort = 18246} | ushort      |
| 2     | /IFD/XMP/XMP : évaluation | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                |
|-------|---------------------|
| 1     | /IFD/{UShort = 18246} |
| 2     | /IFD/XMP/XMP : évaluation |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. SimpleRating](../properties/props-system-simplerating.md)
</dt> </dl>

 

 
