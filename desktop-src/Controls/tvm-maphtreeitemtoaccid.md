---
title: Message TVM_MAPHTREEITEMTOACCID (commctrl. h)
description: Mappe un HTREEITEM à un ID d’accessibilité.
ms.assetid: 87ef0785-88c1-49f4-8a05-872577e16fe4
keywords:
- TVM_MAPHTREEITEMTOACCID les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103720"
---
# <a name="tvm_maphtreeitemtoaccid-message"></a>TVM \_ MAPHTREEITEMTOACCID message

Mappe un **HTREEITEM** à un ID d’accessibilité.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>**HTREEITEM** mappé à un ID d’accessibilité.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un ID d’accessibilité.

## <a name="remarks"></a>Notes

Lorsque vous ajoutez un élément à un contrôle Tree-View, un descripteur **HTREEITEM** qui identifie de façon unique l’élément est retourné.

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_MapHTREEITEMtoAccID TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_maphtreeitemtoaccid)
</dt> </dl>

 

 





