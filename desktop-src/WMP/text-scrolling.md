---
title: TEXTE. défilement
description: L’attribut de défilement spécifie ou récupère une valeur indiquant si le texte défile.
ms.assetid: 1cd5cb4e-673f-4273-91ff-50165c2b08fa
keywords:
- texte. défilement Lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.scrolling
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fdbb80b2033d542da4894172d58451ed5da224f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519393"
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

## <a name="requirements"></a>Spécifications



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

 

 





