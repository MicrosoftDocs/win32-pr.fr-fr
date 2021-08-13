---
title: TEXT. foregroundColor
description: L’attribut foregroundColor spécifie ou récupère la couleur de texte du contrôle de texte.
ms.assetid: 1ddbad93-fbff-4be6-9797-6594b5f09a1e
keywords:
- TEXT. foregroundColor Lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b134058fdc39b653982f752f2623c6cd69b192e24e417ac012a02813a38334a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467069"
---
# <a name="textforegroundcolor"></a>TEXT. foregroundColor

L’attribut **foregroundColor** spécifie ou récupère la couleur de texte du contrôle de texte.

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant toute valeur de couleur Microsoft Internet Explorer. La valeur par défaut est « Black ».

Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .

Quand vous utilisez **alphaBlend** ou **alphaBlendTo** avec un élément de **texte** pour lequel le **backgroundColor** n’est pas spécifié, une couleur d’arrière-plan noire est utilisée. Si la couleur de premier plan est également noire (valeur par défaut pour l’attribut **foregroundColor** ), votre texte peut devenir illisible. Pour éviter cela, spécifiez toujours l’attribut **backgroundColor** ou définissez **foregroundColor** sur une couleur autre que Black.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AmbientAttributes. alphaBlend**](ambientattributes-alphablend.md)
</dt> <dt>

[**AmbientAttributes.alphaBlendTo**](ambientattributes-alphablendto.md)
</dt> <dt>

[**Référence de couleur**](color-reference.md)
</dt> <dt>

[**Élément de texte**](text-element.md)
</dt> <dt>

[**TEXT. backgroundColor**](text-backgroundcolor.md)
</dt> </dl>

 

 





