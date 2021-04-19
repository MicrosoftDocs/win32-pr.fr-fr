---
title: Attribut DisplayArtist
description: L’attribut DisplayArtist est le nom de l’artiste affiché pour un élément.
ms.assetid: 8cf5a4e6-ce96-4fd4-b01a-6cd4264a5c09
keywords:
- Attribut DisplayArtist lecteur Windows Media
topic_type:
- apiref
api_name:
- DisplayArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44d479add519d8b7df346869e783c36560fc46dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523597"
---
# <a name="displayartist-attribute"></a>Attribut DisplayArtist

L’attribut **DisplayArtist** est le nom de l’artiste affiché pour un élément.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)

## <a name="remarks"></a>Notes

En règle générale, **DisplayArtist** aura la même valeur que l’attribut **WM/AlbumArtist** lorsque cet attribut est défini. Dans le cas contraire, la valeur sera le nom de l’artiste associé à la première piste de l’album.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------|
| Version<br/> | Lecteur Windows Media 11<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> <dt>

[**Attribut WM/AlbumArtist**](wm-albumartist-attribute.md)
</dt> </dl>

 

 





