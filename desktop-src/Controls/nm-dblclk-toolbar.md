---
title: Code de notification NM_DBLCLK (barre d’outils) (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle ToolBar que l’utilisateur a double-cliqué sur le bouton gauche de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: c6198245-cfd4-4e1f-877d-94c1d47e09d2
keywords:
- NM_DBLCLK (barre d’outils) code de notification Windows les contrôles
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75abaf61938fbf377dbe8b6c5eaca99ff5ab027abe08c670de72a218dd51f1b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919659"
---
# <a name="nm_dblclk-toolbar-notification-code"></a>\_Code de notification DBLCLK nm (barre d’outils)

Avertit la fenêtre parente d’un contrôle ToolBar que l’utilisateur a double-cliqué sur le bouton gauche de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_DBLCLK

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



 

 





