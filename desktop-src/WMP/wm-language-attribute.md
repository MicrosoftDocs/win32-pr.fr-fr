---
title: Attribut WM/Language
description: L’attribut WM/Language est le langage de l’élément.
ms.assetid: aebfb518-61ca-4b75-875a-ce2127a74b67
keywords:
- attribut WM/Language Lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/Language
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172cc8498bf5360e29822a484bcc2ddacd70b8b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404383"
---
# <a name="wmlanguage-attribute"></a>Attribut WM/Language

L’attribut **WM/Language** est le langage de l’élément.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [attributs de fichier multimédia Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Éléments radio](radio-item-attributes.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

Cet attribut peut avoir plusieurs valeurs. Pour récupérer toutes les valeurs d’un attribut à valeurs multiples, vous devez utiliser la méthode **Media. getItemInfoByType** , et non la méthode **Media. getItemInfo** .

**Language** est un alias de cet attribut.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMLanguage.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure (l’élément radio est pris en charge uniquement dans Lecteur Windows Media série 9)<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





