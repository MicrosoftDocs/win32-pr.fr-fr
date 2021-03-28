---
description: Indique au système qu’un appbar a été activé. Un appbar doit appeler ce message en réponse au message WM \_ Activate.
ms.assetid: 16011302-7c2d-4c34-9953-51cceb96e4b3
title: Message ABM_ACTIVATE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a44bcc33efcd3d1a9af5e7e2abca33893e9fe9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112366"
---
# <a name="abm_activate-message"></a>ABM \_ activer le message

Indique au système qu’un appbar a été activé. Un appbar doit appeler ce message en réponse au message [**WM \_ Activate**](/windows/desktop/inputdev/wm-activate) .


```C++

SHAppBarMessage(ABM_ACTIVATE, pabd); 

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pabd* 
</dt> <dd>

Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) qui identifie le appbar à activer. Vous devez spécifier les membres **cbSize** et **HWND** lors de l’envoi de ce message. tous les autres membres sont ignorés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne toujours la **valeur true**.

## <a name="remarks"></a>Notes

Ce message est ignoré si le membre **HWND** de la structure vers laquelle pointe *pabd* identifie un appbar de masquage automatique. Le système définit automatiquement l’ordre de plan pour les barres de masquage automatique.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

