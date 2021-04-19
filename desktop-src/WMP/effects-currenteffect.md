---
title: EFFECTs. currentEffect
description: L’attribut currentEffect spécifie ou récupère la visualisation actuelle.
ms.assetid: d6b0e77d-2872-420a-b5f5-36fd23243648
keywords:
- EFFECTs. currentEffect Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19398946906fb6c6ea43234c110383b27b16ede
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520836"
---
# <a name="effectscurrenteffect"></a>EFFECTs. currentEffect

L’attribut **currentEffect** spécifie ou récupère la visualisation actuelle.

``` syntax
        elementID.currentEffect
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **objet** en lecture/écriture. La valeur par défaut est la première visualisation dans l’ordre de création. Si aucune visualisation n’a été créée dans l’apparence, la valeur par défaut est la première visualisation dans le registre.

## <a name="remarks"></a>Notes

Vous pouvez utiliser cet objet pour accéder aux visualisations personnalisées que vous avez créées. Par exemple, vous pouvez exposer une propriété par le biais de l’interface **IDispatch** dans votre visualisation. Vous pouvez ensuite modifier la valeur de la propriété à partir de votre apparence en faisant de votre visualisation l’effet actuel, puis en utilisant l’objet **currentEffect** pour définir une nouvelle valeur pour la propriété. Par exemple, si votre visualisation expose une propriété nommée backgroundColor, le code JScript suivant spécifie une nouvelle valeur :


```JScript
// The EFFECTS element ID is MyEffects.
MyEffects.currentEffect.backgroundColor = "blue";
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EFFECTs**](effects-element.md)
</dt> <dt>

[**EFFECTs. currentEffectTitle**](effects-currenteffecttitle.md)
</dt> <dt>

[**EFFECTs. currentEffectType**](effects-currenteffecttype.md)
</dt> </dl>

 

 





