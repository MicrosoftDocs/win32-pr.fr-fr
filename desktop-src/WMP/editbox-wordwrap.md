---
title: EDITBOX. wordWrap
description: L’attribut wordWrap spécifie ou récupère une valeur indiquant si le retour automatique à la ligne est activé.
ms.assetid: 027817f0-e077-4db5-8216-f9a9f41fd210
keywords:
- EDITBOX. wordWrap Lecteur Windows Media
topic_type:
- apiref
api_name:
- EDITBOX.wordWrap
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fefe92691a150571ce16b0c80d187540d58f5f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192791"
---
# <a name="editboxwordwrap"></a>EDITBOX. wordWrap

L’attribut **wordWrap** spécifie ou récupère une valeur indiquant si le retour automatique à la ligne est activé.

``` syntax
        elementID.wordWrap
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une valeur **booléenne** en lecture/écriture dont la valeur par défaut est true.

## <a name="remarks"></a>Notes

Cet attribut est utile uniquement lorsque **editStyle** a la valeur « Multiline ».

Si le retour automatique à la ligne est désactivé et que le texte ne tient pas dans le contrôle, le texte est tronqué.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX. editStyle**](editbox-editstyle.md)
</dt> </dl>

 

 





