---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. PeopleNames.
ms.assetid: 567d5542-fc7b-4d19-bc3c-b9d6e26e3387
title: Stratégie de métadonnées de photo System. photo. PeopleNames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4118cc8242d6dfe8a91d0bcd2b6039095fdf180037f51205d3541b9aefa2cc0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087048"
---
# <a name="systemphotopeoplenames-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. PeopleNames

Stratégie de métadonnées de la photo pour la propriété [System. photo. PeopleNames](../properties/props-system-photo-peoplenames.md) .

### <a name="pkey"></a>A-la

\_Photo \_ PeopleNames

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT Vector \| VT \_

### <a name="input-type"></a>Type d’entrée

StringMulti

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                                                           | Format de disque |
|-------|----------------------------------------------------------------|-------------|
| 1     | /XMP/ <xmpstruct> MP : RegionInfo/ <xmpbag> MPRI : regions | ushort      |



 

### <a name="write-paths"></a>Chemins d’accès en écriture

Impossible d’écrire cette propriété à l’aide de la stratégie de métadonnées.

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                                |
|-------|-------------------------------------|
| 1     | /XMP/ <xmpstruct> MP : RegionInfo |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                                                               | Format de disque |
|-------|--------------------------------------------------------------------|-------------|
| 1     | /IFD/XMP/ <xmpstruct> MP : RegionInfo/ <xmpbag> MPRI : regions | ushort      |



 

### <a name="write-paths"></a>Chemins d’accès en écriture

Impossible d’écrire cette propriété à l’aide de la stratégie de métadonnées.

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                                    |
|-------|-----------------------------------------|
| 1     | /IFD/XMP/ <xmpstruct> MP : RegionInfo |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. ProgramMode](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
