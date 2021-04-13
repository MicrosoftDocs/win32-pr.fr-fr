---
title: DTN_FORMAT le code de notification (commctrl. h)
description: Envoyé par un contrôle de sélecteur de date et heure (PAO) pour demander du texte à afficher dans un champ de rappel. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ce0ee230-638e-425f-9f34-c379342cea93
keywords:
- Contrôles Windows de code de notification DTN_FORMAT
topic_type:
- apiref
api_name:
- DTN_FORMAT
- DTN_FORMATA
- DTN_FORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fadd11b090777d2226eeed85f32d2062e8340e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465919"
---
# <a name="dtn_format-notification-code"></a>\_Code de notification au format DTN

Envoyé par un contrôle de sélecteur de date et heure (PAO) pour demander du texte à afficher dans un champ de rappel. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
DTN_FORMAT

    lpNMFormat = (LPNMDATETIMEFORMAT) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata) contenant des informations relatives à cette instance du code de notification. La structure contient la sous-chaîne qui définit le champ de rappel et reçoit la chaîne mise en forme qui sera affichée par le contrôle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Le propriétaire du contrôle doit retourner zéro.

## <a name="remarks"></a>Notes

La gestion de ce code de notification permet au propriétaire du contrôle de fournir une chaîne personnalisée que le contrôle affichera. (Pour plus d’informations sur les champs de rappel, consultez [champs de rappel](date-and-time-picker-controls.md).)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **DTN \_ FORMATW** (Unicode) et **DTN \_ Formata** (ANSI)<br/>                     |



 

 





