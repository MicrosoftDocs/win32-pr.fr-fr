---
title: EDITBOX. getLineIndex
description: La méthode getLineIndex récupère l’index de caractère du premier caractère sur la ligne avec l’index de ligne spécifié.
ms.assetid: 1298227a-d839-44fc-bacb-44c3c968bd94
keywords:
- EDITBOX. getLineIndex Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f55027bb7d577b7080ad2f006a5a006e718c2d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541783"
---
# <a name="editboxgetlineindex"></a>EDITBOX. getLineIndex

La méthode **getLineIndex** récupère l’index de caractère du premier caractère sur la ligne avec l’index de ligne spécifié.

``` syntax
        elementID.getLineIndex(index)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*évaluer*
</dt> <dd>

**Nombre** (**long**) contenant l’index de la ligne dont l’index de caractère doit être récupéré.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne un **nombre** (**long**).

## <a name="remarks"></a>Notes

Si l’index de ligne spécifié est 1, la ligne contenant le point d’insertion est utilisée.

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

[**EDITBOX. getLineFromChar**](editbox-getlinefromchar.md)
</dt> </dl>

 

 





