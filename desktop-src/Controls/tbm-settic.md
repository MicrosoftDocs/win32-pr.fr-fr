---
title: Message TBM_SETTIC (commctrl. h)
description: Définit une graduation dans un TrackBar à la position logique spécifiée.
ms.assetid: 89b42cac-967e-40c7-9fab-2bd76f06f3f9
keywords:
- TBM_SETTIC les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TBM_SETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a42839157125c8def28a19dd9c2ccce21d3b96c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116366"
---
# <a name="tbm_settic-message"></a>\_Message TBM SETTIC

Définit une graduation dans un TrackBar à la position logique spécifiée.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Position de la graduation. Ce paramètre peut être n’importe laquelle des valeurs entières dans la plage de la plage de la barre de défilement minimale à la position maximale du curseur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** si la graduation est définie, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Un TrackBar crée ses propres première et dernière graduations. N’utilisez pas ce message pour définir les première et dernière graduations.

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

[**TBM \_ GETPTICS**](tbm-getptics.md)
</dt> <dt>

[**TBM \_ GETTIC**](tbm-gettic.md)
</dt> </dl>

 

 





