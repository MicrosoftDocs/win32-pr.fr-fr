---
title: BUTTON. rémanent
description: L’attribut rémanent spécifie ou récupère une valeur indiquant si le bouton est un bouton bascule, c’est-à-dire s’il s’agit d’un bouton à deux États ou un seul État.
ms.assetid: aa0b48b4-29ce-440c-aeb9-dce31ab3cb63
keywords:
- BUTTON. rémanent Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTON.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8de9b4e1a8e4bab04e5729cb45662164e2dfa2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855736"
---
# <a name="buttonsticky"></a>BUTTON. rémanent

L’attribut **rémanent** spécifie ou récupère une valeur indiquant si le **bouton** est un bouton bascule, c’est-à-dire s’il s’agit d’un **bouton** à deux États ou un seul État.

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                        |
|-------|------------------------------------|
| true  | Le **bouton** est rémanent.              |
| false | Par défaut. Le **bouton** n’est pas rémanent. |



 

## <a name="remarks"></a>Notes

Si le **pense-bête** est défini sur true, le **bouton** passe à l’état inactif lorsque vous cliquez dessus et reste dans cet État jusqu’à ce que l’utilisateur clique à nouveau dessus. Quand le **bouton** est à l’état inactif, l’attribut **enfoncé** a la valeur true et le **downImage** est affiché.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BUTTON, élément**](button-element.md)
</dt> <dt>

[**BUTTON. suiv.**](button-down.md)
</dt> <dt>

[**BUTTON. downImage**](button-downimage.md)
</dt> </dl>

 

 





