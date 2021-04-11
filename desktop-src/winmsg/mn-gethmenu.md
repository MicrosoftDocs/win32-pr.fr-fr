---
description: Récupère le handle de menu pour la fenêtre active.
ms.assetid: a2f6e917-39ff-42a3-8ff4-ce01db3ef9ea
title: Message MN_GETHMENU (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64d501654af426a292156d05242b372336eee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104202917"
---
# <a name="mn_gethmenu-message"></a>MN \_ message GETHMENU

Récupère le handle de menu pour la fenêtre active.


```C++
#define MN_GETHMENU                     0x01E1
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HMENU**

En cas de réussite, la valeur de retour est **HMENU** pour la fenêtre active. En cas d’échec, la valeur de retour est **null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



 

 




