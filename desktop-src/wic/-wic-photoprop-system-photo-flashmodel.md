---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. FlashModel.
ms.assetid: ef322823-1b87-40ea-a5e3-e7551f14e44d
title: Stratégie de métadonnées de photo System. photo. FlashModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ade3769cb0d852239af84b769b85d5b3849589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539111"
---
# <a name="systemphotoflashmodel-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. FlashModel

Stratégie de métadonnées de la photo pour la propriété [System. photo. FlashModel](../properties/props-system-photo-flashmodel.md) .

### <a name="pkey"></a>A-la

\_Photo \_ FlashModel

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



| Commande | Chemin d’accès                           | Format de disque | Format de données | Obligatoire |
|-------|--------------------------------|-------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:FlashModel | Unicode     |             | Oui      |



 

### <a name="precedence-of-paths-tiff"></a>Priorité des chemins d’accès (TIFF)

Si le fichier est au format TIFF, le gestionnaire utilise l’ordre de priorité suivant lors de la lecture ou de l’écriture des données.



| Commande | Chemin d’accès                               | Format de disque | Format de données | Obligatoire |
|-------|------------------------------------|-------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:FlashModel | Unicode     |             | Oui      |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. FlashModel](../properties/props-system-photo-flashmodel.md)
</dt> </dl>

 

 
