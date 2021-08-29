---
title: Message HDM_GETITEMDROPDOWNRECT (commctrl. h)
description: Obtient le rectangle englobant du bouton partagé pour un élément d’en-tête avec style HDF \_ SPLITBUTTON. Envoyez ce message de manière explicite ou à l’aide de la macro GetItemDropDownRect d’en-tête \_ .
ms.assetid: d7188dfb-4ffa-4641-b210-2c2ec480ca13
keywords:
- HDM_GETITEMDROPDOWNRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- HDM_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f02fa02dd04720a130bf6303927fed64aadc53f4f90acc70a60e2c0cf7afd7ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047169"
---
# <a name="hdm_getitemdropdownrect-message"></a>\_Message HDM GETITEMDROPDOWNRECT

Obtient le rectangle englobant du bouton partagé pour un élément d’en-tête avec style **HDF \_ SPLITBUTTON**. Envoyez ce message de manière explicite ou à l’aide de la macro [**\_ GetItemDropDownRect d’en-tête**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Index de base zéro de l’élément de contrôle d’en-tête pour lequel récupérer le rectangle englobant.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [**Rect**](/windows/win32/api/windef/ns-windef-rect) qui reçoit les informations de rectangle englobant. L’expéditeur du message est chargé d’allouer cette structure. Les coordonnées retournées dans la structure RECT sont exprimées par rapport au parent du contrôle header.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

L’élément d’en-tête doit être de style **HDF \_ SPLITBUTTON**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[À propos des contrôles Header](header-controls.md)
</dt> </dl>

 

 





