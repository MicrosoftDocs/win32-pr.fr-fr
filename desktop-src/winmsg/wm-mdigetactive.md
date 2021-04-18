---
description: Une application envoie le \_ message WM MDIGETACTIVE à une fenêtre cliente d’interface multidocument (MDI) pour récupérer le handle de la fenêtre enfant MDI active.
ms.assetid: 3ee445be-dd55-4825-8508-fa18a346ffcd
title: Message WM_MDIGETACTIVE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49f4ec321f526cd4c9766555e2361ef2cfbd040
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520038"
---
# <a name="wm_mdigetactive-message"></a>\_Message WM MDIGETACTIVE

Une application envoie le message **WM \_ MDIGETACTIVE** à une fenêtre cliente d’interface multidocument (MDI) pour récupérer le handle de la fenêtre enfant MDI active.


```C++
#define WM_MDIGETACTIVE                  0x0229
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

État agrandi. Si ce paramètre n’est pas **null**, il s’agit d’un pointeur vers une valeur qui indique l’État agrandi de la fenêtre enfant MDI. Si la valeur est **true**, la fenêtre est agrandie ; la valeur **false** indique qu’elle ne l’est pas. Si ce paramètre a la **valeur null**, le paramètre est ignoré.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HWND**

La valeur de retour est le handle de la fenêtre enfant MDI active.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble de l’interface multidocument](multiple-document-interface.md)
</dt> </dl>

 

 




