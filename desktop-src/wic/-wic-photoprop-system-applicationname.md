---
description: Stratégie de métadonnées de la photo pour la propriété System. ApplicationName.
ms.assetid: bf4b310a-7e63-45c5-a327-2638fb31d676
title: Stratégie de métadonnées de la photo System. ApplicationName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e36fac2a864cabfd7c1521d72357d187a8aea50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759507"
---
# <a name="systemapplicationname-photo-metadata-policy"></a>Stratégie de métadonnées de la photo System. ApplicationName

Stratégie de métadonnées de la photo pour la propriété [System. ApplicationName](../properties/props-system-applicationname.md) .

### <a name="pkey"></a>A-la

$ $ \_ Nom_application ApplicationName

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-type"></a>Type d’entrée

String

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                                         | Format de disque |
|-------|----------------------------------------------|-------------|
|       | /App1/IFD/{UShort = 305}                       | ascii       |
|       | Programme/app13/irb/8bimiptc/iptc/Originating |             |
|       | /xmp/xmp:CreatorTool                         | unicode     |
|       | /xmp/xmp:creatortool                         | unicode     |
|       | /XMP/TIFF : logiciel                           | unicode     |
|       | /XMP/TIFF : logiciel                           | unicode     |
|       | Programme/app13/irb/8bimiptc/iptc/Originating |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                                         | Format de disque |
|-------|----------------------------------------------|-------------|
|       | /App1/IFD/{UShort = 305}                       | ascii       |
|       | /xmp/xmp:CreatorTool                         | unicode     |
|       | /xmp/xmp:creatortool                         | unicode     |
|       | /XMP/TIFF : logiciel                           | unicode     |
|       | /XMP/TIFF : logiciel                           | unicode     |
|       | Programme/app13/irb/8bimiptc/iptc/Originating |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                                         |
|-------|----------------------------------------------|
|       | /App1/IFD/{UShort = 305}                       |
|       | /xmp/xmp:CreatorTool                         |
|       | /xmp/xmp:creatortool                         |
|       | /XMP/TIFF : logiciel                           |
|       | /XMP/TIFF : logiciel                           |
|       | Programme/app13/irb/8bimiptc/iptc/Originating |



 

### <a name="tiff-policy"></a>Stratégie TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                                       | Format de disque |
|-------|--------------------------------------------|-------------|
|       | /IFD/{UShort = 305}                          | ascii       |
|       | Programme/ifd/iptc/Originating              |             |
|       | /ifd/xmp/xmp:CreatorTool                   | unicode     |
|       | /ifd/xmp/xmp:creatortool                   | unicode     |
|       | /IFD/XMP/TIFF : logiciel                     | unicode     |
|       | /IFD/XMP/TIFF : logiciel                     | unicode     |
|       | Programme/ifd/iptc/Originating              |             |
|       | Programme/ifd/irb/8bimiptc/iptc/Originating |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                                       | Format de disque |
|-------|--------------------------------------------|-------------|
|       | /IFD/{UShort = 305}                          | ascii       |
|       | /ifd/xmp/xmp:CreatorTool                   | unicode     |
|       | /ifd/xmp/xmp:creatortool                   | unicode     |
|       | /IFD/XMP/TIFF : logiciel                     | unicode     |
|       | /IFD/XMP/TIFF : logiciel                     | unicode     |
|       | Programme/ifd/iptc/Originating              |             |
|       | Programme/ifd/irb/8bimiptc/iptc/Originating |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                                       |
|-------|--------------------------------------------|
|       | /IFD/{UShort = 305}                          |
|       | /ifd/xmp/xmp:CreatorTool                   |
|       | /ifd/xmp/xmp:creatortool                   |
|       | /IFD/XMP/TIFF : logiciel                     |
|       | /IFD/XMP/TIFF : logiciel                     |
|       | Programme/ifd/iptc/Originating              |
|       | Programme/ifd/irb/8bimiptc/iptc/Originating |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. ApplicationName](../properties/props-system-applicationname.md)
</dt> </dl>

 

 
