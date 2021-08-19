---
title: Message LVM_SCROLL (commctrl. h)
description: Fait défiler le contenu d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro de défilement ListView.
ms.assetid: 4bf6b74e-8fea-48ca-a151-8fd649fc50f8
keywords:
- LVM_SCROLL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 604ef35b6d7e62e626aa7cbee32c1563224794781275c470a1b3cd1727b926bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019227"
---
# <a name="lvm_scroll-message"></a>\_Message de défilement LVM

Fait défiler le contenu d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro de [**\_ défilement ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur de type **int** qui spécifie la quantité de défilement horizontal, en pixels, par rapport à la position actuelle du contenu de la vue de liste. Si le contrôle de liste est en mode liste, cette valeur est arrondie au nombre de pixels le plus proche qui forme une colonne entière.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur de type **int** qui spécifie la quantité de défilement vertical, en pixels, par rapport à la position actuelle du contenu de la vue de liste.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite ; Sinon, **false**.

## <a name="remarks"></a>Remarques

Lorsque le contrôle de liste est en mode rapport, le contrôle ne peut être défilé que verticalement dans l’intégralité des incréments de la ligne. Par conséquent, le paramètre *lParam* est arrondi au nombre de pixels le plus proche qui constitue un incrément de ligne entier. Par exemple, si la hauteur d’une ligne est de 16 pixels et que 8 est passé pour *lParam*, la liste défilera de 16 pixels (1 ligne). Si la valeur 7 est passée pour *lParam*, la liste est défilante de 0 pixel (0 ligne).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





