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
ms.openlocfilehash: 56a8a9f85a3dce5ef070519f436c28ec157f7aa467a9115bcd8e2ccefa6444f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997769"
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



 

## <a name="remarks"></a>Remarques

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

 

 





