---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. LensModel.
ms.assetid: 39aeff17-e8d3-4ceb-86a1-1749d2ca98d6
title: Stratégie de métadonnées de photo System. photo. LensModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07fff44e14a04dab220f8dbce243a638710f30db253c43c1ff79a240bb32f3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441869"
---
# <a name="systemphotolensmodel-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. LensModel

Stratégie de métadonnées de la photo pour la propriété [System. photo. LensModel](../properties/props-system-photo-lensmodel.md) .

### <a name="pkey"></a>A-la

\_Photo \_ LensModel

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



| Commande | Chemin                          | Format de disque | Obligatoire |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:LensModel | Unicode     | Oui      |



 

### <a name="precedence-of-paths-tiff"></a>Priorité des chemins d’accès (TIFF)

Si le fichier est au format TIFF, le gestionnaire utilise l’ordre de priorité suivant lors de la lecture ou de l’écriture des données.



| Commande | Chemin                              | Format de disque | Obligatoire |
|-------|-----------------------------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:LensModel | Unicode     | Oui      |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. LensModel](../properties/props-system-photo-lensmodel.md)
</dt> </dl>

 

 
