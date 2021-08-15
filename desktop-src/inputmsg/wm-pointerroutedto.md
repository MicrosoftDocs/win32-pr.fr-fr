---
title: Message WM_POINTERROUTEDTO
description: Envoyé lors de l’entrée de pointeur en cours, pour un ID de pointeur existant, passe d’un processus à un autre dans le contenu configuré pour le chaînage inter-processus (AddContentWithCrossProcessChaining).
ms.assetid: 163E2C31-4E29-4CBA-B079-1963D4762D7B
keywords:
- WM_POINTERROUTEDTO les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDTO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9b7de7dd1affb9100a29613e3b4186d3d5bdaa32d853e683579fdcc62e7f981f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117695620"
---
# <a name="wm_pointerroutedto-message"></a>Message WM_POINTERROUTEDTO

Envoyé lors de l’entrée de pointeur en cours, pour un ID de pointeur existant, passe d’un processus à un autre dans le contenu configuré pour le chaînage inter-processus ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).

Ce message est envoyé au processus qui ne reçoit pas actuellement l’entrée de pointeur.


```C++
#define WM_POINTERROUTEDTO       0x0251
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

Ce message n’est pas envoyé lorsqu’un message de [**WM_POINTERDOWN**](wm-pointerdown.md) est publié pour un nouvel ID de pointeur sur un processus différent.

Un message de [**WM_POINTERDOWN**](wm-pointerdown.md) n’est pas envoyé si un message **WM_POINTERROUTEDTO** est publié en premier.

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

[**WM_POINTERROUTEDAWAY**](wm-pointerroutedaway.md)
</dt> </dl>

 

