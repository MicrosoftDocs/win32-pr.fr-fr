---
description: Définit les États Masquer automatiquement et toujours en haut de la barre des tâches Windows.
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
ms.openlocfilehash: 3cd21ca49d1a57d870c26e010420f978f1d9b88a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972094"
---
# <a name="abm_setstate-message"></a>\_Message ABM SETSTATE

Définit les États Masquer automatiquement et toujours en haut de la barre des tâches Windows.


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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




