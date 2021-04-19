---
description: Stratégie de métadonnées de la photo pour la propriété System. image. VerticalResolution.
ms.assetid: a58b7463-3572-4ca8-8299-93d92d2f06fb
title: Stratégie de métadonnées de la photo System. image. VerticalResolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e895ef9e1181a3ec40b474940c6dfaaa3e1329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527510"
---
# <a name="systemimageverticalresolution-photo-metadata-policy"></a>Stratégie de métadonnées de la photo System. image. VerticalResolution

Stratégie de métadonnées de la photo pour la propriété [System. image. VerticalResolution](../properties/props-system-image-verticalresolution.md) .

### <a name="pkey"></a>A-la

Image de l’image de la trop propre \_ \_

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
| 1     | /App1/IFD/{UShort = 283} |             |
| 2     | /xmp/tiff:YResolution  |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                        |
|-------|-----------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 283} |
| 2     | /xmp/tiff:yresolution       |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 283}    |             |
| 2     | /ifd/xmp/tiff:YResolution |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{UShort = 283}    |
| 2     | /ifd/xmp/tiff:yresolution |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. image. VerticalResolution](../properties/props-system-image-verticalresolution.md)
</dt> </dl>

 

 
