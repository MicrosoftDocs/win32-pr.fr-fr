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
ms.openlocfilehash: 8902d36ebe9e8227d22f55273e8351d7ed09c592953b44a31e45c06b838f9871
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122649"
---
# <a name="wmlanguage-attribute"></a>Attribut WM/Language

L’attribut **WM/Language** est le langage de l’élément.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [attributs de fichier multimédia Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Éléments radio](radio-item-attributes.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Remarques

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

Cet attribut peut avoir plusieurs valeurs. Pour récupérer toutes les valeurs d’un attribut à valeurs multiples, vous devez utiliser la méthode **Media. getItemInfoByType** , et non la méthode **Media. getItemInfo** .

**Language** est un alias de cet attribut.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMLanguage.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure (l’élément radio est pris en charge uniquement dans Lecteur Windows Media série 9)<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





