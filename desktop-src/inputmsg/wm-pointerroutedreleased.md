---
title: Message WM_POINTERROUTEDRELEASED
description: Envoyé à tous les processus (configurés pour le chaînage inter-processus via AddContentWithCrossProcessChaining et ne gérant pas actuellement l’entrée de pointeur) jamais associés à un ID de pointeur spécifique, lors de la réception d’un message de WM_POINTERUP sur le processus actuel.
ms.assetid: B031ED80-6F1B-42A7-B4E2-55934E2C456C
keywords:
- WM_POINTERROUTEDRELEASED les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDRELEASED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 8e24a0df1a2bbdf2b0a9df97057686aa6045eff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384684"
---
# <a name="wm_pointerroutedreleased-message"></a>Message WM_POINTERROUTEDRELEASED

Envoyé à tous les processus (configurés pour le chaînage inter-processus via [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) et ne gérant pas actuellement l’entrée de pointeur) jamais associés à un ID de pointeur spécifique, lors de la réception d’un message de [**WM_POINTERUP**](wm-pointerup.md) sur le processus actuel.


```C++
#define WM_POINTERROUTEDRELEASED       0x0253
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Messages](messages.md)
</dt> </dl>

 

