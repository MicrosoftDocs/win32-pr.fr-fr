---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. TranscodedForSync.
ms.assetid: 1869d845-6264-425a-ab3e-e0a9f942961a
title: Stratégie de métadonnées de photo System. photo. TranscodedForSync
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e78086284e1ca13b01c5e7cd188b761afe7eeba8acb5f2bca103234f80955b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964758"
---
# <a name="systemphototranscodedforsync-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. TranscodedForSync

Stratégie de métadonnées de la photo pour la propriété [System. photo. TranscodedForSync](../properties/props-system-photo-transcodedforsync.md) .

### <a name="pkey"></a>A-la

\_Photo \_ TranscodedForSync

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ bool

### <a name="input-type"></a>Type d’entrée

Propriété booléenne.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                                  | Format de disque  |
|-------|---------------------------------------|--------------|
| 1     | /App1/IFD/{UShort = 18248}              | bool \_ UShort |
| 2     | /xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                                  | Format de disque  |
|-------|---------------------------------------|--------------|
| 1     | /App1/IFD/{UShort = 18248}              | bool \_ UShort |
| 2     | /xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                                  |
|-------|---------------------------------------|
| 1     | /App1/IFD/{UShort = 18248}              |
| 2     | /xmp/microsoftphoto:transcodedforsync |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                                      | Format de disque  |
|-------|-------------------------------------------|--------------|
| 1     | /IFD/{UShort = 18248}                       | bool \_ UShort |
| 2     | /ifd/xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                                      | Format de disque  |
|-------|-------------------------------------------|--------------|
| 1     | /IFD/{UShort = 18248}                       | bool \_ UShort |
| 2     | /ifd/xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                                      |
|-------|-------------------------------------------|
| 1     | /IFD/{UShort = 18248}                       |
| 2     | /ifd/xmp/microsoftphoto:transcodedforsync |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. TranscodedForSync](../properties/props-system-photo-transcodedforsync.md)
</dt> </dl>

 

 
