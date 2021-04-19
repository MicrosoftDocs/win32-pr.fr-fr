---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. PeopleNames.
ms.assetid: 567d5542-fc7b-4d19-bc3c-b9d6e26e3387
title: Stratégie de métadonnées de photo System. photo. PeopleNames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3de9f5adda67fcd0e555194500f109df078bdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535502"
---
# <a name="systemphotopeoplenames-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. PeopleNames

Stratégie de métadonnées de la photo pour la propriété [System. photo. PeopleNames](../properties/props-system-photo-peoplenames.md) .

### <a name="pkey"></a>A-la

\_Photo \_ PeopleNames

### <a name="containers"></a>Conteneurs

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



| Commande | Chemin d’accès                                                           | Format de disque |
|-------|----------------------------------------------------------------|-------------|
| 1     | /XMP/ <xmpstruct> MP : RegionInfo/ <xmpbag> MPRI : regions | ushort      |



 

### <a name="write-paths"></a>Chemins d’accès en écriture

Impossible d’écrire cette propriété à l’aide de la stratégie de métadonnées.

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                                |
|-------|-------------------------------------|
| 1     | /XMP/ <xmpstruct> MP : RegionInfo |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                                                               | Format de disque |
|-------|--------------------------------------------------------------------|-------------|
| 1     | /IFD/XMP/ <xmpstruct> MP : RegionInfo/ <xmpbag> MPRI : regions | ushort      |



 

### <a name="write-paths"></a>Chemins d’accès en écriture

Impossible d’écrire cette propriété à l’aide de la stratégie de métadonnées.

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                                    |
|-------|-----------------------------------------|
| 1     | /IFD/XMP/ <xmpstruct> MP : RegionInfo |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. ProgramMode](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
