---
title: Message RB_INSERTBAND (commctrl. h)
description: Insère une nouvelle bande dans un contrôle rebar.
ms.assetid: ac621f65-b8ab-41d6-928d-a48fbea572e7
keywords:
- RB_INSERTBAND les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_INSERTBAND
- RB_INSERTBANDA
- RB_INSERTBANDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39b45eb662fb4c2058b87837352339c84762188
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844457"
---
# <a name="rb_insertband-message"></a>\_Message INSERTBAND RB

Insère une nouvelle bande dans un contrôle rebar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de l’emplacement où la bande sera insérée. Si vous affectez la valeur-1 à ce paramètre, le contrôle ajoutera la nouvelle bande au dernier emplacement.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) qui définit la bande à insérer. Vous devez définir le membre **cbSize** de cette structure sur **sizeof**(REBARBANDINFO) avant d’envoyer ce message.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **RB \_ INSERTBANDW** (Unicode) et **RB \_ INSERTBANDA** (ANSI)<br/>               |



 

 





