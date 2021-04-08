---
title: Code de notification NM_LDOWN (barre d’outils) (commctrl. h)
description: Avertit la fenêtre parente d’une barre d’outils que le bouton gauche de la souris a été enfoncé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: f5b356fb-265b-4eb0-a5a3-2a22d688f847
keywords:
- Contrôles Windows de code de notification NM_LDOWN (barre d’outils)
topic_type:
- apiref
api_name:
- NM_LDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60f1f05d85aa8885acf31a36098056d68612ba2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843066"
---
# <a name="nm_ldown-toolbar-notification-code"></a>\_Code de notification LDOWN nm (barre d’outils)

Avertit la fenêtre parente d’une barre d’outils que le bouton gauche de la souris a été enfoncé. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_LDOWN

    lpnmmouse = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) qui contient des informations sur ce code de notification. Si l’utilisateur a cliqué sur un élément de la barre d’outils, le membre **dwItemSpec** contient l’identificateur de l’élément et le membre **dwItemData** contient les données de l’élément. Si vous avez cliqué sur un séparateur ou un espace blanc dans la barre d’outils, le membre **dwItemSpec** contient-1.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **false** pour permettre au contrôle de barre d’outils d’effectuer le traitement par défaut de l’événement, ou **true** pour empêcher le contrôle de traiter l’événement.

## <a name="remarks"></a>Notes

Cette notification est envoyée après l’envoi du code de notification de [ \_ liste déroulante TBN](tbn-dropdown.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





