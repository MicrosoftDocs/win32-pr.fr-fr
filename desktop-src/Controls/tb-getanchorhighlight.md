---
title: Message TB_GETANCHORHIGHLIGHT (commctrl. h)
description: Récupère le paramètre de surbrillance d’ancrage d’une barre d’outils.
ms.assetid: 167d481c-8684-40eb-9323-cfa238be3643
keywords:
- TB_GETANCHORHIGHLIGHT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eadee4fd029cfe8ffb43960070538cf6574ca3bb178829f65af1ddc0753b9ef2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919079"
---
# <a name="tb_getanchorhighlight-message"></a>TO \_ GETANCHORHIGHLIGHT message

Récupère le paramètre de surbrillance d’ancrage d’une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur booléenne qui indique si la mise en surbrillance de l’ancre est définie. Si cette valeur est différente de zéro, la mise en surbrillance de l’ancre est activée. Si cette valeur est égale à zéro, elle est désactivée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TO \_ SETANCHORHIGHLIGHT**](tb-setanchorhighlight.md)
</dt> </dl>

 

 





