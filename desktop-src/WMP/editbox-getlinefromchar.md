---
title: EDITBOX. getLineFromChar
description: La méthode getLineFromChar récupère l’index de ligne pour l’index de caractère spécifié.
ms.assetid: c3a29bdf-ff63-4b6d-90e8-d414dde87f85
keywords:
- EDITBOX. getLineFromChar Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineFromChar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3462ce628da72ca1e55df79e408fc79e0ec8b63a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526496"
---
# <a name="editboxgetlinefromchar"></a>EDITBOX. getLineFromChar

La méthode **getLineFromChar** récupère l’index de ligne pour l’index de caractère spécifié.

``` syntax
        elementID.getLineFromChar(index)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*évaluer*
</dt> <dd>

**Nombre** (**long**) contenant l’index du caractère dont l’index de ligne doit être récupéré.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne un **nombre** (**long**).

## <a name="remarks"></a>Notes

Si la position de caractère spécifiée est 1, cette méthode récupère l’index de ligne de la ligne active.

Cette méthode ne peut être appelée qu’une fois que le contrôle est visible.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX. getLine**](editbox-getline.md)
</dt> <dt>

[**EDITBOX. getLineIndex**](editbox-getlineindex.md)
</dt> </dl>

 

 





