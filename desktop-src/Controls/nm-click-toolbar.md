---
title: Code de notification NM_CLICK (barre d’outils) (commctrl. h)
description: Envoyé par un contrôle de barre d’outils lorsque l’utilisateur clique sur un élément avec le bouton gauche de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: fa43c9bc-db2a-4460-b193-2b4694d06d83
keywords:
- Contrôles Windows de code de notification NM_CLICK (barre d’outils)
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca31e3553327c94d371617d016a85395519c211d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844462"
---
# <a name="nm_click-toolbar-notification-code"></a>\_Code de notification de clic (barre d’outils) sur nm

Envoyé par un contrôle de barre d’outils lorsque l’utilisateur clique sur un élément avec le bouton gauche de la souris. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_CLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) qui contient des informations supplémentaires sur cette notification. Le membre **dwItemSpec** contient l’index de la section sur laquelle l’utilisateur a cliqué.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** pour indiquer que le clic de souris a été géré et supprimer le traitement par défaut par le système. Retourne **false** pour autoriser le traitement par défaut du clic.

## <a name="remarks"></a>Notes

Si vous cliquez sur un élément avec le bouton gauche de la souris, la barre d’outils envoie un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) avec le code de notification sur lequel l' [ \_ utilisateur a cliqué](bn-clicked.md) dans la fenêtre parente. La \_ notification de clic sur nm est envoyée après le message de **\_ commande WM** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

