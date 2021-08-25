---
title: Message CB_GETDROPPEDSTATE (winuser. h)
description: Détermine si la zone de liste d’une zone de liste déroulante est déroulée.
ms.assetid: a3f4e352-298d-45ea-a5a7-007f1fc1a387
keywords:
- CB_GETDROPPEDSTATE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_GETDROPPEDSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1674406b4dc5a4dd5e7985ba497fce8ef93e7c3480c050db0420b541c6d2ab6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089249"
---
# <a name="cb_getdroppedstate-message"></a>\_Message GETDROPPEDSTATE CB

Détermine si la zone de liste d’une zone de liste déroulante est déroulée.

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

Si la zone de liste est visible, la valeur de retour est **true**; Sinon, la **valeur est false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SHOWDROPDOWN CB**](cb-showdropdown.md)
</dt> </dl>

 

 





