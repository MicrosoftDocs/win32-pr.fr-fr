---
description: Une application envoie le \_ message WM MDIICONARRANGE à une fenêtre cliente d’interface multidocument (MDI) pour réorganiser toutes les fenêtres enfants MDI réduites. Elle n’affecte pas les fenêtres enfants qui ne sont pas réduites.
ms.assetid: 935b9e29-224d-449e-b89f-b6062bed7702
title: Message WM_MDIICONARRANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bacb38a03ab71f185bd4db0618e3f0180515f7af370e0cab3cc1ac9010dd3edd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030807"
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

## <a name="requirements"></a>Conditions requises



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

**Méthodologique**
</dt> <dt>

[Interface multidocument](multiple-document-interface.md)
</dt> </dl>

 

 




