---
title: Message BM_SETSTATE (winuser. h)
description: Définit l’état de surbrillance d’un bouton. L’état de mise en surbrillance indique si le bouton est mis en surbrillance comme si l’utilisateur l’avait poussé. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ macro SetState.
ms.assetid: 675ebe8d-b381-46ca-b328-ebe9f25d864a
keywords:
- BM_SETSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- BM_SETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9b60231980f406b0aeb499d724dc6aa7025513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511748"
---
# <a name="bm_setstate-message"></a>\_Message SETSTATE BM

Définit l’état de surbrillance d’un bouton. L’état de mise en surbrillance indique si le bouton est mis en surbrillance comme si l’utilisateur l’avait poussé. Vous pouvez envoyer ce message de manière explicite ou utiliser le [**bouton macro \_ SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur **booléenne** qui spécifie si le bouton est mis en surbrillance. La valeur **true** met en surbrillance le bouton. La valeur **false** supprime toute mise en surbrillance.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message retourne toujours la valeur zéro.

## <a name="remarks"></a>Notes

La mise en surbrillance affecte uniquement l’apparence d’un bouton. Elle n’a aucun effet sur l’état d’activation d’une case d’option ou d’une case à cocher.

Un bouton est automatiquement mis en surbrillance lorsque l’utilisateur positionne le curseur sur celui-ci et appuie sur le bouton gauche de la souris et le maintient enfoncé. La mise en surbrillance est supprimée lorsque l’utilisateur relâche le bouton de la souris.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETSTATE BM**](bm-getstate.md)
</dt> <dt>

[**\_SETCHECK BM**](bm-setcheck.md)
</dt> </dl>

 

 





