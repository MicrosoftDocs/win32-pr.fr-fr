---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. CameraSerialNumber.
ms.assetid: 85f78f45-5e76-4d52-88a2-ac3c9e2b6a1e
title: Stratégie de métadonnées de photo System. photo. CameraSerialNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a730df8041534a377262d9bb55a19c9b109b35ab03e47d1b7e8cb88014987b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710136"
---
# <a name="systemphotocameraserialnumber-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. CameraSerialNumber

Stratégie de métadonnées de la photo pour la propriété [System. photo. CameraSerialNumber](../properties/props-system-photo-cameraserialnumber.md) .

### <a name="pkey"></a>A-la

\_Photo \_ CameraSerialNumber

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

Si le fichier est au format JPEG, le gestionnaire lit, écrit et supprime les données du chemin d’accès suivant :



| Commande | Chemin                                   | Format de disque | Obligatoire |
|-------|----------------------------------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:CameraSerialNumber | Unicode     | Oui      |



 

### <a name="precedence-of-paths-tiff"></a>Priorité des chemins d’accès (TIFF)

Si le fichier est au format TIFF, le gestionnaire lira, écrira et supprime les données du chemin d’accès suivant



| Commande | Chemin                                       | Format de disque | Obligatoire |
|-------|--------------------------------------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:CameraSerialNumber | Unicode     | Oui      |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. CameraSerialNumber](../properties/props-system-photo-cameraserialnumber.md)
</dt> </dl>

 

 
