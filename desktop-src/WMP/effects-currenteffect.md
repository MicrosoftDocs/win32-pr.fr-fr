---
title: EFFECTs. currentEffect
description: L’attribut currentEffect spécifie ou récupère la visualisation actuelle.
ms.assetid: d6b0e77d-2872-420a-b5f5-36fd23243648
keywords:
- effects. currentEffect Lecteur Windows Media
topic_type:
- apiref
api_name:
- EFFECTS.currentEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d9ac47ef88d1a0bce4982f71ce2e20e33f48933c9916bbb1e62085b5a1e5178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996869"
---
# <a name="effectscurrenteffect"></a>EFFECTs. currentEffect

L’attribut **currentEffect** spécifie ou récupère la visualisation actuelle.

``` syntax
        elementID.currentEffect
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **objet** en lecture/écriture. La valeur par défaut est la première visualisation dans l’ordre de création. Si aucune visualisation n’a été créée dans l’apparence, la valeur par défaut est la première visualisation dans le registre.

## <a name="remarks"></a>Remarques

Vous pouvez utiliser cet objet pour accéder aux visualisations personnalisées que vous avez créées. Par exemple, vous pouvez exposer une propriété par le biais de l’interface **IDispatch** dans votre visualisation. Vous pouvez ensuite modifier la valeur de la propriété à partir de votre apparence en faisant de votre visualisation l’effet actuel, puis en utilisant l’objet **currentEffect** pour définir une nouvelle valeur pour la propriété. par exemple, si votre visualisation expose une propriété nommée backgroundColor, le code JScript suivant spécifie une nouvelle valeur :


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

 

 





