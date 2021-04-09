---
title: Message LB_GETSELCOUNT (winuser. h)
description: Obtient le nombre total d’éléments sélectionnés dans une zone de liste à sélection multiple.
ms.assetid: 1597f6d0-e8f2-4e10-8a0e-ef76192e6238
keywords:
- LB_GETSELCOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_GETSELCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed73b387315d1b612241d41e47e6b613a3a75f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103368"
---
# <a name="lb_getselcount-message"></a>\_Message GETSELCOUNT lb

Obtient le nombre total d’éléments sélectionnés dans une zone de liste à sélection multiple.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est le nombre d’éléments sélectionnés dans la zone de liste. Si la zone de liste est une zone de liste à sélection unique, la valeur de retour est LB \_ Err.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETSEL lb**](lb-setsel.md)
</dt> </dl>

 

 





