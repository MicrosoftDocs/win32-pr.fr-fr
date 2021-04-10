---
title: Message TVM_GETSCROLLTIME (commctrl. h)
description: Récupère la durée maximale de défilement pour le contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetScrollTime TreeView.
ms.assetid: 992d1906-cda3-4ac7-ba90-c681c551ac2e
keywords:
- TVM_GETSCROLLTIME les contrôles de message Windows
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
ms.openlocfilehash: e6f0bacc6c12dd7f54f20d882faf738c11848d59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103209"
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

## <a name="remarks"></a>Notes

La durée maximale de défilement est la durée la plus longue qu’une opération de défilement peut prendre. Le défilement est ajusté afin que le défilement s’effectue dans le délai de défilement maximal. Une opération de défilement peut prendre moins de temps que la valeur maximale.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVM \_ SETSCROLLTIME**](tvm-setscrolltime.md)
</dt> </dl>

 

 





