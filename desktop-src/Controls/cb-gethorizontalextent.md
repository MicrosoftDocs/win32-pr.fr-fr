---
title: Message CB_GETHORIZONTALEXTENT (winuser. h)
description: Obtient la largeur, en pixels, que peut faire défiler la zone de liste horizontalement (largeur avec défilement). Cela s’applique uniquement si la zone de liste comporte une barre de défilement horizontale.
ms.assetid: 7c9fff88-2750-4c94-b7f6-6bdd81c224e9
keywords:
- CB_GETHORIZONTALEXTENT les contrôles de message Windows
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
ms.openlocfilehash: 8a2b1fb7c8fe7549360801516364528c9a2ef1f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032855"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETHORIZONTALEXTENT CB**](cb-sethorizontalextent.md)
</dt> </dl>

 

 





