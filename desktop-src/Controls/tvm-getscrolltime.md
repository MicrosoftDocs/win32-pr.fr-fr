---
title: Message TVM_GETSCROLLTIME (commctrl. h)
description: Récupère la durée maximale de défilement pour le contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetScrollTime TreeView.
ms.assetid: 992d1906-cda3-4ac7-ba90-c681c551ac2e
keywords:
- TVM_GETSCROLLTIME les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_GETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e026a463476d5625f7632d7b6679ce94ca2c8ab6d8c6a050d8938bd46d9858b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408496"
---
# <a name="tvm_getscrolltime-message"></a>TVM \_ GETSCROLLTIME message

Récupère la durée maximale de défilement pour le contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetScrollTime TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la durée maximale de défilement, en millisecondes.

## <a name="remarks"></a>Remarques

La durée maximale de défilement est la durée la plus longue qu’une opération de défilement peut prendre. Le défilement est ajusté afin que le défilement s’effectue dans le délai de défilement maximal. Une opération de défilement peut prendre moins de temps que la valeur maximale.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVM \_ SETSCROLLTIME**](tvm-setscrolltime.md)
</dt> </dl>

 

 





