---
description: L’élément Effect définit un objet d’effet audio ou vidéo. Un effet est appliqué à un seul flux (par exemple, une composition, une piste ou une source).
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: Effect, élément (Gdipluseffects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd31e85407b99c3dffd4417a051be168f7c6d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537851"
---
# <a name="effect-element"></a>Effect, élément

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `effect` élément définit un objet d’effet audio ou vidéo. Un effet est appliqué à un seul flux (par exemple, une composition, une piste ou une source).

## <a name="attributes"></a>Attributs

[**CLSID**](clsid-attribute.md), [**Lock**](lock-attribute.md), [**muet**](mute-attribute.md), [**Start**](start-attribute.md), [**Stop**](stop-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informations parent/enfant



|          |                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| Parent   | [**composite**](composite-element.md), [**Group**](group-element.md), [**clip**](clip-element.md), [**Track**](track-element.md) |
| Children | [**envoyés**](param-element.md)                                                                                                       |



 

## <a name="remarks"></a>Notes

L’attribut **CLSID** spécifie le sous-objet qui crée l’effet.

## <a name="examples"></a>Exemples


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Gdipluseffects. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments XTL](xtl-elements.md)
</dt> </dl>

 

 




