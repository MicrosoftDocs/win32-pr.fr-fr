---
title: Message WM_POINTERROUTEDAWAY
description: Se produit sur le processus qui reçoit l’entrée lorsque l’entrée du pointeur est routée vers un autre processus. AddContentWithCrossProcessChaining).
ms.assetid: 06F8152C-0DA0-4820-835E-07AD35B24310
keywords:
- WM_POINTERROUTEDAWAY les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDAWAY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3c099c02338aa70817d75717064e0b99ac13c96b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520341"
---
# <a name="wm_pointerroutedaway-message"></a>Message WM_POINTERROUTEDAWAY

Se produit sur le processus qui reçoit l’entrée lorsque l’entrée du pointeur est routée vers un autre processus.

Envoyé lorsque l’entrée de pointeur passe d’un processus à un autre dans le contenu configuré pour le chaînage inter-processus ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).

Ce message est envoyé au processus qui reçoit actuellement l’entrée de pointeur.


```C++
#define WM_POINTERROUTEDAWAY       0x0252
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Inutilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Inutilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

NULL

## <a name="remarks"></a>Notes

Ce message n’est pas envoyé avec un message [**WM_POINTERUP**](wm-pointerup.md) ou un message [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Messages](messages.md)
</dt> <dt>

[**WM_POINTERROUTEDTO**](wm-pointerroutedto.md)
</dt> </dl>

 

