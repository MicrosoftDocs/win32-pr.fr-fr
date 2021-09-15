---
description: Une application envoie le \_ message WM MDIICONARRANGE à une fenêtre cliente d’interface multidocument (MDI) pour réorganiser toutes les fenêtres enfants MDI réduites. Elle n’affecte pas les fenêtres enfants qui ne sont pas réduites.
ms.assetid: 935b9e29-224d-449e-b89f-b6062bed7702
title: Message WM_MDIICONARRANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2d50d4bccebe3e9758752cc7d0d259e973875c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522145"
---
# <a name="wm_mdiiconarrange-message"></a>\_Message WM MDIICONARRANGE

Une application envoie le message **WM \_ MDIICONARRANGE** à une fenêtre cliente d’interface multidocument (MDI) pour réorganiser toutes les fenêtres enfants MDI réduites. Elle n’affecte pas les fenêtres enfants qui ne sont pas réduites.


```C++
#define WM_MDIICONARRANGE               0x0228
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_MDICASCADE WM**](wm-mdicascade.md)
</dt> <dt>

[**\_MDITILE WM**](wm-mditile.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Interface multidocument](multiple-document-interface.md)
</dt> </dl>

 

 




