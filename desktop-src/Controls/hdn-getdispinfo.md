---
title: HDN_GETDISPINFO le code de notification (commctrl. h)
description: Envoyé au propriétaire d’un contrôle header lorsque le contrôle a besoin d’informations sur un élément d’en-tête de rappel. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 51522df0-83ae-4d9a-a8fc-31083e24242a
keywords:
- Contrôles Windows de code de notification HDN_GETDISPINFO
topic_type:
- apiref
api_name:
- HDN_GETDISPINFO
- HDN_GETDISPINFOA
- HDN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45fe753b610fae69956b89caadade394566d0dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032433"
---
# <a name="hdn_getdispinfo-notification-code"></a>\_Code de notification HDN GETDISPINFO

Envoyé au propriétaire d’un contrôle header lorsque le contrôle a besoin d’informations sur un élément d’en-tête de rappel. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_GETDISPINFO

   pNMHDDispInfo = (LPNMHDDISPINFO) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) . En entrée, les champs de la structure spécifient les informations requises et l’élément concerné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un LRESULT.

## <a name="remarks"></a>Notes

Remplissez les membres appropriés de la structure pour retourner les informations demandées au contrôle header. Si votre gestionnaire de messages définit le membre **Mask** de la structure [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) sur HDI \_ di \_ SETITEM, le contrôle header stocke les informations et ne les redemande pas.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **HDN \_ GETDISPINFOW** (Unicode) et **HDN \_ GETDISPINFOA** (ANSI)<br/>           |



 

 





