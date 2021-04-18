---
title: Attribut WM/OriginalArtist
description: L’attribut WM/OriginalArtist est le nom de l’artiste qui a initialement produit le contenu.
ms.assetid: b00e8a1f-0f6a-4ef4-b1bc-01a4d0a28c19
keywords:
- Attribut WM/OriginalArtist lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/OriginalArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e7b78bb8b36db22dca1a616c1bdeffc3186b1f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540679"
---
# <a name="wmoriginalartist-attribute"></a>Attribut WM/OriginalArtist

L’attribut **WM/OriginalArtist** est le nom de l’artiste qui a initialement produit le contenu.

## <a name="applies-to"></a>S'applique à

-   [Fichiers musicaux](music-file-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké uniquement dans un fichier musical qui ne se trouve pas dans la bibliothèque.

La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMOriginalArtist.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





