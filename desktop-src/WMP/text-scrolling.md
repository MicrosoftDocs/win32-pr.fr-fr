---
title: TEXTE. défilement
description: L’attribut de défilement spécifie ou récupère une valeur indiquant si le texte défile.
ms.assetid: 1cd5cb4e-673f-4273-91ff-50165c2b08fa
keywords:
- TEXT. défilement du lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.scrolling
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fdbb80b2033d542da4894172d58451ed5da224f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545492"
---
# <a name="textscrolling"></a>TEXTE. défilement

L’attribut de **défilement** spécifie ou récupère une valeur indiquant si le texte défile.

``` syntax
        elementID.scrolling
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                     |
|-------|---------------------------------|
| true  | Le défilement est activé.           |
| false | Par défaut. Le défilement est désactivé. |



 

## <a name="remarks"></a>Notes

La fonctionnalité de défilement fournit une mémoire tampon à deux espaces entre la fin du texte et le début de la ligne répétée.

L’attribut **Justification** spécifie l’emplacement où le texte apparaît pour la première fois avant le début du défilement.

Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément de texte**](text-element.md)
</dt> <dt>

[**TEXT. Justification**](text-justification.md)
</dt> <dt>

[**TEXT. scrollingAmount**](text-scrollingamount.md)
</dt> <dt>

[**TEXT. scrollingDelay**](text-scrollingdelay.md)
</dt> <dt>

[**TEXT. scrollingDirection**](text-scrollingdirection.md)
</dt> </dl>

 

 





