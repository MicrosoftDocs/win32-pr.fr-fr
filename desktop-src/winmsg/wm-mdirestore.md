---
description: Une application envoie le \_ message WM MDIRESTORE à une fenêtre cliente d’interface multidocument (MDI) pour restaurer une fenêtre enfant MDI de taille agrandie ou réduite.
ms.assetid: bb99fda1-9eb5-4307-9326-9a417a046c22
title: Message WM_MDIRESTORE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8bc9a8b4a414a1f987ad51b01f94c50b336adb8a32a298a83a1a3b9de8b0bd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110698"
---
# <a name="wm_mdirestore-message"></a>\_Message WM MDIRESTORE

Une application envoie le message **WM \_ MDIRESTORE** à une fenêtre cliente d’interface multidocument (MDI) pour restaurer une fenêtre enfant MDI de taille agrandie ou réduite.


```C++
#define WM_MDIRESTORE                   0x0223
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre enfant MDI à restaurer.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **zéro**

La valeur de retour est toujours zéro.

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

[**\_MDIMAXIMIZE WM**](wm-mdimaximize.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Interface multidocument](multiple-document-interface.md)
</dt> </dl>

 

 




