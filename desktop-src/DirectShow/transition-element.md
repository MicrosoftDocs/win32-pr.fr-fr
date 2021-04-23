---
description: L’élément transition définit un objet de transition. Une transition est une transformation à deux entrées qui produit une transition d’un flux (par exemple, composite ou Track) à une autre.
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: Élément transition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60bf6b915a393ab153f0e94862cb5ed72dd3424c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910037"
---
# <a name="transition-element"></a>Élément transition

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `transition` élément définit un objet de transition. Une transition est une transformation à deux entrées qui produit une transition d’un flux (par exemple, composite ou Track) à une autre.

## <a name="attributes"></a>Attributs

[**CLSID**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**Lock**](lock-attribute.md), [**muet**](mute-attribute.md), [**Start**](start-attribute.md), [**Stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informations parent/enfant



| Étiquette | Valeur |
|----------|------------------------------------------------------------------------|
| Parent   | [**composite**](composite-element.md), [ **Track**](track-element.md) |
| Children | [**envoyés**](param-element.md)                                         |



 

## <a name="remarks"></a>Remarques

L’attribut **CLSID** spécifie le sous-objet qui crée la transition.

## <a name="examples"></a>Exemples


```XML
<transition
    clsid="{2a54c913-07aa-11d2-8d6d-00c04f8ef8e0}"
    start="7"
    stop="10"
/>
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments XTL](xtl-elements.md)
</dt> </dl>

 

 



