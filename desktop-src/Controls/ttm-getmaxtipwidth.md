---
title: Message TTM_GETMAXTIPWIDTH (commctrl. h)
description: Récupère la largeur maximale d’une fenêtre d’info-bulle.
ms.assetid: 0f0a5403-fe2e-4e5a-96c2-a435827a5fd7
keywords:
- TTM_GETMAXTIPWIDTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_GETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f89c56692db9d451eb18db61af262cc0f3a715f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942147"
---
# <a name="ttm_getmaxtipwidth-message"></a>\_Message atténuation GETMAXTIPWIDTH

Récupère la largeur maximale d’une fenêtre d’info-bulle.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **int** qui représente la largeur d’info-bulle maximale, en pixels. Si aucune largeur maximale n’a été définie précédemment, le message retourne-1.

## <a name="remarks"></a>Notes

La valeur de largeur d’info-bulle maximale n’indique pas la largeur réelle d’une fenêtre d’info-bulle. Au lieu de cela, si une chaîne d’info-bulle dépasse la largeur maximale, le contrôle divise le texte en plusieurs lignes, à l’aide d’espaces pour déterminer les sauts de ligne. Si le texte ne peut pas être segmenté en plusieurs lignes, il est affiché sur une seule ligne. La longueur de cette ligne peut dépasser la largeur d’info-bulle maximale.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ATTÉNUATION \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md)
</dt> </dl>

 

 





