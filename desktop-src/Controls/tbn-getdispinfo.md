---
title: TBN_GETDISPINFO le code de notification (commctrl. h)
description: Récupère les informations d’affichage d’un élément de barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ed6e4141-2bf8-4a92-8349-f3833c87fcf3
keywords:
- TBN_GETDISPINFO les contrôles de Windows de code de notification
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ffa2afafee64a82fb440d3d1e3031899ab94c0614d32449062ca29426aaa6a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876849"
---
# <a name="tbn_getdispinfo-notification-code"></a>\_Code de notification TBN GETDISPINFO

Récupère les informations d’affichage d’un élément de barre d’outils. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_GETDISPINFO 

    lptbdi = (LPNMTBDISPINFO) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTBDISPINFO**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa) . Le membre **idCommand** spécifie l’identificateur de commande de l’élément, le membre **lParam** contient les données définies par l’application de l’élément et le membre **dwMask** spécifie les informations demandées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée par le contrôle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TBN \_ GETDISPINFOW** (Unicode) et **TBN \_ GETDISPINFOA** (ANSI)<br/>           |



 

 





