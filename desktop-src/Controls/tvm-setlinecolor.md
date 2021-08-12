---
title: Message TVM_SETLINECOLOR (commctrl. h)
description: Le \_ message TVM SETLINECOLOR définit la couleur de la ligne active.
ms.assetid: c5fc28af-5603-489f-aa6b-73e153f9aebc
keywords:
- TVM_SETLINECOLOR les contrôles de Windows de message
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
ms.openlocfilehash: af66e7a711611ff5e59ec0d68b58a24fb39399245437b0e5d81840c1c38b2d0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669519"
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

## <a name="remarks"></a>Remarques

Ce message modifie uniquement les couleurs des lignes. Pour modifier les couleurs de' + 'et'-'à l’intérieur des boutons, utilisez le message [**TVM \_ SETTEXTCOLOR**](tvm-settextcolor.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVM \_ GETLINECOLOR**](tvm-getlinecolor.md)
</dt> </dl>

 

 





