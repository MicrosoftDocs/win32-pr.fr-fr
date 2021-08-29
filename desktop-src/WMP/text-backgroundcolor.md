---
title: TEXT. backgroundColor
description: L’attribut backgroundColor spécifie ou récupère la couleur d’arrière-plan du contrôle de texte.
ms.assetid: 0c16318f-bf57-4c5f-85c1-46641124d431
keywords:
- TEXT. backgroundColor Lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65361f581a265b2fa65c8f64e3a05f165691d2c03276bd3412ecd86588f8ff73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901049"
---
# <a name="textbackgroundcolor"></a>TEXT. backgroundColor

L’attribut **backgroundColor** spécifie ou récupère la couleur d’arrière-plan du contrôle de texte.

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant toute valeur de couleur Microsoft Internet Explorer ou la valeur « None ». Sa valeur par défaut est « None », ce qui signifie que l’arrière-plan est transparent.

## <a name="remarks"></a>Remarques

La couleur d’arrière-plan est définie pour la hauteur et la largeur du contrôle. Si la hauteur et la largeur ne sont pas définies, la couleur d’arrière-plan est définie sur la hauteur et la largeur du texte.

Quand vous utilisez **alphaBlend** ou **alphaBlendTo** avec un élément de **texte** pour lequel le **backgroundColor** n’est pas spécifié, une couleur d’arrière-plan noire est utilisée. Si la couleur de premier plan est également noire (valeur par défaut pour l’attribut **foregroundColor** ), votre texte peut devenir illisible. Pour éviter cela, spécifiez toujours l’attribut **backgroundColor** ou définissez **foregroundColor** sur une couleur autre que Black.

Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .

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

[**TEXT. foregroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





