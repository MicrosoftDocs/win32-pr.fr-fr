---
title: Message CB_GETHORIZONTALEXTENT (winuser. h)
description: Obtient la largeur, en pixels, que peut faire défiler la zone de liste horizontalement (largeur avec défilement). Cela s’applique uniquement si la zone de liste comporte une barre de défilement horizontale.
ms.assetid: 7c9fff88-2750-4c94-b7f6-6bdd81c224e9
keywords:
- CB_GETHORIZONTALEXTENT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 928561b812dd3a09909d8d89c7dda1dc67b63f9177769d80db2d16ac78cbbf72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089209"
---
# <a name="cb_gethorizontalextent-message"></a>\_Message GETHORIZONTALEXTENT CB

Obtient la largeur, en pixels, que peut faire défiler la zone de liste horizontalement (largeur avec défilement). Cela s’applique uniquement si la zone de liste comporte une barre de défilement horizontale.

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

La valeur de retour est la largeur de défilement, en pixels.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETHORIZONTALEXTENT CB**](cb-sethorizontalextent.md)
</dt> </dl>

 

 





