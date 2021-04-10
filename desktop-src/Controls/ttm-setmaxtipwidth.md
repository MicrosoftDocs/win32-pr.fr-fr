---
title: Message TTM_SETMAXTIPWIDTH (commctrl. h)
description: Définit la largeur maximale d’une fenêtre d’info-bulle.
ms.assetid: 3cfb6011-d0c3-4a57-aead-d4ec09a057cc
keywords:
- TTM_SETMAXTIPWIDTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_SETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ce930b289205b5fb0d2768068b8cb28cd11aec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200553"
---
# <a name="ttm_setmaxtipwidth-message"></a>\_Message atténuation SETMAXTIPWIDTH

Définit la largeur maximale d’une fenêtre d’info-bulle.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Largeur maximale de la fenêtre d’info-bulle, ou-1 pour autoriser toute largeur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la largeur d’info-bulle maximale précédente.

## <a name="remarks"></a>Notes

La valeur de largeur maximale n’indique pas la largeur réelle d’une fenêtre d’info-bulle. Au lieu de cela, si une chaîne d’info-bulle dépasse la largeur maximale, le contrôle divise le texte en plusieurs lignes, à l’aide d’espaces pour déterminer les sauts de ligne. Si le texte ne peut pas être segmenté en plusieurs lignes, il est affiché sur une seule ligne, qui peut dépasser la largeur d’info-bulle maximale.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ATTÉNUATION \_ GETMAXTIPWIDTH**](ttm-getmaxtipwidth.md)
</dt> </dl>

 

 





