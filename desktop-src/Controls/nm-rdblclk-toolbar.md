---
title: Code de notification NM_RDBLCLK (barre d’outils) (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle que l’utilisateur a double-cliqué sur le bouton droit de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0281a687-3f1c-4fc1-bf1d-19c7ac920cd3
keywords:
- NM_RDBLCLK (barre d’outils) code de notification Windows les contrôles
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d81fadafa6faa0a4375d9aa34e98bb22a0099f9d0cdabcdbe1a385317e5df1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119391529"
---
# <a name="nm_rdblclk-toolbar-notification-code"></a>\_Code de notification RDBLCLK nm (barre d’outils)

Avertit la fenêtre parente d’un contrôle que l’utilisateur a double-cliqué sur le bouton droit de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_RDBLCLK

    lpnmmouse = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) qui contient des informations sur ce code de notification. Si l’utilisateur a cliqué sur un élément de la barre d’outils, le membre **dwItemSpec** contient l’identificateur de l’élément et le membre **dwItemData** contient les données de l’élément. Si vous avez cliqué sur un séparateur ou un espace blanc dans la barre d’outils, le membre **dwItemSpec** contient-1.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **false** pour permettre au contrôle de barre d’outils d’effectuer le traitement par défaut de l’événement, ou **true** pour empêcher le contrôle de traiter l’événement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





