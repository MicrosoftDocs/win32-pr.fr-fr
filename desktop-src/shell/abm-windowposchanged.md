---
description: Notifie le système lorsque la position d’un appbar a changé. Un appbar doit appeler ce message en réponse au message WM \_ WINDOWPOSCHANGED.
ms.assetid: 8ca51f5f-b6cf-4f2c-98f4-69c992679320
title: Message ABM_WINDOWPOSCHANGED (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d770d50629342095308376856b98e6250adc1f9a1f2559da8509d685995428ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057809"
---
# <a name="abm_windowposchanged-message"></a>\_Message ABM WINDOWPOSCHANGED

Notifie le système lorsque la position d’un appbar a changé. Un appbar doit appeler ce message en réponse au message [**WM \_ WINDOWPOSCHANGED**](/windows/desktop/winmsg/wm-windowposchanged) .


```C++
SHAppBarMessage(ABM_WINDOWPOSCHANGED, pabd); 
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

Ce message est ignoré si le membre **HWND** de la structure vers laquelle pointe *pabd* identifie un appbar de masquage automatique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

