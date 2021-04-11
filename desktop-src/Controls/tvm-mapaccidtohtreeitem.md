---
title: Message TVM_MAPACCIDTOHTREEITEM (commctrl. h)
description: Mappe un ID d’accessibilité à un HTREEITEM.
ms.assetid: f4feb7cb-2138-4930-b8ee-b9e2d4b19001
keywords:
- TVM_MAPACCIDTOHTREEITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_MAPACCIDTOHTREEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b827b18387723fe4792321f7932e1abb3673466e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032598"
---
# <a name="tvm_mapaccidtohtreeitem-message"></a>TVM \_ MAPACCIDTOHTREEITEM message

Mappe un ID d’accessibilité à un **HTREEITEM**.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>**Uint** qui contient l’ID d’accessibilité à mapper à un **HTREEITEM**. </dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le **HTREEITEM** auquel l’ID d’accessibilité spécifié est mappé.

## <a name="remarks"></a>Notes

Lorsque vous ajoutez un élément à un contrôle Tree-View, un **HTREEITEM** retourne, qui identifie de façon unique l’élément.

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

[**\_MapAccIDToHTREEITEM TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
</dt> </dl>

 

 





