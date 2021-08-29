---
description: L’élément transition définit un objet de transition. Une transition est une transformation à deux entrées qui produit une transition d’un flux (par exemple, composite ou Track) à une autre.
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: Élément transition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e725c5c6282a35f027cad87fd0b8693dbf4885ce7d4c1d5948abc2caa9014301
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951478"
---
# <a name="transition-element"></a>Élément transition

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

L' `transition` élément définit un objet de transition. Une transition est une transformation à deux entrées qui produit une transition d’un flux (par exemple, composite ou Track) à une autre.

## <a name="attributes"></a>Attributs

[**CLSID**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**Lock**](lock-attribute.md), [**muet**](mute-attribute.md), [**Start**](start-attribute.md), [**Stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informations parent/enfant



| Étiquette | Valeur |
|----------|------------------------------------------------------------------------|
| Parent   | [**composite**](composite-element.md), [ **Track**](track-element.md) |
| Children | [**param**](param-element.md)                                         |



 

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

 

 



