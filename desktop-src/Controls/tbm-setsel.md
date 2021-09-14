---
title: Message TBM_SETSEL (commctrl. h)
description: Définit les positions de début et de fin de la plage de sélection disponible dans un TrackBar.
ms.assetid: 71f5b9f8-4850-44a8-8acf-adca9bda84c3
keywords:
- TBM_SETSEL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TBM_SETSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2edebc6b6dcf3b0b93e3047a39aac74c34d121bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116378"
---
# <a name="tbm_setsel-message"></a>\_Message TBM SETSEL

Définit les positions de début et de fin de la plage de sélection disponible dans un TrackBar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indicateur de redessin. Si ce paramètre a la **valeur true**, le message redessine le TrackBar une fois la plage de sélection définie. Si ce paramètre a la **valeur false**, le message définit la plage de sélection, mais ne redessine pas le TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>

Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la position logique de départ pour la plage de sélection, tandis que le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la position logique de fin.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Ce message est ignoré si le TrackBar n’a pas le style [**tbs \_ ENABLESELRANGE**](trackbar-control-styles.md) .

**TBM \_ SETSEL** vous permet de limiter le pointeur à une partie de la plage disponible pour la barre de progression.

## <a name="requirements"></a>Spécifications



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

[**TBM \_ SETSELEND**](tbm-setselend.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

