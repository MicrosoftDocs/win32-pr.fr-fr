---
title: Message TVM_SETSCROLLTIME (commctrl. h)
description: Définit la durée maximale de défilement pour le contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetScrollTime TreeView.
ms.assetid: b0ad81ba-0621-42b7-8fe1-f3bd5bc16d6a
keywords:
- TVM_SETSCROLLTIME les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b49fab2f662b5ec641d9ffc6cc276f2196d2613e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510976"
---
# <a name="tvm_setscrolltime-message"></a>TVM \_ SETSCROLLTIME message

Définit la durée maximale de défilement pour le contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetScrollTime TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nouvelle durée maximale de défilement, en millisecondes.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le temps de défilement maximal précédent, en millisecondes.

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

[**TVM \_ GETSCROLLTIME**](tvm-getscrolltime.md)
</dt> </dl>

 

 





