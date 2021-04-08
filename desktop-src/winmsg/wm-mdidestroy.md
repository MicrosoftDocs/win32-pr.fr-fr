---
description: Une application envoie le \_ message WM MDIDESTROY à une fenêtre cliente d’interface multidocument (MDI) pour fermer une fenêtre enfant MDI.
ms.assetid: b415393d-a5c2-4b70-af18-0dc7b3939a47
title: Message WM_MDIDESTROY (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edea8fe8dadc691ca912df4e9ee5d57421124bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751212"
---
# <a name="wm_mdidestroy-message"></a>\_Message WM MDIDESTROY

Une application envoie le message **WM \_ MDIDESTROY** à une fenêtre cliente d’interface multidocument (MDI) pour fermer une fenêtre enfant MDI.


```C++
#define WM_MDIDESTROY                   0x0221
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre enfant MDI à fermer.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **zéro**

Ce message retourne toujours la valeur zéro.

## <a name="remarks"></a>Notes

Ce message supprime le titre de la fenêtre enfant MDI de la fenêtre frame MDI et désactive la fenêtre enfant. Une application doit utiliser ce message pour fermer toutes les fenêtres enfants MDI.

Si une fenêtre cliente MDI reçoit un message qui modifie l’activation de ses fenêtres enfants et que la fenêtre enfant MDI active est agrandie, le système restaure la fenêtre enfant active et agrandit la fenêtre enfant qui vient d’être activée.

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

[**\_MDICREATE WM**](wm-mdicreate.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Interface multidocument](multiple-document-interface.md)
</dt> </dl>

 

 




