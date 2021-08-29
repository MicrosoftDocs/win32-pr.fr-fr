---
description: récupère le rectangle englobant de la barre des tâches Windows.
ms.assetid: 8072bb2d-05e6-4baa-a7f4-1377b94fdd45
title: Message ABM_GETTASKBARPOS (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ea826756ea083996ec6de9218cdacad3b99a6aad50d52d5da67fc1908e8efca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884859"
---
# <a name="abm_gettaskbarpos-message"></a>\_Message ABM GETTASKBARPOS

récupère le rectangle englobant de la barre des tâches Windows.


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

## <a name="remarks"></a>Remarques

Notez que cela s’applique uniquement à la barre des tâches système. D’autres objets, en particulier les barres d’outils fournies avec des logiciels tiers, peuvent également être présents. par conséquent, une partie de la zone d’écran non couverte par la barre des tâches Windows peut ne pas être visible par l’utilisateur. Pour récupérer la zone de l’écran non couverte par la barre des tâches et d’autres barres de l’application, la zone de travail disponible pour votre application, utilisez la fonction [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

