---
title: BUTTONELEMENT. collant
description: L’attribut rémanent spécifie ou récupère une valeur indiquant si le BUTTONELEMENT est un bouton bascule, c’est-à-dire s’il s’agit d’un bouton à deux États ou un seul État.
ms.assetid: a7e74f70-9fa6-45a1-ab65-2db107e13551
keywords:
- BUTTONELEMENT. collant Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTONELEMENT.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc8a709fc28f0d1529c58725db5856931195a66cc370559dd9d14af61e869db6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120035"
---
# <a name="buttonelementsticky"></a>BUTTONELEMENT. collant

L’attribut **rémanent** spécifie ou récupère une valeur indiquant si le **BUTTONELEMENT** est un bouton bascule, c’est-à-dire s’il s’agit d’un bouton à deux États ou un seul État.

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                               |
|-------|-------------------------------------------|
| true  | **BUTTONELEMENT** est rémanente.              |
| false | Par défaut. **BUTTONELEMENT** n’est pas rémanent. |



 

## <a name="remarks"></a>Remarques

Si l’attribut **rémanent** a la valeur true, l’élément Button passe à l’état inactif lorsque vous cliquez dessus et reste dans cet État jusqu’à ce que l’utilisateur clique à nouveau dessus. Lorsque l’élément Button est dans l’état inactif, l’attribut **UpDown** a la valeur true et la partie appropriée du groupe de boutons **downImage** est affichée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément BUTTONELEMENT**](buttonelement-element.md)
</dt> <dt>

[**BUTTONELEMENT. suiv.**](buttonelement-down.md)
</dt> <dt>

[**BUTTONGROUP. downImage**](buttongroup-downimage.md)
</dt> </dl>

 

 





