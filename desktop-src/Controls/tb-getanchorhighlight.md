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
ms.openlocfilehash: 7bfff5ef1853bbf5657604c673dcc6a9be43af83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116817"
---
# <a name="tb_getanchorhighlight-message"></a>TO \_ GETANCHORHIGHLIGHT message

Récupère le paramètre de surbrillance d’ancrage d’une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur booléenne qui indique si la mise en surbrillance de l’ancre est définie. Si cette valeur est différente de zéro, la mise en surbrillance de l’ancre est activée. Si cette valeur est égale à zéro, elle est désactivée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TO \_ SETANCHORHIGHLIGHT**](tb-setanchorhighlight.md)
</dt> </dl>

 

 





