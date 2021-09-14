---
title: Message HDM_SETFOCUSEDITEM (commctrl. h)
description: Définit le focus sur un élément spécifié dans un contrôle header. Envoyez ce message de manière explicite ou à l’aide de la macro SetFocusedItem d’en-tête \_ .
ms.assetid: 20a321ce-4420-4239-b34d-9e7f24a89fc3
keywords:
- HDM_SETFOCUSEDITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- HDM_SETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd416744478248760f4e2c9f94a362db5a8d327
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006265"
---
# <a name="hdm_setfocuseditem-message"></a>\_Message HDM SETFOCUSEDITEM

Définit le focus sur un élément spécifié dans un contrôle header. Envoyez ce message de manière explicite ou à l’aide de la macro [**\_ SetFocusedItem d’en-tête**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Non utilisé. Doit être zéro.</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Index de l’élément.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[À propos des contrôles Header](header-controls.md)
</dt> </dl>

 

 





