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
ms.openlocfilehash: 56ed83649795ccbd9b41270272f5a8984ddf257c3f5881a0c0fb69232081974e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913999"
---
# <a name="tvm_getlinecolor-message"></a>TVM \_ GETLINECOLOR message

Le message **TVM \_ GETLINECOLOR** obtient la couleur de la ligne active.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la couleur de la ligne active ou la \_ valeur CLR par défaut si aucune valeur n’a été spécifiée.

## <a name="remarks"></a>Remarques

Ce message récupère uniquement les couleurs de ligne. Pour récupérer les couleurs de' + 'et'-'à l’intérieur des boutons, utilisez le message [**TVM \_ GETTEXTCOLOR**](tvm-gettextcolor.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVM \_ SETLINECOLOR**](tvm-setlinecolor.md)
</dt> </dl>

 

 





