---
title: Message CB_GETDROPPEDCONTROLRECT (winuser. h)
description: Une application envoie un \_ message CB GETDROPPEDCONTROLRECT pour récupérer les coordonnées d’écran d’une zone de liste déroulante dans son état abandonné.
ms.assetid: fd8d78c0-e1a8-49c8-9e35-a105d00b863c
keywords:
- CB_GETDROPPEDCONTROLRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_GETDROPPEDCONTROLRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c140abb139cc47020f333ccf66f71cf36d890449be91d66f51b646db22091c39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089279"
---
# <a name="cb_getdroppedcontrolrect-message"></a>\_Message GETDROPPEDCONTROLRECT CB

Une application envoie un message **CB \_ GETDROPPEDCONTROLRECT** pour récupérer les coordonnées d’écran d’une zone de liste déroulante dans son état abandonné.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui reçoit les coordonnées de la zone de liste déroulante dans son état abandonné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le message est correctement exécuté, la valeur de retour est différente de zéro.

Si le message échoue, la valeur de retour est zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RECTANGULAIRE**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

