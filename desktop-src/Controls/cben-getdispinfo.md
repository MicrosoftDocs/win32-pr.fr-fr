---
title: CBEN_GETDISPINFO le code de notification (commctrl. h)
description: Envoyé pour récupérer des informations d’affichage sur un élément de rappel. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: a181be28-0001-4953-8e59-77aff2dc40be
keywords:
- CBEN_GETDISPINFO les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- CBEN_GETDISPINFO
- CBEN_GETDISPINFOA
- CBEN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3121d15b1482bdedf19a814a42e3309265909f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123854"
---
# <a name="cben_getdispinfo-notification-code"></a>\_Code de notification CBEN GETDISPINFO

Envoyé pour récupérer des informations d’affichage sur un élément de rappel. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
CBEN_GETDISPINFO

    pDispInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) qui contient des informations sur le code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

L’application traitant ce code de notification doit retourner zéro.

## <a name="remarks"></a>Notes

La structure [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) contient une structure [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) . Le membre de **masque** spécifie les informations demandées par le contrôle.

Remplissez les membres appropriés de la structure pour retourner les informations demandées au contrôle. Si votre gestionnaire de messages définit le membre **Mask** de la structure [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) sur CBEIF \_ di \_ SETITEM, le contrôle stocke les informations et ne les redemande pas.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **CBEN \_ GETDISPINFOW** (Unicode) et **CBEN \_ GETDISPINFOA** (ANSI)<br/>         |



 

 





