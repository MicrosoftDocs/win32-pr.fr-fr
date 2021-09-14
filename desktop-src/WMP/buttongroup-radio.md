---
title: BUTTONGROUP. radio
description: L’attribut radio spécifie ou récupère une valeur indiquant si le BUTTONGROUP est composé de cases d’option.
ms.assetid: f84479f8-af4f-4ca8-991e-1c2ab39d7110
keywords:
- BUTTONGROUP. radio Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.radio
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1765a7756aedcebc2b7b030634d8598a5cd89e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126852682"
---
# <a name="buttongroupradio"></a>BUTTONGROUP. radio

L’attribut **radio** spécifie ou récupère une valeur indiquant si le **BUTTONGROUP** est composé de cases d’option.

``` syntax
        elementID.radio
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                                      |
|-------|--------------------------------------------------|
| true  | Le **BUTTONGROUP** est de type radio.              |
| false | Par défaut. **BUTTONGROUP** n’est pas de type radio. |



 

## <a name="remarks"></a>Notes

Si **radio** a la valeur true, tous les éléments **BUTTONELEMENT** dans le **BUTTONGROUP** seront rémanents, mais un seul bouton à la fois sera à l’état inactif.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BUTTONELEMENT. collant**](buttonelement-sticky.md)
</dt> <dt>

[**Élément BUTTONGROUP**](buttongroup-element.md)
</dt> </dl>

 

 





