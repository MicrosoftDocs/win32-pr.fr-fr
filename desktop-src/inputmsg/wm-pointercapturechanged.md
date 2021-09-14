---
title: Message WM_POINTERCAPTURECHANGED
description: Envoyé à une fenêtre qui perd la capture d’un pointeur d’entrée.
ms.assetid: 6eec37da-227c-4be1-bf0b-98704caa1322
keywords:
- WM_POINTERCAPTURECHANGED les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_POINTERCAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 768dc81be57bb61a23acab7ebea450dba577d60a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520372"
---
# <a name="wm_pointercapturechanged-message"></a>Message WM_POINTERCAPTURECHANGED

Envoyé à une fenêtre qui perd la capture d’un pointeur d’entrée.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_POINTERCAPTURECHANGED           0x024C
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Contient des informations sur le pointeur d’entrée qui est perdu. Utilisez [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) pour récupérer l’ID du pointeur.

</dd> <dt>

*lParam* 
</dt> <dd>

Contient un handle vers la fenêtre qui capture le pointeur d’entrée. Cette valeur peut être NULL si le pointeur n’est plus capturé par la fenêtre.

Si ce message est généré à partir du traitement interne, la valeur peut être le handle de la fenêtre qui reçoit le message.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si une application traite ce message, elle doit retourner la valeur zéro.

Si l’application ne traite pas ce message, elle doit appeler [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Notes

Une fenêtre doit utiliser cette notification pour arrêter le traitement des messages suivants et lancer tout nettoyage requis pour la perte du pointeur. Le traitement des mouvements associés au pointeur doit également être terminé (par exemple, en appelant [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)) et les contacts restants sont à nouveau associés à la fenêtre.

En règle générale, si une fenêtre reçoit la notification **WM_POINTERCAPTURECHANGED** , aucune notification ultérieure relative au pointeur d’entrée n’est reçue. Pour cette raison, ne dépendez pas de notifications jumelées telles que [**WM_POINTERENTER**](wm-pointerenter.md) et [**WM_POINTERLEAVE**](wm-pointerleave.md).

**WM_POINTERCAPTURECHANGED** n’inclut pas les données [**POINTER_INFO**](/previous-versions/windows/desktop/api) . À part l’indicateur [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) défini, les données retournées par [**GetPointerInfo**](/previous-versions/windows/desktop/api) (ou toute variante) sont identiques à celles retournées avant la notification.

Si l’application ne traite pas cette notification, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) peut générer un ou plusieurs messages [**WM_GESTURE**](../wintouch/wm-gesture.md) ou, si un mouvement n’est pas reconnu, **DefWindowProc** peut générer une entrée de souris.

Si une application consomme de manière sélective une entrée de pointeur et passe le reste à [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), le comportement résultant n’est pas défini.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Messages](messages.md)
</dt> </dl>

 

