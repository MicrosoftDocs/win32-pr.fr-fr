---
title: Attribut AlbumIDAlbumArtist
description: L’attribut AlbumIDAlbumArtist est un identificateur unique pour l’album.
ms.assetid: beaa8d01-1722-4545-8705-6b3d130113b1
keywords:
- Lecteur Windows Media de l’attribut AlbumIDAlbumArtist
topic_type:
- apiref
api_name:
- AlbumIDAlbumArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4905f0448c7e08abe308a57b1ad08020d47563847db1aa32744c0de3279cdcdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055387"
---
# <a name="albumidalbumartist-attribute"></a>Attribut AlbumIDAlbumArtist

L’attribut **AlbumIDAlbumArtist** est un identificateur unique pour l’album.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)

## <a name="remarks"></a>Remarques

Cet attribut est stocké uniquement dans la bibliothèque.

L’identificateur unique est une combinaison du titre de l’album et du nom de l’artiste de l’album. Dans cet attribut, le nom de l’artiste de l’album est le premier. Lorsque vous utilisez la méthode [MediaCollection. getAttributeStringCollection](mediacollection-getattributestringcollection.md) pour obtenir un objet **StringCollection** à l’aide de cet attribut, les valeurs sont triées par nom de l’artiste de l’album.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attribut AlbumID**](albumid-attribute.md)
</dt> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





