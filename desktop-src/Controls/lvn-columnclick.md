---
title: LVN_COLUMNCLICK le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle List-View qu’un clic a été effectué sur un en-tête de colonne alors que le contrôle List-View était en mode rapport. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: a6bfbd6c-4778-47a7-92e9-9140d46d89cc
keywords:
- Contrôles Windows de code de notification LVN_COLUMNCLICK
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
ms.openlocfilehash: 27cfd75d913c62c89c4cfe305333a934fe172fe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032422"
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

## <a name="remarks"></a>Notes

L’utilisation de formats de contrôle d’en-tête tels que HDF \_ case à cocher pour modifier le format des en-têtes de colonnes dans un contrôle List-View entraîne l’envoi par le contrôle du code de notification [ \_ ITEMSTATEICONCLICK HDN](hdn-itemstateiconclick.md) au lieu de LVN \_ COLUMNCLICK lorsqu’un utilisateur clique sur un élément d’en-tête.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





