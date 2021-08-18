---
description: Indique au système qu’un appbar a été activé. Un appbar doit appeler ce message en réponse au message WM \_ Activate.
ms.assetid: 16011302-7c2d-4c34-9953-51cceb96e4b3
title: Message ABM_ACTIVATE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 224f04a88a1e69a1a67fc08c6018d33af2bcdbc6f34ff9fbd00d1dd76f82ce5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118461132"
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

## <a name="remarks"></a>Remarques

Ce message est ignoré si le membre **HWND** de la structure vers laquelle pointe *pabd* identifie un appbar de masquage automatique. Le système définit automatiquement l’ordre de plan pour les barres de masquage automatique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

