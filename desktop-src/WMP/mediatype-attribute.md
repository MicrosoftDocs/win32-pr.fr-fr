---
title: MediaType (attribut)
description: L’attribut MediaType est le type de contenu de l’élément.
ms.assetid: 0d8a6937-32d8-4a4a-87e5-0002f077fefe
keywords:
- Lecteur Windows Media d’attribut MediaType
topic_type:
- apiref
api_name:
- MediaType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f75871e2b258b229483114be8f7673cccb7ca005e0b3618f4cfd803d47fe3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996229"
---
# <a name="mediatype-attribute"></a>MediaType (attribut)

L’attribut **MediaType** est le type de contenu de l’élément.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Autres éléments](other-item-attributes.md)
-   [Éléments de photo](photo-item-attributes.md)
-   [Sélections](playlist-attributes-ref.md)
-   [Éléments radio](radio-item-attributes.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Remarques

Cet attribut est stocké uniquement dans la bibliothèque.

Cet attribut a l’une des valeurs suivantes : « audio », « other », « photo », « playlist », « radio » ou « Video ». Utilisez cet attribut avec *MediaCollection*. méthode **getByAttribute** pour récupérer une sélection contenant tous les éléments d’un type particulier.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> <dt>

[**MediaCollection.getByAttribute**](mediacollection-getbyattribute.md)
</dt> </dl>

 

 





