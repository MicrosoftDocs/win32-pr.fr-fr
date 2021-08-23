---
title: Attribut DisplayArtist
description: L’attribut DisplayArtist est le nom de l’artiste affiché pour un élément.
ms.assetid: 8cf5a4e6-ce96-4fd4-b01a-6cd4264a5c09
keywords:
- Lecteur Windows Media de l’attribut DisplayArtist
topic_type:
- apiref
api_name:
- DisplayArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6c20e3d693aa7d5be5be0236d9eefebe7efcb70bc236db3f84389e5a3ceeccf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997319"
---
# <a name="displayartist-attribute"></a>Attribut DisplayArtist

L’attribut **DisplayArtist** est le nom de l’artiste affiché pour un élément.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)

## <a name="remarks"></a>Remarques

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

 

 





