---
title: Message RB_ENDDRAG (commctrl. h)
description: Termine l’opération de glisser-déplacer du contrôle rebar. Ce message n’entraîne pas l’envoi d’une \_ notification ENDDRAG RBN.
ms.assetid: 4991dda6-32ea-4d3e-9d39-17c2b6995f09
keywords:
- RB_ENDDRAG les contrôles de Windows de message
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
ms.openlocfilehash: bacf910ff61cb0504883854313379a07096a9d5f1cd5e9cc2ac772ee6f6d7a43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085109"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_BEGINDRAG RB**](rb-begindrag.md)
</dt> <dt>

[**\_DRAGMOVE RB**](rb-dragmove.md)
</dt> </dl>

 

 





