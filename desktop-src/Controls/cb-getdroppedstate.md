---
title: Message CB_GETDROPPEDSTATE (winuser. h)
description: Détermine si la zone de liste d’une zone de liste déroulante est déroulée.
ms.assetid: a3f4e352-298d-45ea-a5a7-007f1fc1a387
keywords:
- CB_GETDROPPEDSTATE les contrôles de message Windows
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
ms.openlocfilehash: 5ae321bbaa3078a04ffc97d4a8083a674d03d651
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033274"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SHOWDROPDOWN CB**](cb-showdropdown.md)
</dt> </dl>

 

 





