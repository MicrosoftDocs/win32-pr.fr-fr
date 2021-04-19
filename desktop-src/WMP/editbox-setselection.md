---
title: EDITBOX. setSelection
description: La méthode setSelection sélectionne le texte dans le contrôle zone d’édition à partir de l’index de début spécifié jusqu’à l’index de fin spécifié.
ms.assetid: 97b20a17-4b9c-4144-b448-8d7611c0e994
keywords:
- Windows Media Player. setSelection. setSelection
topic_type:
- apiref
api_name:
- EDITBOX.setSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d7077de0ea59940c4afa551d22188d5583d0e4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532233"
---
# <a name="editboxsetselection"></a>EDITBOX. setSelection

La méthode **SetSelection** sélectionne le texte dans le contrôle zone d’édition à partir de l’index de début spécifié jusqu’à l’index de fin spécifié.

``` syntax
        elementID.setSelection(start, end)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="start"></span><span id="START"></span>*activer*
</dt> <dd>

**Nombre** (**long**) contenant l’index de caractère de la position de départ du texte sélectionné.

</dd> <dt>

<span id="end"></span><span id="END"></span>*effet*
</dt> <dd>

**Nombre** (**long**) contenant l’index de caractère de la position de fin du texte sélectionné.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si le début est égal à 0 et que la fin est égale à 1, tout le texte du contrôle de zone d’édition est sélectionné. Si le début est 1, toute sélection actuelle est désélectionnée.

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

[**EDITBOX. replaceSelection**](editbox-replaceselection.md)
</dt> </dl>

 

 





