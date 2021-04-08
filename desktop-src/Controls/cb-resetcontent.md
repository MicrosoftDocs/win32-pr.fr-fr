---
title: Message CB_RESETCONTENT (winuser. h)
description: Supprime tous les éléments de la zone de liste et le contrôle d’édition d’une zone de liste déroulante.
ms.assetid: 55203c34-87ca-46e9-a914-a480d43ccadd
keywords:
- CB_RESETCONTENT les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3567f31ef98fffe42e53c4811acc786d41ae9f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843565"
---
# <a name="cb_resetcontent-message"></a>\_Message RESETCONTENT CB

Supprime tous les éléments de la zone de liste et le contrôle d’édition d’une zone de liste déroulante.

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

Ce message retourne toujours CB \_ OK.

## <a name="remarks"></a>Notes

Si vous créez la zone de liste déroulante avec un style owner-drawn mais sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , le propriétaire de la zone de liste déroulante reçoit un message [**WM \_ DELETEITEM**](wm-deleteitem.md) pour chaque élément de la zone de liste déroulante.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_DELETESTRING CB**](cb-deletestring.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





