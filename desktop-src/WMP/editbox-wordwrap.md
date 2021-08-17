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
ms.openlocfilehash: 2f9e02ff9665eac98717e1d316899a78f9b3b5908e5e41b3928b5cda541b96c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749251"
---
# <a name="editboxwordwrap"></a>EDITBOX. wordWrap

L’attribut **wordWrap** spécifie ou récupère une valeur indiquant si le retour automatique à la ligne est activé.

``` syntax
        elementID.wordWrap
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une valeur **booléenne** en lecture/écriture dont la valeur par défaut est true.

## <a name="remarks"></a>Remarques

Cet attribut est utile uniquement lorsque **editStyle** a la valeur « Multiline ».

Si le retour automatique à la ligne est désactivé et que le texte ne tient pas dans le contrôle, le texte est tronqué.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX. editStyle**](editbox-editstyle.md)
</dt> </dl>

 

 





