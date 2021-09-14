---
title: HDN_GETDISPINFO le code de notification (commctrl. h)
description: Envoyé au propriétaire d’un contrôle header lorsque le contrôle a besoin d’informations sur un élément d’en-tête de rappel. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 51522df0-83ae-4d9a-a8fc-31083e24242a
keywords:
- HDN_GETDISPINFO les contrôles de Windows de code de notification
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999923"
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

## <a name="return-value"></a>Valeur de retour

Retourne un LRESULT.

## <a name="remarks"></a>Notes

Remplissez les membres appropriés de la structure pour retourner les informations demandées au contrôle header. Si votre gestionnaire de messages définit le membre **Mask** de la structure [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) sur HDI \_ di \_ SETITEM, le contrôle header stocke les informations et ne les redemande pas.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **HDN \_ GETDISPINFOW** (Unicode) et **HDN \_ GETDISPINFOA** (ANSI)<br/>           |



 

 





