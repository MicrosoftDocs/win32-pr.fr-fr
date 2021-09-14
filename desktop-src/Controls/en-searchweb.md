---
title: EN_SEARCHWEB le code de notification (CommCtrl. h)
description: Envoyé lorsqu’un contrôle d’édition perd le focus clavier. La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un \_ message WM Notify.
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- EN_SEARCHWEB les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- EN_SEARCHWEB
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 2b995c90e8f4a607d7181adc8a357314acb84dc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006311"
---
# <a name="en_searchweb-notification-code"></a>\_Code de notification en SEARCHWEB

Envoyé après qu’un contrôle d’édition a effectué une recherche sur le Web lorsque la fonctionnalité « Rechercher sur le Web » est activée, consultez [EM_ENABLESEARCHWEB](em-enablesearchweb.md). La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
EN_SEARCHWEB

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle du contrôle d’édition.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMSEARCHWEB**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb) .

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, 1809 \[ applications de bureau uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2019 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_ENABLESEARCHWEB em**](em-enablesearchweb.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**\_notification WM**](wm-notify.md)
</dt> </dl>

 

 





