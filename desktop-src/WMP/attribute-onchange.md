---
title: attribute_onchange
description: Lorsqu’un attribut d’apparence change de valeur, un événement qui peut être géré par un gestionnaire d’événements se produit. Le nom du gestionnaire d’événements est le nom de l’attribut suivi d’un trait de soulignement et de \ 0034 ; OnChange \ 0034 ;, par exemple, \ 0034 ; valeur \_ OnChange \ 0034 ;.
ms.assetid: 783b686c-d56c-4036-9af4-97b9b246ef7e
keywords:
- attribute_onchange Lecteur Windows Media
topic_type:
- apiref
api_name:
- attribute_onchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c707b04587b6e975f81c8a0d0918b14c8e193d303f82c61b5220796bb6975b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573759"
---
# <a name="attribute_onchange"></a>OnChange d’attribut \_

Lorsqu’un attribut d’apparence change de valeur, un événement qui peut être géré par un gestionnaire d’événements se produit. Le nom du gestionnaire d’événements est le nom de l’attribut suivi d’un trait de soulignement et de « OnChange », tels que « valeur \_ OnChange ».

``` syntax
        attribute_onchange
```

## <a name="examples"></a>Exemples


```JScript
<SLIDER 
  thumbImage = "thumb.gif"
  value_onchange = "JScript: if (value == 100) backgroundColor = 'green';"
/>

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 70 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Gestionnaires d’événements ambiants**](ambient-event-handlers.md)
</dt> </dl>

 

 





