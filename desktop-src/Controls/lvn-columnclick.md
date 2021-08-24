---
title: LVN_COLUMNCLICK le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle List-View qu’un clic a été effectué sur un en-tête de colonne alors que le contrôle List-View était en mode rapport. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: a6bfbd6c-4778-47a7-92e9-9140d46d89cc
keywords:
- LVN_COLUMNCLICK les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- LVN_COLUMNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74cd88674b10a799f58fd0549a6711f3d00934f7b1baaf892cff86c6ef223d19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319809"
---
# <a name="lvn_columnclick-notification-code"></a>\_Code de notification LVN COLUMNCLICK

Avertit une fenêtre parente d’un contrôle List-View qu’un clic a été effectué sur un en-tête de colonne alors que le contrôle List-View était en mode rapport. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_COLUMNCLICK

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . Le membre **iItem** est-1 et le membre **iSubItem** identifie la colonne. Tous les autres membres sont nuls.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

L’utilisation de formats de contrôle d’en-tête tels que HDF \_ case à cocher pour modifier le format des en-têtes de colonnes dans un contrôle List-View entraîne l’envoi par le contrôle du code de notification [ \_ ITEMSTATEICONCLICK HDN](hdn-itemstateiconclick.md) au lieu de LVN \_ COLUMNCLICK lorsqu’un utilisateur clique sur un élément d’en-tête.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





