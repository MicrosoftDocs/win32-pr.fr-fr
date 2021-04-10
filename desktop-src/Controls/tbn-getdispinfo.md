---
title: TBN_GETDISPINFO le code de notification (commctrl. h)
description: Récupère les informations d’affichage d’un élément de barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ed6e4141-2bf8-4a92-8349-f3833c87fcf3
keywords:
- Contrôles Windows de code de notification TBN_GETDISPINFO
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f3a0a47adfe7f172f7a4d0e4c9139b67aef01d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105028"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TBN \_ GETDISPINFOW** (Unicode) et **TBN \_ GETDISPINFOA** (ANSI)<br/>           |



 

 





