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
ms.openlocfilehash: d6df21a5464aa44621c2eca760690806237f9e75a79c5f695d3df5b7604a6878
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964219"
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

## <a name="return-value"></a>Valeur retournée

NULL

## <a name="remarks"></a>Remarques

Ce message n’est pas envoyé avec un message [**WM_POINTERUP**](wm-pointerup.md) ou un message [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) .

## <a name="requirements"></a>Configuration requise



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

 

