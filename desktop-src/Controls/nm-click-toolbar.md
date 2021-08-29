---
title: Code de notification NM_CLICK (barre d’outils) (commctrl. h)
description: Envoyé par un contrôle de barre d’outils lorsque l’utilisateur clique sur un élément avec le bouton gauche de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: fa43c9bc-db2a-4460-b193-2b4694d06d83
keywords:
- NM_CLICK (barre d’outils) code de notification Windows les contrôles
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
ms.openlocfilehash: 1b116ee8a47252b01713637cd8af8bbd484bf0c6cc26a34e1be882f805f501b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834489"
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

## <a name="remarks"></a>Remarques

Si vous cliquez sur un élément avec le bouton gauche de la souris, la barre d’outils envoie un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) avec le code de notification sur lequel l' [ \_ utilisateur a cliqué](bn-clicked.md) dans la fenêtre parente. La \_ notification de clic sur nm est envoyée après le message de **\_ commande WM** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

