---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. LensManufacturer.
ms.assetid: ee25da96-982f-475e-8957-e24ef7721b78
title: Stratégie de métadonnées de photo System. photo. LensManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f6beebc06ce690b05da62c023480bec25b675a7a9ec6093cec1752ac3a0e343
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881981"
---
# <a name="systemphotolensmanufacturer-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. LensManufacturer

Stratégie de métadonnées de la photo pour la propriété [System. photo. LensManufacturer](../properties/props-system-photo-lensmanufacturer.md) .

### <a name="pkey"></a>A-la

\_Photo \_ LensManufacturer

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-type"></a>Type d’entrée

Chaîne.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="precedence-of-paths-jpeg"></a>Priorité des chemins d’accès (JPEG)

Si le fichier est au format JPEG, le gestionnaire utilise le chemin d’accès suivant lors de la lecture ou de l’écriture des données.



| Commande | Chemin                                 | Format de disque | Obligatoire |
|-------|--------------------------------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:LensManufacturer | Unicode     | Oui      |



 

### <a name="precedence-of-paths-tiff"></a>Priorité des chemins d’accès (TIFF)

Si le fichier est au format TIFF, le gestionnaire utilise l’ordre de priorité suivant lors de la lecture ou de l’écriture des données.



| Commande | Chemin                                     | Format de disque | Obligatoire |
|-------|------------------------------------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:LensManufacturer | Unicode     | Oui      |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. LensManufacturer](../properties/props-system-photo-lensmanufacturer.md)
</dt> </dl>

 

 
