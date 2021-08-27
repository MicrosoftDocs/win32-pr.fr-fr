---
title: Message HDM_GETORDERARRAY (commctrl. h)
description: Obtient l’ordre de gauche à droite actuel des éléments dans un contrôle header. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ GetOrderArray.
ms.assetid: b287d3c1-ae61-41a4-a884-dc008eb24ad8
keywords:
- HDM_GETORDERARRAY les contrôles de Windows de message
topic_type:
- apiref
api_name:
- HDM_GETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f374424fe3f1d84c4919c26948486a9bae1660072975556aecaac4b08b85b33b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062829"
---
# <a name="hdm_getorderarray-message"></a>\_Message HDM GETORDERARRAY

Obtient l’ordre de gauche à droite actuel des éléments dans un contrôle header. Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ GetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre d’éléments entiers que *lParam* peut contenir. Cette valeur doit être égale au nombre d’éléments dans le contrôle (consultez [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md)).

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau d’entiers qui reçoivent les valeurs d’index des éléments dans l’en-tête.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, et la mémoire tampon au niveau de *lParam* reçoit le numéro d’élément de chaque élément du contrôle header dans l’ordre dans lequel ils apparaissent de gauche à droite. Dans le cas contraire, le message retourne la valeur zéro.

## <a name="remarks"></a>Remarques

Le nombre d’éléments dans *lParam* est spécifié dans *wParam* et doit être égal au nombre d’éléments dans le contrôle. Par exemple, le fragment de code suivant réserve une quantité de mémoire suffisante pour contenir les valeurs d’index.


```
int iItems,

    *lpiArray;



// Get memory for buffer.

(iItems = SendMessage(hwndHD, HDM_GETITEMCOUNT, 0,0))!=-1)

    if(!(lpiArray = calloc(iItems,sizeof(int))))

MessageBox(hwnd, "Out of memory.","Error", MB_OK);
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





