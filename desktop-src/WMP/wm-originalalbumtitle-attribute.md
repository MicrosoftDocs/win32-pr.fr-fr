---
title: Attribut WM/OriginalAlbumTitle
description: L’attribut WM/OriginalAlbumTitle est le nom de l’album sur lequel la piste est apparue pour la première fois.
ms.assetid: e670c793-bae3-4dc5-92a1-4407cb2a094b
keywords:
- Attribut WM/OriginalAlbumTitle lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/OriginalAlbumTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0dc2344c95bf3d0b09448277f1522baa879c80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528691"
---
# <a name="wmoriginalalbumtitle-attribute"></a>Attribut WM/OriginalAlbumTitle

L’attribut **WM/OriginalAlbumTitle** est le nom de l’album sur lequel la piste est apparue pour la première fois.

## <a name="applies-to"></a>S'applique à

-   [Fichiers musicaux](music-file-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké uniquement dans un fichier musical qui ne se trouve pas dans la bibliothèque.

La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMOriginalAlbumTitle.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





