---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. LensManufacturer.
ms.assetid: ee25da96-982f-475e-8957-e24ef7721b78
title: Stratégie de métadonnées de photo System. photo. LensManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6696e7113a14a9b5b26a26f38258f30a5ba82cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204220"
---
# <a name="systemphotolensmanufacturer-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. LensManufacturer

Stratégie de métadonnées de la photo pour la propriété [System. photo. LensManufacturer](../properties/props-system-photo-lensmanufacturer.md) .

### <a name="pkey"></a>A-la

\_Photo \_ LensManufacturer

### <a name="containers"></a>Conteneurs

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



| Commande | Chemin d’accès                                 | Format de disque | Obligatoire |
|-------|--------------------------------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:LensManufacturer | Unicode     | Oui      |



 

### <a name="precedence-of-paths-tiff"></a>Priorité des chemins d’accès (TIFF)

Si le fichier est au format TIFF, le gestionnaire utilise l’ordre de priorité suivant lors de la lecture ou de l’écriture des données.



| Commande | Chemin d’accès                                     | Format de disque | Obligatoire |
|-------|------------------------------------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:LensManufacturer | Unicode     | Oui      |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. LensManufacturer](../properties/props-system-photo-lensmanufacturer.md)
</dt> </dl>

 

 
