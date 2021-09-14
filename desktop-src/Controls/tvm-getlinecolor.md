---
title: Message TVM_GETLINECOLOR (commctrl. h)
description: Le \_ message TVM GETLINECOLOR obtient la couleur de la ligne active.
ms.assetid: e74441b3-5d4f-4454-b896-2e96ce649419
keywords:
- TVM_GETLINECOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_GETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd55149f38fb17238e13135e798ebbe55b15009
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115669"
---
# <a name="tvm_getlinecolor-message"></a>TVM \_ GETLINECOLOR message

Le message **TVM \_ GETLINECOLOR** obtient la couleur de la ligne active.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la couleur de la ligne active ou la \_ valeur CLR par défaut si aucune valeur n’a été spécifiée.

## <a name="remarks"></a>Notes

Ce message récupère uniquement les couleurs de ligne. Pour récupérer les couleurs de' + 'et'-'à l’intérieur des boutons, utilisez le message [**TVM \_ GETTEXTCOLOR**](tvm-gettextcolor.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVM \_ SETLINECOLOR**](tvm-setlinecolor.md)
</dt> </dl>

 

 





