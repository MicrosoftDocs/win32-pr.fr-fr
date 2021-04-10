---
title: Message LB_GETLISTBOXINFO (winuser. h)
description: Obtient le nombre d’éléments par colonne dans une zone de liste spécifiée.
ms.assetid: 925bebd9-2563-4892-a7d7-73d4ef012b42
keywords:
- LB_GETLISTBOXINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_GETLISTBOXINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f49f96e3f12b1c21e81e8b5358e174e576d07f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032757"
---
# <a name="lb_getlistboxinfo-message"></a>\_Message GETLISTBOXINFO lb

Obtient le nombre d’éléments par colonne dans une zone de liste spécifiée.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est le nombre d’éléments par colonne.

## <a name="remarks"></a>Notes

Ce message est équivalent à [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo)
</dt> </dl>

 

 





