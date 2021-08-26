---
description: Une application envoie le \_ message WM MDINEXT à une fenêtre cliente d’interface multidocument (MDI) pour activer la fenêtre enfant suivante ou précédente.
ms.assetid: a4822b99-330a-4094-bad9-b9a5923e02a8
title: Message WM_MDINEXT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aa2b88e5368db2a6b700e0b4d469d1ba680d3caa4d2c1e1c208c5143660396f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931239"
---
# <a name="wm_mdinext-message"></a>\_Message WM MDINEXT

Une application envoie le message **WM \_ MDINEXT** à une fenêtre cliente d’interface multidocument (MDI) pour activer la fenêtre enfant suivante ou précédente.


```C++
#define WM_MDINEXT                      0x0224
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre enfant MDI. Le système active la fenêtre enfant qui est immédiatement avant ou après la fenêtre enfant spécifiée, selon la valeur du paramètre *lParam* . Si le paramètre *wParam* est **null**, le système active la fenêtre enfant qui est immédiatement avant ou après la fenêtre enfant actuellement active.

</dd> <dt>

*lParam* 
</dt> <dd>

Si ce paramètre est égal à zéro, le système active la fenêtre enfant MDI suivante et place la fenêtre enfant identifiée par le paramètre *wParam* derrière toutes les autres fenêtres enfants. Si ce paramètre est différent de zéro, le système active la fenêtre enfant précédente, en la plaçant devant la fenêtre enfant identifiée par *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **zéro**

La valeur de retour est toujours zéro.

## <a name="remarks"></a>Remarques

Si une fenêtre cliente MDI reçoit un message qui modifie l’activation de ses fenêtres enfants alors que la fenêtre enfant MDI active est agrandie, le système restaure la fenêtre enfant active et agrandit la fenêtre enfant qui vient d’être activée.

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

[**\_MDIACTIVATE WM**](wm-mdiactivate.md)
</dt> <dt>

[**\_MDIGETACTIVE WM**](wm-mdigetactive.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Interface multidocument](multiple-document-interface.md)
</dt> </dl>

 

 




