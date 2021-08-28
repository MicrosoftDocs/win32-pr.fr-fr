---
title: Message TVM_GETVISIBLECOUNT (commctrl. h)
description: Obtient le nombre d’éléments qui peuvent être complètement visibles dans la fenêtre cliente d’un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetVisibleCount TreeView.
ms.assetid: c3519543-3fb2-4ecf-ac01-905d0946cb1b
keywords:
- TVM_GETVISIBLECOUNT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_GETVISIBLECOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07604eed3d3ece140d33bb9c612a2f898f6de02785f2c9916332de60358693fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698658"
---
# <a name="tvm_getvisiblecount-message"></a>TVM \_ GETVISIBLECOUNT message

Obtient le nombre d’éléments qui peuvent être complètement visibles dans la fenêtre cliente d’un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetVisibleCount TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le nombre d’éléments qui peuvent être complètement visibles dans la fenêtre cliente du contrôle Tree-View.

## <a name="remarks"></a>Remarques

Le nombre d’éléments pouvant être entièrement visibles peut être supérieur au nombre d’éléments dans le contrôle. Le contrôle calcule cette valeur en divisant la hauteur de la fenêtre client par la hauteur d’un élément.

Notez que la valeur de retour est le nombre d’éléments qui peuvent être *entièrement* visibles. Si vous pouvez voir tous les 20 éléments et une partie d’un autre élément, la valeur de retour est 20.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





