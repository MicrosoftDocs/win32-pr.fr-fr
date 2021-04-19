---
title: EDITBOX. getSelectionStart
description: La méthode getSelectionStart récupère la position de départ du texte sélectionné dans le contrôle EditBox.
ms.assetid: 2d7efe14-549c-4f73-96a7-b8ce88b881ad
keywords:
- EDITBOX. getSelectionStart Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionStart
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2508119e5b1d46d09b3531582e86caad7e7facbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534928"
---
# <a name="editboxgetselectionstart"></a>EDITBOX. getSelectionStart

La méthode **getSelectionStart** récupère la position de départ du texte sélectionné dans le contrôle EditBox.

``` syntax
        elementID.getSelectionStart()
```

## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne un **nombre** (**long**).

## <a name="remarks"></a>Notes

Si aucun texte n’est sélectionné, cette méthode retourne la position du point d’insertion.

Si le contrôle est multiligne, cette méthode retourne l’index de caractère dans le contrôle, et non l’index de ligne.

Cette méthode ne peut être appelée qu’une fois que le contrôle est visible.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX. getSelectionEnd**](editbox-getselectionend.md)
</dt> <dt>

[**EDITBOX. replaceSelection**](editbox-replaceselection.md)
</dt> <dt>

[**EDITBOX. setSelection**](editbox-setselection.md)
</dt> </dl>

 

 





