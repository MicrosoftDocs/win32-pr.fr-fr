---
title: Message TB_SETANCHORHIGHLIGHT (commctrl. h)
description: Définit le paramètre de surbrillance d’ancrage pour une barre d’outils.
ms.assetid: d31652d5-e9cf-4bf3-8f90-818eb078fa87
keywords:
- TB_SETANCHORHIGHLIGHT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 809f71e446f7768d637258152db1dd2d56346dfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518057"
---
# <a name="tb_setanchorhighlight-message"></a>TO \_ SETANCHORHIGHLIGHT message

Définit le paramètre de surbrillance d’ancrage pour une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur **booléenne** qui spécifie si la mise en surbrillance de l’ancre est activée ou désactivée. Si cette valeur est différente de zéro, la mise en surbrillance de l’ancre est activée. Si cette valeur est égale à zéro, la mise en surbrillance de l’ancre est désactivée.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le paramètre de surbrillance d’ancrage précédent. Si cette valeur est différente de zéro, la mise en surbrillance de l’ancre a été activée. Si cette valeur est égale à zéro, la mise en surbrillance de l’ancre était désactivée.

## <a name="remarks"></a>Notes

La mise en surbrillance d’ancre dans une barre d’outils signifie que le dernier élément mis en surbrillance reste en surbrillance jusqu’à ce qu’un autre élément Cela se produit même si le curseur quitte le contrôle ToolBar.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





