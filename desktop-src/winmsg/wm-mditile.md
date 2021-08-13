---
description: Une application envoie le \_ message WM MDITILE à une fenêtre cliente d’interface multidocument (MDI) pour réorganiser toutes ses fenêtres enfants MDI dans un format de vignette.
ms.assetid: a480ba61-807e-4d0e-bda2-f1876e0bb13c
title: Message WM_MDITILE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379394d413c0c9d15b9f63297934b97da6aff65b4ae5d803627cb0107493c4e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436216"
---
# <a name="wm_mditile-message"></a>\_Message WM MDITILE

Une application envoie le message **WM \_ MDITILE** à une fenêtre cliente d’interface multidocument (MDI) pour réorganiser toutes ses fenêtres enfants MDI dans un format de vignette.


```C++
#define WM_MDITILE                      0x0226
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Option de mosaïque. Ce paramètre peut avoir l’une des valeurs suivantes, éventuellement combinées avec **MDITILE \_ SKIPDISABLED** pour empêcher les fenêtres enfants MDI désactivées d’être présentées en mosaïque.



| Valeur                                                                                                                                                                                                                                    | Signification                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MDITILE_HORIZONTAL"></span><span id="mditile_horizontal"></span><dl> <dt>**MDITILE \_**</dt> <dt>0x0001</dt> horizontal </dl> | Mosaïques horizontalement les fenêtres.<br/> |
| <span id="MDITILE_VERTICAL"></span><span id="mditile_vertical"></span><dl> <dt>**MDITILE \_ VERTICAL**</dt> <dt>0x0000</dt> </dl>       | Mosaïque verticalement les fenêtres.<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **bool**

Si le message est correctement exécuté, la valeur de retour est **true**.

Si le message échoue, la valeur de retour est **false**.

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

[**\_MDICASCADE WM**](wm-mdicascade.md)
</dt> <dt>

[**\_MDIICONARRANGE WM**](wm-mdiiconarrange.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Interface multidocument](multiple-document-interface.md)
</dt> </dl>

 

 




