---
title: Message TVM_SETLINECOLOR (commctrl. h)
description: Le \_ message TVM SETLINECOLOR définit la couleur de la ligne active.
ms.assetid: c5fc28af-5603-489f-aa6b-73e153f9aebc
keywords:
- TVM_SETLINECOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70340ea0d2339055faa3fb473269f3b244f335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032971"
---
# <a name="tvm_setlinecolor-message"></a>TVM \_ SETLINECOLOR message

Le message **TVM \_ SETLINECOLOR** définit la couleur de la ligne active.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Nouvelle couleur de ligne. Utilisez la \_ valeur CLR par défaut pour restaurer les couleurs par défaut du système.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la couleur de ligne précédente.

## <a name="remarks"></a>Notes

Ce message modifie uniquement les couleurs des lignes. Pour modifier les couleurs de' + 'et'-'à l’intérieur des boutons, utilisez le message [**TVM \_ SETTEXTCOLOR**](tvm-settextcolor.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVM \_ GETLINECOLOR**](tvm-getlinecolor.md)
</dt> </dl>

 

 





