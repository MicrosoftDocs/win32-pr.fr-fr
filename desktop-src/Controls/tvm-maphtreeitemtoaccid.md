---
title: Message TVM_MAPHTREEITEMTOACCID (commctrl. h)
description: Cartes un HTREEITEM à un ID d’accessibilité.
ms.assetid: 87ef0785-88c1-49f4-8a05-872577e16fe4
keywords:
- TVM_MAPHTREEITEMTOACCID les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_MAPHTREEITEMTOACCID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6267c2040583917283fc444db74ddacbdabd69
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115626"
---
# <a name="tvm_maphtreeitemtoaccid-message"></a>TVM \_ MAPHTREEITEMTOACCID message

Cartes un **HTREEITEM** à un ID d’accessibilité.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>**HTREEITEM** mappé à un ID d’accessibilité.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne un ID d’accessibilité.

## <a name="remarks"></a>Notes

Lorsque vous ajoutez un élément à un contrôle Tree-View, un descripteur **HTREEITEM** qui identifie de façon unique l’élément est retourné.

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_MapHTREEITEMtoAccID TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_maphtreeitemtoaccid)
</dt> </dl>

 

 





