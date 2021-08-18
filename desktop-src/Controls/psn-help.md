---
title: PSN_HELP le code de notification (Prsht. h)
description: Notifie une page sur laquelle l’utilisateur a cliqué sur le bouton aide. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 4ad2c608-8caa-44c6-845d-4c0c1bd80763
keywords:
- PSN_HELP les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- PSN_HELP
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f03dc1e016780494c8c5ca35e62baf2570af04ee77daf21f404d7371e9df168
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588199"
---
# <a name="psn_help-notification-code"></a>\_Code de notification d’aide PSN

Notifie une page sur laquelle l’utilisateur a cliqué sur le bouton aide. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
PSN_HELP 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) qui contient des informations sur le code de notification. Cette structure contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) en tant que premier membre, **HDR**. Le membre **hwndFrom** de cette structure **NMHDR** contient le handle de la feuille de propriétés. Le membre **lParam** de la structure **PSHNOTIFY** ne contient aucune information.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Une application doit afficher des informations d’aide pour la page.

> [!Note]  
> Ce code de notification n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





