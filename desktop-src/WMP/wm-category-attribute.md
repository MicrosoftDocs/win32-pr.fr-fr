---
title: Attribut WM/Category
description: L’attribut WM/Category est la catégorie du contenu.
ms.assetid: ca7d9d77-7b17-4617-82ec-70aa04e95022
keywords:
- attribut WM/Category Lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/Category
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5537d8ead3ec7d68a56fb5f67018c944ab2988fbbf7c751988c22f646e7cd28f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761409"
---
# <a name="wmcategory-attribute"></a>Attribut WM/Category

L’attribut **WM/Category** est la catégorie du contenu.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [attributs de fichier multimédia Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Autres éléments](other-item-attributes.md)
-   [Éléments de photo](photo-item-attributes.md)
-   [Sélections](playlist-attributes-ref.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Remarques

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMCategory.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure (l’élément photo est pris en charge uniquement dans Lecteur Windows Media 10 ou version ultérieure)<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





