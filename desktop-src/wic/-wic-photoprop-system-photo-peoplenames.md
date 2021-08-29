---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. PeopleNames.
ms.assetid: 567d5542-fc7b-4d19-bc3c-b9d6e26e3387
title: Stratégie de métadonnées de photo System. photo. PeopleNames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5540356001cdd33bb7c0d3340534f9c69e230a5d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886448"
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



| JSON | Chemin d’accès                                                           | Format de disque |
|-------|----------------------------------------------------------------|-------------|
| 1     | /XMP/ &lt; xmpstruct &gt; MP : RegionInfo/ &lt; Xmpbag &gt; MPRI : regions | ushort      |



 

### <a name="write-paths"></a>Chemins d’accès en écriture

Impossible d’écrire cette propriété à l’aide de la stratégie de métadonnées.

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                                |
|-------|-------------------------------------|
| 1     | /XMP/ &lt; xmpstruct &gt; MP : RegionInfo |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                                                               | Format de disque |
|-------|--------------------------------------------------------------------|-------------|
| 1     | /IFD/XMP/ &lt; xmpstruct &gt; MP : RegionInfo/ &lt; Xmpbag &gt; MPRI : regions | ushort      |



 

### <a name="write-paths"></a>Chemins d’accès en écriture

Impossible d’écrire cette propriété à l’aide de la stratégie de métadonnées.

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                                    |
|-------|-----------------------------------------|
| 1     | /IFD/XMP/ &lt; xmpstruct &gt; MP : RegionInfo |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. ProgramMode](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
