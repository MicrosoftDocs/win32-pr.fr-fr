---
title: Attribut AlbumID
description: L’attribut AlbumID est un identificateur unique pour l’album.
ms.assetid: 0412d91a-11a7-434c-8717-a71d85655679
keywords:
- Lecteur Windows Media de l’attribut AlbumID
topic_type:
- apiref
api_name:
- AlbumID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2690e4b6dd6bf6c8d795c8a06aca9c65c3f2c17513cf9b8ab8d55419b00d517
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124069"
---
# <a name="albumid-attribute"></a>Attribut AlbumID

L’attribut **AlbumID** est un identificateur unique pour l’album.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)

## <a name="remarks"></a>Remarques

Cet attribut est stocké uniquement dans la bibliothèque.

L’identificateur unique est une combinaison du titre de l’album et du nom de l’artiste de l’album. Dans cet attribut, le titre de l’album est le premier. Lorsque vous utilisez la méthode [MediaCollection. getAttributeStringCollection](mediacollection-getattributestringcollection.md) pour obtenir un objet **StringCollection** à l’aide de cet attribut, les valeurs sont triées par titre d’album.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attribut AlbumIDAlbumArtist**](albumidalbumartist-attribute.md)
</dt> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





