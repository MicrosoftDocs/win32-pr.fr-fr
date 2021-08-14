---
title: RBN_CHEVRONPUSHED le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar lorsqu’un chevron fait l’objet d’un push. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 58aa2c9d-8ab6-46ee-b32f-5c04fb7afa84
keywords:
- RBN_CHEVRONPUSHED les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- RBN_CHEVRONPUSHED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f5f8d52558251524e9d978c52ae703565a9641febdd53190925cfb8b127160
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985319"
---
# <a name="rbn_chevronpushed-notification-code"></a>\_Code de notification RBN CHEVRONPUSHED

Envoyé par un contrôle rebar lorsqu’un chevron fait l’objet d’un push. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
RBN_CHEVRONPUSHED

    lpnm = (NMREBARCHEVRON) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la structure [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) de la bande.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de cette notification n’est pas utilisée.

## <a name="remarks"></a>Remarques

Lorsqu’une application reçoit ce code de notification, il est chargé d’afficher un menu contextuel contenant des éléments pour chaque outil masqué. Utilisez le membre **RC** de la structure [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) pour rechercher la position correcte du menu contextuel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





