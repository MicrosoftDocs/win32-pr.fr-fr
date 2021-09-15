---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. FlashManufacturer.
ms.assetid: f62e85ec-2dc6-456b-a43b-7b76d162b608
title: Stratégie de métadonnées de photo System. photo. FlashManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa1e785dfd00662acf065021a3c80de5c587586c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404236"
---
# <a name="systemphotoflashmanufacturer-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. FlashManufacturer

Stratégie de métadonnées de la photo pour la propriété [System. photo. FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md) .

### <a name="pkey"></a>A-la

\_Photo \_ FlashManufacturer

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



| JSON | Chemin d’accès                                  | Format de disque | Format de données | Obligatoire |
|-------|---------------------------------------|-------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:FlashManufacturer | Unicode     |             | Oui      |



 

### <a name="precedence-of-paths-tiff"></a>Priorité des chemins d’accès (TIFF)

Si le fichier est au format TIFF, le gestionnaire utilise l’ordre de priorité suivant lors de la lecture ou de l’écriture des données.



| JSON | Chemin d’accès                                      | Format de disque | Format de données | Obligatoire |
|-------|-------------------------------------------|-------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:FlashManufacturer | Unicode     |             | Oui      |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md)
</dt> </dl>

 

 
