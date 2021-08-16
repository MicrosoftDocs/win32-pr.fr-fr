---
description: Demande une taille et une position à l’écran pour un appbar.
ms.assetid: 061a30fb-a68a-464e-ad8c-0bda672b57d9
title: Message ABM_QUERYPOS (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f7a5e78b6b040904144a64e1068fea3a3e56c7b42fdfcf314f2ced4bfff9e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225030"
---
# <a name="abm_querypos-message"></a>\_Message ABM QUERYPOS

Demande une taille et une position à l’écran pour un appbar. Lorsque la demande est effectuée, le message propose un bord d’écran et un rectangle englobant pour le appbar. le système ajuste le rectangle englobant de sorte que le appbar n’interfère pas avec la barre des tâches Windows ou tout autre barres.


```C++
SHAppBarMessage(ABM_QUERYPOS, pabd); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pabd* 
</dt> <dd>

Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Le membre **uEdge** spécifie un bord d’écran et le membre **RC** contient le rectangle englobant proposé. Lorsque la fonction [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) retourne, **RC** contient le rectangle englobant approuvé. Vous devez spécifier les membres **cbSize**, **HWND**, **uEdge** et **RC** lors de l’envoi de ce message. tous les autres membres sont ignorés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne toujours la **valeur true**.

## <a name="remarks"></a>Remarques

Un appbar doit envoyer ce message avant d’envoyer le message [**ABM \_ SetPos**](abm-setpos.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




