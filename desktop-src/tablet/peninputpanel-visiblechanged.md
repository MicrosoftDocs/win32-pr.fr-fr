---
description: Obsolète. Le PenInputPanel a été remplacé par le panneau de saisie de texte (TIP). Se produit lorsque l’objet PenInputPanel est affiché ou masqué.
ms.assetid: bf4651f4-2cf4-4952-a93e-3c6ba4846722
title: Événement PenInputPanel. VisibleChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c739f3517ad9739f1d1ba95af9e5001dfbe659a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538377"
---
# <a name="peninputpanelvisiblechanged-event"></a>Événement PenInputPanel. VisibleChanged

Action déconseillée. Le [**PenInputPanel**](peninputpanel-class.md) a été remplacé par le [panneau de saisie de texte (TIP)](text-input-panel-reference.md).

Se produit lorsque l’objet [**PenInputPanel**](peninputpanel-class.md) est affiché ou masqué.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT VisibleChanged(
  [in] VARIANT_BOOL NewVisibility
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NewVisibility* \[ dans\]
</dt> <dd>

**Variante \_ TRUE** pour faire en sorte que l’objet [**PenInputPanel**](peninputpanel-class.md) devienne visible ; Sinon, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cet événement a la valeur, il retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

L’événement **VisibleChanged** s’applique à la cible de pointage du panneau de saisie Tablet PC. Toutefois, il n’est pas déclenché lorsque la cible de survol se développe pour afficher le panneau de saisie complet du Tablet PC.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 




