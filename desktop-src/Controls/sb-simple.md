---
title: Message SB_SIMPLE (commctrl. h)
description: Spécifie si une fenêtre d’état affiche du texte simple ou affiche toutes les parties de fenêtre définies par un \_ message SB SETPARTS précédent.
ms.assetid: 457209cb-67d4-4a9f-8d18-75aa5eb9ca1d
keywords:
- SB_SIMPLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_SIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f7a462a917c86531cd70f5f5c8ea60bf448ff6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105064"
---
# <a name="sb_simple-message"></a>\_Message simple SB

Spécifie si une fenêtre d’état affiche du texte simple ou affiche toutes les parties de fenêtre définies par un message [**SB \_ SETPARTS**](sb-setparts.md) précédent.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indicateur de type d’affichage. Si ce paramètre a la **valeur true**, la fenêtre affiche un texte simple. Si la **valeur est false**, elle affiche plusieurs parties.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour n’est pas utilisée.

## <a name="remarks"></a>Notes

Si la fenêtre d’état passe de non simple à simple, ou vice versa, la fenêtre est immédiatement redessinée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





