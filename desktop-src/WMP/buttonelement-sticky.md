---
title: BUTTONELEMENT. collant
description: L’attribut rémanent spécifie ou récupère une valeur indiquant si le BUTTONELEMENT est un bouton bascule, c’est-à-dire s’il s’agit d’un bouton à deux États ou un seul État.
ms.assetid: a7e74f70-9fa6-45a1-ab65-2db107e13551
keywords:
- BUTTONELEMENT. collant le lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTONELEMENT.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713b26fdee3062fbe803d05e034bc9896cdd5563
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541343"
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



 

## <a name="remarks"></a>Notes

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

 

 





