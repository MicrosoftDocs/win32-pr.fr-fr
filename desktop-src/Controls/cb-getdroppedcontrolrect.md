---
title: Message CB_GETDROPPEDCONTROLRECT (winuser. h)
description: Une application envoie un \_ message CB GETDROPPEDCONTROLRECT pour récupérer les coordonnées d’écran d’une zone de liste déroulante dans son état abandonné.
ms.assetid: fd8d78c0-e1a8-49c8-9e35-a105d00b863c
keywords:
- CB_GETDROPPEDCONTROLRECT les contrôles de message Windows
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
ms.openlocfilehash: adff5ad10ff91557b2579006dae6e1258650d74e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465719"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RECTANGULAIRE**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

