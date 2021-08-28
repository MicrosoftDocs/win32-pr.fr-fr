---
description: Stratégie de métadonnées de la photo pour la propriété System. Copyright.
ms.assetid: 84d2f55b-5ca4-4912-b038-c18a72e6fc34
title: Stratégie de métadonnées de photos System. Copyright
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3e17190205b3df5c2ede9b1a7db231d0fdbbe21
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882700"
---
# <a name="systemcopyright-photo-metadata-policy"></a>Stratégie de métadonnées de photos System. Copyright

Stratégie de métadonnées de la photo pour la propriété [System. Copyright](../properties/props-system-copyright.md) .

### <a name="pkey"></a>A-la

Copyright de la présente \_

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-propvariant-type"></a>Type de PROPVARIANT d’entrée

Chaîne

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                                      | Format de disque |
|-------|-------------------------------------------|-------------|
|       | /App1/IFD/{UShort = 33432}                  | ascii       |
|       | Avis/APP13/IRB/8bimiptc/IPTC/Copyright |             |
|       | /XMP/ &lt; xmpalt &gt; DC : droits              | unicode     |
|       | /XMP/DC : droits                            | unicode     |
|       | Avis/APP13/IRB/8bimiptc/IPTC/Copyright |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                                      | Format de disque |
|-------|-------------------------------------------|-------------|
|       | /XMP/DC : droits                            | unicode     |
|       | /XMP/ &lt; xmpalt &gt; DC : droits              | unicode     |
|       | Avis/APP13/IRB/8bimiptc/IPTC/Copyright |             |
|       | /App1/IFD/{UShort = 33432}                  | ascii       |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                                      |
|-------|-------------------------------------------|
|       | /XMP/DC : droits                            |
|       | Avis/APP13/IRB/8bimiptc/IPTC/Copyright |
|       | /App1/IFD/{UShort = 33432}                  |



 

### <a name="tiff-policy"></a>Stratégie TIFF

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                                    | Format de disque |
|-------|-----------------------------------------|-------------|
|       | /IFD/{UShort = 33432}                     | ascii       |
|       | Avis/IFD/IPTC/Copyright              |             |
|       | /IFD/XMP/ &lt; xmpalt &gt; DC : droits        | unicode     |
|       | /IFD/XMP/DC : droits                      | unicode     |
|       | Avis/IFD/IPTC/Copyright              |             |
|       | Avis/IFD/IRB/8bimiptc/IPTC/Copyright |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                                    | Format de disque |
|-------|-----------------------------------------|-------------|
|       | /IFD/XMP/DC : droits                      | unicode     |
|       | /IFD/XMP/ &lt; xmpalt &gt; DC : droits        | unicode     |
|       | Avis/IFD/IPTC/Copyright              |             |
|       | Avis/IFD/IRB/8bimiptc/IPTC/Copyright |             |
|       | /IFD/{UShort = 33432}                     | ascii       |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                                    |
|-------|-----------------------------------------|
|       | /IFD/XMP/DC : droits                      |
|       | Avis/IFD/IPTC/Copyright              |
|       | Avis/IFD/IRB/8bimiptc/IPTC/Copyright |
|       | /IFD/{UShort = 33432}                     |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. Copyright](../properties/props-system-copyright.md)
</dt> </dl>

 

 
