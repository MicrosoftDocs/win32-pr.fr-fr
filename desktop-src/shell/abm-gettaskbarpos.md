---
description: Récupère le rectangle englobant de la barre des tâches Windows.
ms.assetid: 8072bb2d-05e6-4baa-a7f4-1377b94fdd45
title: Message ABM_GETTASKBARPOS (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb678b6e7ade1f148d2deb4b0de6c8953f019d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525431"
---
# <a name="abm_gettaskbarpos-message"></a>\_Message ABM GETTASKBARPOS

Récupère le rectangle englobant de la barre des tâches Windows.


```C++
fResult = (BOOL) SHAppBarMessage(ABM_GETTASKBARPOS, pabd);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pabd* 
</dt> <dd>

Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) dont le membre **RC** reçoit le rectangle englobant, en coordonnées d’écran, de la barre des tâches. Vous devez spécifier le **cbSize** lors de l’envoi de ce message. tous les autres membres sont ignorés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite ; Sinon, **false**.

## <a name="remarks"></a>Notes

Notez que cela s’applique uniquement à la barre des tâches système. D’autres objets, en particulier les barres d’outils fournies avec des logiciels tiers, peuvent également être présents. Par conséquent, une partie de la zone d’écran non couverte par la barre des tâches Windows peut ne pas être visible pour l’utilisateur. Pour récupérer la zone de l’écran non couverte par la barre des tâches et d’autres barres de l’application, la zone de travail disponible pour votre application, utilisez la fonction [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

