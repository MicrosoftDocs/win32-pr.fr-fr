---
title: Attribut auteur
description: L’attribut Author est le nom d’un artiste multimédia ou d’un acteur associé au contenu.
ms.assetid: 6621a955-dd6b-4725-9690-0cc96e73d94f
keywords:
- Lecteur Windows Media de l’attribut Author
topic_type:
- apiref
api_name:
- Author
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94ef73679aa3869a9a3d87b926b7f38464b1001
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856090"
---
# <a name="author-attribute"></a>Attribut auteur

L’attribut **Author** est le nom d’un artiste multimédia ou d’un acteur associé au contenu.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Sélections de CD](cd-playlist-attributes.md)
-   [Pistes de CD](cd-track-attributes.md)
-   [fichiers multimédias Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [DVD](dvd-attributes.md)
-   [Media. getItemInfoByType](media-getiteminfobytype.md)
-   [Éléments de photo](photo-item-attributes.md)
-   [Sélections](playlist-attributes-ref.md)
-   [Éléments radio](radio-item-attributes.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké à la fois dans la bibliothèque (ou le cache) et dans le fichier multimédia.

Cet attribut peut avoir plusieurs valeurs. Pour récupérer toutes les valeurs d’un attribut à valeurs multiples, vous devez utiliser le *média*. méthode **getItemInfoByType** , pas le *média*. méthode **getItemInfo** .

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMAuthor.

L' **acteur** et l' **artiste** sont des alias de cet attribut.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





