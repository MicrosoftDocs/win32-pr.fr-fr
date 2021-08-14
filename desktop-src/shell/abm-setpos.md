---
description: Définit la taille et la position à l’écran d’un appbar.
ms.assetid: b3c56278-b9a2-4e08-bf98-7b3e4c8bd082
title: Message ABM_SETPOS (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431bbdc02ed202c94d66b6b93ce43aba0ebd40f1fb7058583f56c027cfc29b70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861601"
---
# <a name="abm_setpos-message"></a>\_Message ABM SetPos

Définit la taille et la position à l’écran d’un appbar. Le message spécifie un bord d’écran et le rectangle englobant pour le appbar. le système peut ajuster le rectangle englobant afin que le appbar n’interfère pas avec la barre des tâches Windows ou tout autre barres.


```C++
SHAppBarMessage(ABM_SETPOS, pabd); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pabd* 
</dt> <dd>

Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Le membre **uEdge** spécifie un bord d’écran et le membre **RC** contient le rectangle englobant. Lorsque la fonction [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) retourne, **RC** contient le rectangle englobant approuvé. Vous devez spécifier les membres **cbSize**, **HWND**, **uEdge** et **RC** lors de l’envoi de ce message. tous les autres membres sont ignorés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne toujours la **valeur true**.

## <a name="remarks"></a>Remarques

Ce message amène le système à envoyer le message de notification [**ABN \_ POSCHANGED**](abn-poschanged.md) à tous les barres.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




