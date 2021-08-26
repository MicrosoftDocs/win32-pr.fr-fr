---
title: Message TVM_MAPACCIDTOHTREEITEM (commctrl. h)
description: Cartes un ID d’accessibilité à un HTREEITEM.
ms.assetid: f4feb7cb-2138-4930-b8ee-b9e2d4b19001
keywords:
- TVM_MAPACCIDTOHTREEITEM les contrôles de Windows de message
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
ms.openlocfilehash: f6481d8db806156d10536ac0ec7c66fdeb4693a1133365767b4c3dc37ad8420f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045799"
---
# <a name="tvm_mapaccidtohtreeitem-message"></a>TVM \_ MAPACCIDTOHTREEITEM message

Cartes un ID d’accessibilité à un **HTREEITEM**.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>**Uint** qui contient l’ID d’accessibilité à mapper à un **HTREEITEM**. </dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le **HTREEITEM** auquel l’ID d’accessibilité spécifié est mappé.

## <a name="remarks"></a>Remarques

Lorsque vous ajoutez un élément à un contrôle Tree-View, un **HTREEITEM** retourne, qui identifie de façon unique l’élément.

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_MapAccIDToHTREEITEM TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
</dt> </dl>

 

 





