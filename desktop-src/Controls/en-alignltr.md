---
title: Code de notification EN_ALIGNLTR (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit que la direction du paragraphe est passée de gauche à droite. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message de commande WM.
ms.assetid: 754ac2b5-bcec-487b-a1ab-b653f673830a
keywords:
- EN_ALIGNLTR les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- EN_ALIGNLTR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 884f2750501dc1670d2f8e0497a196276571328809d295a687b3518a34b38ec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019447"
---
# <a name="en_alignltr-notification-code"></a>\_Code de notification en ALIGNLTR

Avertit une fenêtre parente d’un contrôle RichEdit que la direction du paragraphe est passée de gauche à droite. Un contrôle RichEdit envoie ce code de notification sous la forme d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_ALIGNLTR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle Rich Edit. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle du contrôle RichEdit.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce code de notification ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**en \_ ALIGNRTL**](en-alignrtl.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM, \_ commande**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

