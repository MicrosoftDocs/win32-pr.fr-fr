---
title: Message RB_ENDDRAG (commctrl. h)
description: Termine l’opération de glisser-déplacer du contrôle rebar. Ce message n’entraîne pas l’envoi d’une \_ notification ENDDRAG RBN.
ms.assetid: 4991dda6-32ea-4d3e-9d39-17c2b6995f09
keywords:
- RB_ENDDRAG les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b6f201471b6f260555aacb9d89c1363492ed6bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942461"
---
# <a name="rb_enddrag-message"></a>\_Message ENDDRAG RB

Termine l’opération de glisser-déplacer du contrôle rebar. Ce message n’entraîne pas l’envoi d’une notification [ \_ ENDDRAG RBN](rbn-enddrag.md) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de ce message n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_BEGINDRAG RB**](rb-begindrag.md)
</dt> <dt>

[**\_DRAGMOVE RB**](rb-dragmove.md)
</dt> </dl>

 

 





