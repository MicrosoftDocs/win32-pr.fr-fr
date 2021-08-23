---
title: Objet MetadataPicture
description: L’objet MetadataPicture fournit un moyen de récupérer les valeurs de l’attribut de métadonnées WM/Picture. Cet attribut correspond à une pochette d’album contenue dans un fichier multimédia numérique, et non à une pochette d’album téléchargée sur Internet.
ms.assetid: c0d6f43d-1a88-4ac2-a7b3-c502f4d57afb
keywords:
- objet MetadataPicture Lecteur Windows Media
topic_type:
- apiref
api_name:
- MetadataPicture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 261ed17a156e1b5563b52744490e2ed014803eb9f1e75c182f44d5bd228b11c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996209"
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
| [**Média**](media-object.md) | [**getItemInfoByType**](media-getiteminfobytype.md) |



 

À des fins d’illustration, `player.currentMedia.getItemInfoByType(name, language, index)` est utilisé dans les sections de syntaxe de référence.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 