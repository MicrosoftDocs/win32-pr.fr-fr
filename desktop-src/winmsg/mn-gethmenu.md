---
description: Récupère le handle de menu pour la fenêtre active.
ms.assetid: a2f6e917-39ff-42a3-8ff4-ce01db3ef9ea
title: Message MN_GETHMENU (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92cfc1eb6086f94f64e1a0e152e6f86fe89a0ea0278a6c4cc25a487edb6f93ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089929"
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



 

 




