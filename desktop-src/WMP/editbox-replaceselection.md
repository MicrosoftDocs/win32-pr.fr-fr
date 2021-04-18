---
title: EDITBOX. replaceSelection
description: La méthode replaceSelection remplace la sélection actuelle par le texte spécifié.
ms.assetid: 600650fb-f0c8-489a-9bf2-04f31705c6b0
keywords:
- EDITBOX. replaceSelection Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.replaceSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6546f24c864d0b466acd17d9a42616c3f8ab01b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540363"
---
# <a name="editboxreplaceselection"></a>EDITBOX. replaceSelection

La méthode **ReplaceSelection** remplace la sélection actuelle par le texte spécifié.

``` syntax
        elementID.replaceSelection(newValue)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*newValue*
</dt> <dd>

**Chaîne** contenant le texte pour remplacer le texte sélectionné.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si aucun texte n’est sélectionné, le texte de remplacement est inséré à l’emplacement actuel du point d’insertion.

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

[**EDITBOX. getSelectionStart**](editbox-getselectionstart.md)
</dt> <dt>

[**EDITBOX. setSelection**](editbox-setselection.md)
</dt> </dl>

 

 





