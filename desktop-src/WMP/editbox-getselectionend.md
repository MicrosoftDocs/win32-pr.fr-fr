---
title: EDITBOX. getSelectionEnd
description: La méthode getSelectionEnd récupère la position de fin du texte sélectionné dans le contrôle EditBox.
ms.assetid: 82a445da-3c50-41b7-8ac8-da6c860056ba
keywords:
- EDITBOX. getSelectionEnd Lecteur Windows Media
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionEnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f27c2974360e7e77becfa67a27b4e96b529ad1e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126852622"
---
# <a name="editboxgetselectionend"></a>EDITBOX. getSelectionEnd

La méthode **getSelectionEnd** récupère la position de fin du texte sélectionné dans le contrôle EditBox.

``` syntax
        elementID.getSelectionEnd()
```

## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne un **nombre** (**long**).

## <a name="remarks"></a>Notes

Si aucun texte n’est sélectionné, cette méthode retourne la position du point d’insertion.

Si le contrôle est multiligne, cette méthode retourne l’index de caractère dans le contrôle, et non l’index de ligne.

Cette méthode ne peut être appelée qu’une fois que le contrôle est visible.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX. getSelectionStart**](editbox-getselectionstart.md)
</dt> <dt>

[**EDITBOX. replaceSelection**](editbox-replaceselection.md)
</dt> <dt>

[**EDITBOX. setSelection**](editbox-setselection.md)
</dt> </dl>

 

 





