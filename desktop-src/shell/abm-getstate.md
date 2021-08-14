---
description: récupère les états masquer automatiquement et toujours en haut de la barre des tâches Windows.
title: Message ABM_GETSTATE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 18e16752-16be-492b-a4fa-c951e18dc86c
api_name:
- ABM_GETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b1a3618be793f4728dc6184b50b7a4e0e57c3ffd2c4d2cd8acde17372aa031f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225228"
---
# <a name="abm_getstate-message"></a>\_Message ABM GETSTATE

récupère les états masquer automatiquement et toujours en haut de la barre des tâches Windows.


```C++
uState = (UINT) SHAppBarMessage(ABM_GETSTATE, pabd);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pabd* 
</dt> <dd>

Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Vous devez spécifier le membre **cbSize** lors de l’envoi de ce message. tous les autres membres sont ignorés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne zéro si la barre des tâches n’est ni dans l’état de masquage automatique ni toujours en haut. Dans le cas contraire, la valeur de retour est l’une des valeurs suivantes, ou les deux :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Code de retour</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>ABS_ALWAYSONTOP</strong></dt> </dl></td>
<td>La barre des tâches est dans l’État Always on Top. <br/>
<blockquote>
[!Note]<br />
à partir de Windows 7, ABS_ALWAYSONTOP n’est plus renvoyé car la barre des tâches est toujours dans cet état. Le code plus ancien doit être mis à jour pour ignorer l’absence de cette valeur dans ne pas supposer que la valeur de retour signifie que la barre des tâches ne se trouve pas dans l’État Always on Top.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>ABS_AUTOHIDE</strong></dt> </dl></td>
<td>La barre des tâches est dans l’État Masquer automatiquement.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




