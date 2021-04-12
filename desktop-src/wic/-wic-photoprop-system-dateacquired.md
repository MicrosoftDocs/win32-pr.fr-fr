---
description: Stratégie de métadonnées de la photo pour la propriété System. DateAcquired.
ms.assetid: 04a61ecc-d168-4f93-b143-3e6ba8aaf322
title: Stratégie de métadonnées de photo System. DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f126ccb4424d1489f671f61f719a505559a78c8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210282"
---
# <a name="systemdateacquired-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. DateAcquired

Stratégie de métadonnées de la photo pour la propriété [System. DateAcquired](../properties/props-system-dateacquired.md) .

### <a name="pkey"></a>A-la

DateAcquired de la \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

de VT \_ fileTime

### <a name="input-propvariant-type"></a>Type de PROPVARIANT d’entrée

de VT \_ fileTime

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="precedence-of-paths-jpeg"></a>Priorité des chemins d’accès (JPEG)

Si le fichier est au format JPEG, le gestionnaire recherche les données dans l’ordre suivant :



| Commande | Chemin d’accès                             | Format de disque                        | Obligatoire |
|-------|----------------------------------|------------------------------------|----------|
| 1     | /xmp/MicrosoftPhoto:DateAcquired | Chaîne Unicode au format de date XMP. | Oui      |



 

### <a name="precedence-of-paths-tiff"></a>Priorité des chemins d’accès (TIFF)

Si le fichier est au format TIFF, le gestionnaire recherche les données dans l’ordre suivant :



| Commande | Chemin d’accès                                 | Format de disque                        | Obligatoire |
|-------|--------------------------------------|------------------------------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:DateAcquired | Chaîne Unicode au format de date XMP. | Oui      |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. DateAcquired](../properties/props-system-dateacquired.md)
</dt> </dl>

 

 
