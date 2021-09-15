---
description: Une application envoie le \_ message WM MDIRESTORE à une fenêtre cliente d’interface multidocument (MDI) pour restaurer une fenêtre enfant MDI de taille agrandie ou réduite.
ms.assetid: bb99fda1-9eb5-4307-9326-9a417a046c22
title: Message WM_MDIRESTORE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc2cf36a0b428e1e9003682a5e766f613fd7ba81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404712"
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

## <a name="return-value"></a>Valeur de retour

Type : **zéro**

La valeur de retour est toujours zéro.

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

[**\_MDIMAXIMIZE WM**](wm-mdimaximize.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Interface multidocument](multiple-document-interface.md)
</dt> </dl>

 

 




