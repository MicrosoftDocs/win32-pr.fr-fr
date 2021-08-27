---
title: LISTBOX. popUp
description: L’attribut popUp spécifie une valeur indiquant si l’élément représente un contrôle Popup ou zone de liste.
ms.assetid: b0ade23a-6164-4dd4-b599-43ea1fcd44e4
keywords:
- LISTBOX. popUp Lecteur Windows Media
topic_type:
- apiref
api_name:
- LISTBOX.popUp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a755a4fc8f5e1451ee118f718a9b6618e75875789faef7318164f7f2add2069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996439"
---
# <a name="listboxpopup"></a>LISTBOX. popUp

L’attribut **popUp** spécifie une valeur indiquant si l’élément représente un contrôle Popup ou zone de liste.

``` syntax
<ELEMENT popUp="value">
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** spécifiée au moment de la conception uniquement.



| Valeur | Description                                |
|-------|--------------------------------------------|
| true  | L’élément représente un contrôle Popup.    |
| false | L’élément représente un contrôle de zone de liste. |



 

## <a name="remarks"></a>Remarques

L’élément **Popup** représente un contrôle de zone de liste qui s’affiche uniquement lorsque cela est nécessaire. Elle est identique à l’élément **ListBox** , à l’exception de la valeur par défaut de cet attribut, qui modifie le comportement d’affichage. Pour les éléments **ListBox** , la valeur par défaut est false. Pour les éléments **Popup** , la valeur par défaut est true. Au lieu de spécifier cet attribut, l’élément **ListBox** ou **Popup** doit être utilisé en fonction du comportement souhaité.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément LISTBOX**](listbox-element.md)
</dt> <dt>

[**POPUP (élément)**](popup-element.md)
</dt> </dl>

 

 





