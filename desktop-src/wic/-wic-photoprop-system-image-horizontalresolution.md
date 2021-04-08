---
title: Stratégie de métadonnées de photo System. image. HorizontalResolution
description: Stratégie de métadonnées de la photo pour la propriété System. image. HorizontalResolution.
ms.assetid: 1fe73c50-4179-4ea4-be1c-9e103fb65d59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade406e644524fea84ef6baf957aed661d2adf07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756916"
---
# <a name="systemimagehorizontalresolution-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. image. HorizontalResolution

Stratégie de métadonnées de la photo pour la propriété [System. image. HorizontalResolution](../properties/props-system-image-horizontalresolution.md) .

### <a name="pkey"></a>A-la

Image de la \_ \_ HorizontalResolution

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui.

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur est générée par le système et ne peut pas être écrite directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                   | Format de disque |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{UShort = 282} |             |
| 2     | /xmp/tiff:XResolution  |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                        | Format de disque |
|-------|-----------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 282} |             |
| 2     | /xmp/tiff:xresolution       |             |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 282}    |             |
| 2     | /ifd/xmp/tiff:XResolution |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 282}    |             |
| 2     | /ifd/xmp/tiff:xresolution |             |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. image. HorizontalResolution](../properties/props-system-image-horizontalresolution.md)
</dt> </dl>

 

 
