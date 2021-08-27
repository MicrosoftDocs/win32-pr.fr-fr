---
title: Message SB_SIMPLE (commctrl. h)
description: Spécifie si une fenêtre d’état affiche du texte simple ou affiche toutes les parties de fenêtre définies par un \_ message SB SETPARTS précédent.
ms.assetid: 457209cb-67d4-4a9f-8d18-75aa5eb9ca1d
keywords:
- SB_SIMPLE les contrôles de Windows de message
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
ms.openlocfilehash: 229f0a896c9adcab6886151753761c62aefb8f4dc6ee21b7e85bb7507bda11f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132209"
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

## <a name="remarks"></a>Remarques

Si la fenêtre d’état passe de non simple à simple, ou vice versa, la fenêtre est immédiatement redessinée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





