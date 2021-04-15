---
title: Objet MetadataPicture
description: L’objet MetadataPicture fournit un moyen de récupérer les valeurs de l’attribut de métadonnées WM/Picture. Cet attribut correspond à une pochette d’album contenue dans un fichier multimédia numérique, et non à une pochette d’album téléchargée sur Internet.
ms.assetid: c0d6f43d-1a88-4ac2-a7b3-c502f4d57afb
keywords:
- Objet MetadataPicture lecteur Windows Media
topic_type:
- apiref
api_name:
- MetadataPicture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 892b162ba05ab43740565c849b00bc4e3c52aad6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463554"
---
# <a name="metadatapicture-object"></a>Objet MetadataPicture

L’objet **MetadataPicture** fournit un moyen de récupérer les valeurs de l’attribut de métadonnées [**WM/Picture**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) . Cet attribut correspond à une pochette d’album contenue dans un fichier multimédia numérique, et non à une pochette d’album téléchargée sur Internet.

L’objet **MetadataPicture** prend en charge les propriétés suivantes.



| Propriété                                           | Description                                       |
|----------------------------------------------------|---------------------------------------------------|
| [**descriptive**](metadatapicture-description.md) | Récupère une description de l’image de métadonnées.    |
| [**mimeType**](metadatapicture-mimetype.md)       | Récupère le type MIME de l’image de métadonnées.    |
| [**Picture**](metadatapicture-picturetype.md) | Récupère le type d’image de l’image de métadonnées. |
| [**URL**](metadatapicture-url.md)                 | À usage interne uniquement                                |



 

L’objet **MetadataPicture** est accessible par le biais de la méthode suivante.



| Object                        | Méthode                                               |
|-------------------------------|------------------------------------------------------|
| [**Multimédia**](media-object.md) | [**getItemInfoByType**](media-getiteminfobytype.md) |



 

À des fins d’illustration, `player.currentMedia.getItemInfoByType(name, language, index)` est utilisé dans les sections de syntaxe de référence.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 