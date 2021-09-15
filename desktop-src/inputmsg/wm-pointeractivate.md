---
title: Message WM_POINTERACTIVATE
description: Envoyé à une fenêtre inactive lorsqu’un pointeur principal génère un WM_POINTERDOWN sur la fenêtre.
ms.assetid: 4eec37da-227c-4be1-bf0b-99704caa1322
keywords:
- WM_POINTERACTIVATE les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_POINTERACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: b9bda11b5cb7a27f7744df6e20890a125a66bd88
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520373"
---
# <a name="wm_pointeractivate-message"></a>Message WM_POINTERACTIVATE

Envoyé à une fenêtre inactive lorsqu’un pointeur principal génère un [**WM_POINTERDOWN**](wm-pointerdown.md) sur la fenêtre. Tant que le message reste non géré, il se déplace vers le haut de la chaîne de la fenêtre parente jusqu’à ce qu’il atteigne la fenêtre de niveau supérieur. Les applications peuvent répondre à ce message pour spécifier s’ils souhaitent être activés.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_POINTERACTIVATE             0x024B
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Contient l’identificateur du pointeur et des informations supplémentaires. Utilisez les macros suivantes pour récupérer ces informations.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : identificateur de pointeur

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam) : valeur de test de positionnement retournée par le traitement du message de [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .

</dd> <dt>

*lParam* 
</dt> <dd>

Contient le handle de la fenêtre de niveau supérieur de la fenêtre en cours d’activation.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si une application traite ce message, elle doit retourner l’une des valeurs décrites dans la section Notes.

Si l’application ne traite pas ce message, elle doit appeler [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Notes

Une application peut gérer ce message et retourner l’une des valeurs suivantes pour déterminer comment le système traite l’activation et l’entrée d’activation :

-   PA_ACTIVATE
-   PA_NOACTIVATE

Il est important de noter que, lorsque l’utilisateur interagit avec le système avec plusieurs pointeurs simultanés, l’opportunité d’activation que le message **WM_POINTERACTIVATE** représente est disponible pour les applications uniquement pour le premier de ces pointeurs. Les applications doivent donc être conscientes qu’elles peuvent toujours recevoir des entrées des pointeurs alors qu’elles sont inactives.

Si l’application ne gère pas ce message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) transmet le message à la fenêtre parente.

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

 

