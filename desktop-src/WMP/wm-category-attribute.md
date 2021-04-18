---
title: Attribut WM/Category
description: L’attribut WM/Category est la catégorie du contenu.
ms.assetid: ca7d9d77-7b17-4617-82ec-70aa04e95022
keywords:
- Attribut WM/Category lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/Category
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57fbf8d08a5a1b6af003f4127441f15b7b9ca505
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526047"
---
# <a name="wmcategory-attribute"></a>Attribut WM/Category

L’attribut **WM/Category** est la catégorie du contenu.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Attributs de fichiers Windows Media couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Autres éléments](other-item-attributes.md)
-   [Éléments de photo](photo-item-attributes.md)
-   [Sélections](playlist-attributes-ref.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMCategory.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure (l’élément photo est pris en charge uniquement dans le lecteur Windows Media 10 ou version ultérieure)<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





