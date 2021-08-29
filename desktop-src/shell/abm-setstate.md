---
description: définit les états masquer automatiquement et toujours en haut de la barre des tâches Windows.
title: Message ABM_SETSTATE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a60e156d-19ef-49b9-83fc-138d1a2169f2
api_name:
- ABM_SETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1a50671a750f8ca1800cea200c2c58828803bc8a45ae055082c5b6d78959dd12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710869"
---
# <a name="abm_setstate-message"></a>\_Message ABM SETSTATE

définit les états masquer automatiquement et toujours en haut de la barre des tâches Windows.


```C++
SHAppBarMessage(ABM_SETSTATE, pabd); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pabd* 
</dt> <dd>

Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Vous devez spécifier les membres **cbSize** et **HWND** lors de l’envoi de ce message. Les données de l’état souhaité sont envoyées dans le membre **lParam** en utilisant l’une des valeurs suivantes.

<dt>

<span id="0"></span>

<span id="0"></span>**entre**


</dt> <dd>

Masquage automatique et Always on-Top

</dd> <dt>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**\_ALWAYSONTOP ABS**


</dt> <dd>

Always on-Top on, masquage automatique désactivé

</dd> <dt>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**\_masquage automatique ABS**


</dt> <dd>

Masquer automatiquement activé, toujours en haut

</dd> <dt>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**ABS- \_ Masquer automatiquement \| ABS \_ ALWAYSONTOP**


</dt> <dd>

Masquer automatiquement et toujours en haut sur

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne toujours la **valeur true**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




