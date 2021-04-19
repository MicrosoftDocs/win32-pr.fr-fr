---
title: BUTTONGROUP. radio
description: L’attribut radio spécifie ou récupère une valeur indiquant si le BUTTONGROUP est composé de cases d’option.
ms.assetid: f84479f8-af4f-4ca8-991e-1c2ab39d7110
keywords:
- BUTTONGROUP. radio Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.radio
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1765a7756aedcebc2b7b030634d8598a5cd89e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539964"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BUTTONELEMENT. collant**](buttonelement-sticky.md)
</dt> <dt>

[**Élément BUTTONGROUP**](buttongroup-element.md)
</dt> </dl>

 

 





