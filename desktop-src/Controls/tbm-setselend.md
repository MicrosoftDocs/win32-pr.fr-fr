---
title: Message TBM_SETSELEND (commctrl. h)
description: Définit la position logique de fin de la plage de sélection actuelle dans un TrackBar. Ce message est ignoré si le TrackBar n’a pas le \_ style tbs ENABLESELRANGE.
ms.assetid: 1feec14c-1607-49d5-a147-af2443f82dc1
keywords:
- TBM_SETSELEND les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TBM_SETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9ee524bf6a519a7d0071e4149ed03191a9aec989e2deefe596cca1072dbd098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167064"
---
# <a name="tbm_setselend-message"></a>\_Message TBM SETSELEND

Définit la position logique de fin de la plage de sélection actuelle dans un TrackBar. Ce message est ignoré si le TrackBar n’a pas le style [**tbs \_ ENABLESELRANGE**](trackbar-control-styles.md) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indicateur de redessin. Si ce paramètre a la **valeur true**, le message redessine le TrackBar une fois la plage de sélection définie. Si ce paramètre a la **valeur false**, le message définit la plage de sélection, mais ne redessine pas le TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>

Position logique de fin de la plage de sélection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**TBM \_ GETSELEND**](tbm-getselend.md)
</dt> <dt>

[**TBM \_ GETSELSTART**](tbm-getselstart.md)
</dt> <dt>

[**TBM \_ SETSEL**](tbm-setsel.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

 





