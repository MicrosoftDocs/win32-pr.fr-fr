---
title: TEXT. textWidth
description: L’attribut textWidth récupère la largeur en pixels du texte contenu dans l’attribut value.
ms.assetid: 46c34659-f441-467c-8846-45785f7a2736
keywords:
- TEXT. textWidth Lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.textWidth
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17ce93517837aecf737336137df3cf5d8bf292dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412215"
---
# <a name="texttextwidth"></a>TEXT. textWidth

L’attribut **textWidth** récupère la largeur en pixels du texte contenu dans l’attribut **value** .

``` syntax
        elementID.textWidth
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture seule (**int**).

## <a name="remarks"></a>Notes

La valeur retournée est basée sur les attributs **fontFace**, **FontSize** et **FontStyle** , ainsi que sur les caractères réels dans la chaîne de l’attribut **value** .

Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément de texte**](text-element.md)
</dt> <dt>

[**TEXT. fontFace**](text-fontface.md)
</dt> <dt>

[**TEXT. FontSize**](text-fontsize.md)
</dt> <dt>

[**TEXT. fontStyle**](text-fontstyle.md)
</dt> <dt>

[**TEXT. Value**](text-value.md)
</dt> </dl>

 

 





