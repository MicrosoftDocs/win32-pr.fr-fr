---
title: Attribut WM/MediaClassSecondaryID
description: L’attribut WM/MediaClassSecondaryID est un GUID spécifiant la classe de support secondaire, qui est une sous-classe de la classe de support primaire.
ms.assetid: 8112513a-b73a-497a-9c24-24ccef31cffc
keywords:
- Lecteur Windows Media de l’attribut WM/MediaClassSecondaryID
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb88ea03e565df649088366e13b20332256b374d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404380"
---
# <a name="wmmediaclasssecondaryid-attribute"></a>Attribut WM/MediaClassSecondaryID

L’attribut **WM/MediaClassSecondaryID** est un GUID spécifiant la classe de support secondaire, qui est une sous-classe de la classe de support primaire.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [attributs de fichier multimédia Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Autres éléments](other-item-attributes.md)
-   [Éléments de photo](photo-item-attributes.md)
-   [Sélections](playlist-attributes-ref.md)
-   [Éléments radio](radio-item-attributes.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

Le tableau suivant répertorie les GUID pris en charge et leurs descriptions.



| GUID                                 | Description                                    |
|--------------------------------------|------------------------------------------------|
| D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC | L’objet Media représente une sélection statique. |
| EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D | L’objet Media représente une sélection automatique.  |



 

**MediaClassSecondaryID** est un alias pour cet attribut.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMMediaClassSecondaryID.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | l’élément photo est pris en charge uniquement dans Lecteur Windows Media 10 ou ultérieur l’élément radio est pris en charge uniquement dans la série Lecteur Windows Media 9. tous les autres éléments sont pris en charge dans Lecteur Windows Media série 9 et versions ultérieures<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





