---
title: Message LB_GETCOUNT (winuser. h)
description: Obtient le nombre d’éléments dans une zone de liste.
ms.assetid: 1fbe44fc-8b9d-4bfa-a8bb-06817eecf064
keywords:
- LB_GETCOUNT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4f4792bf290343e2868b754f8efb1bfc03d0be1f600c9f7584f051053400b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435478"
---
# <a name="lb_getcount-message"></a>\_Message lb GETCOUNT

Obtient le nombre d’éléments dans une zone de liste.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est le nombre d’éléments dans la zone de liste, ou LB \_ Err si une erreur se produit.

## <a name="remarks"></a>Remarques

Le nombre retourné est supérieur à la valeur d’index du dernier élément (l’index est de base zéro).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETCOUNT lb**](lb-setcount.md)
</dt> </dl>

 

 





