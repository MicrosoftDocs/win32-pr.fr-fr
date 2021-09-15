---
title: TEXT. fontSmoothing
description: L’attribut fontSmoothing spécifie ou récupère une valeur indiquant si le lissage des polices est activé.
ms.assetid: bd6f0468-285e-44b3-a5e8-361744c5ce4a
keywords:
- TEXT. fontSmoothing Lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.fontSmoothing
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcdf285572b4edda0f514cb3519b6953f9e94677
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294343"
---
# <a name="textfontsmoothing"></a>TEXT. fontSmoothing

L’attribut **fontSmoothing** spécifie ou récupère une valeur indiquant si le lissage des polices est activé.

``` syntax
        elementID.fontSmoothing
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                          |
|-------|--------------------------------------|
| true  | Le lissage des polices est activé.           |
| false | Par défaut. Le lissage des polices est désactivé. |



 

## <a name="remarks"></a>Notes

Le lissage des polices utilise la fonctionnalité d’anticrénelage du système d’exploitation. si le lissage des polices est activé et que le système d’exploitation prend en charge l’anticrénelage, Lecteur Windows Media tente de lisser le texte. Toutes les polices ne prennent pas en charge l’anticrénelage. Lecteur Windows Media 10 utilise la méthode d’anticrénelage ClearType Windows XP.

-   **Avertissement** Le lissage des polices sur une couleur transparente peut entraîner la fusion de la couleur transparente dans les caractères. Il n’est pas recommandé d’utiliser **fontSmoothing** si le texte s’affiche sur une transparence.

Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément de texte**](text-element.md)
</dt> </dl>

 

 





