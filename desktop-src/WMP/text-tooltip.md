---
title: TEXT. toolTip
description: L’attribut toolTip spécifie ou récupère le texte d’info-bulle pour le contrôle Text.
ms.assetid: 3e275607-e7ff-4424-8310-c628ede22629
keywords:
- TEXT. toolTip lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.toolTip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b064f2abefd07ec65a82069196b1012561699b62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545456"
---
# <a name="texttooltip"></a>TEXT. toolTip

L’attribut **ToolTip** spécifie ou récupère le texte d’info-bulle pour le contrôle Text.

``` syntax
        elementID.toolTip
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture d’une longueur maximale de 1024 caractères. Il n'a aucune valeur par défaut.

## <a name="remarks"></a>Notes

Si cet attribut n’est pas spécifié et que le texte de l’attribut de **valeur** est tronqué dans le contrôle de texte, ou si **wordWrap** a la valeur true, l’info-bulle affiche le texte complet de l’attribut **value** .

Lorsque cet attribut a la valeur "" (chaîne vide), aucune info-bulle n’est affichée.

Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément de texte**](text-element.md)
</dt> <dt>

[**TEXT. Value**](text-value.md)
</dt> <dt>

[**TEXT. wordWrap**](text-wordwrap.md)
</dt> </dl>

 

 





