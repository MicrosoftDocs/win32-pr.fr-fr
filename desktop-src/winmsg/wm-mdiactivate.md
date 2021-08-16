---
description: Une application envoie le \_ message WM MDIACTIVATE à une fenêtre cliente d’interface multidocument (MDI, multiple-document interface) pour indiquer à la fenêtre cliente d’activer une autre fenêtre enfant MDI.
ms.assetid: c5de18b5-fac3-4e55-9eca-3b6672df0e7b
title: Message WM_MDIACTIVATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e8b71e0f3755d76ecb44d60eecbd3b92c124aa59339a6fbf59a098b1eeb274f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931269"
---
# <a name="wm_mdiactivate-message"></a>\_Message WM MDIACTIVATE

Une application envoie le message **WM \_ MDIACTIVATE** à une fenêtre cliente d’interface multidocument (MDI, multiple-document interface) pour indiquer à la fenêtre cliente d’activer une autre fenêtre enfant MDI.


```C++
#define WM_MDIACTIVATE                  0x0222
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre enfant MDI à activer.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Si une application envoie ce message à une fenêtre cliente MDI, la valeur de retour est zéro.

Une fenêtre enfant MDI doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Remarques

Lorsque la fenêtre cliente traite ce message, il envoie **WM \_ MDIACTIVATE** à la fenêtre enfant qui est désactivée et à la fenêtre enfant en cours d’activation. Les paramètres de message reçus par une fenêtre enfant MDI sont les suivants :

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Handle de la fenêtre enfant MDI en cours de désactivation.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Handle de la fenêtre enfant MDI en cours d’activation.

</dd> </dl>

Une fenêtre enfant MDI est activée indépendamment de la fenêtre frame MDI. Lorsque la fenêtre frame devient active, la fenêtre enfant qui a été activée pour la dernière fois à l’aide du message **WM \_ MDIACTIVATE** reçoit le message [**WM \_ NCACTIVATE**](wm-ncactivate.md) pour dessiner un cadre de fenêtre et une barre de titre active ; la fenêtre enfant ne reçoit pas un autre message **WM \_ MDIACTIVATE** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_MDIGETACTIVE WM**](wm-mdigetactive.md)
</dt> <dt>

[**\_MDINEXT WM**](wm-mdinext.md)
</dt> <dt>

[**\_NCACTIVATE WM**](wm-ncactivate.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Interface multidocument](multiple-document-interface.md)
</dt> </dl>

 

 




