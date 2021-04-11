---
title: Message BM_GETCHECK (winuser. h)
description: Obtient l’état d’activation d’une case d’option ou d’une case à cocher. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ GetCheck macro.
ms.assetid: a25b2c8d-0b32-4807-bfb4-e277675924f1
keywords:
- BM_GETCHECK les contrôles de message Windows
topic_type:
- apiref
api_name:
- BM_GETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1aa89dc256ea9e0036259239d1c74e1e82b272
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105769"
---
# <a name="bm_getcheck-message"></a>\_Message GETCHECK BM

Obtient l’état d’activation d’une case d’option ou d’une case à cocher. Vous pouvez envoyer ce message de manière explicite ou utiliser le [**bouton \_ GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) macro.

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

La valeur renvoyée par un bouton créé à l’aide de la fonction [**BS \_ autocase**](button-styles.md), [**BS \_ RadioButton**](button-styles.md), [**BS \_ AUTO3STATE**](button-styles.md), [**BS \_ case**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)ou [**BS \_ 3STATE**](button-styles.md) style peut être l’une des suivantes.



| Code de retour                                                                                       | Description                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BST \_ vérifié**</dt> </dl>       | Le bouton est activé.<br/>                                                                                                                                                                                     |
| <dl> <dt>**BST \_ indéterminé**</dt> </dl> | Le bouton est grisé, ce qui indique un état indéterminé (s’applique uniquement si le bouton a le style [**BS \_ 3STATE**](button-styles.md) ou [**BS \_ AUTO3STATE**](button-styles.md) ).<br/> |
| <dl> <dt>**BST \_ désactivé**</dt> </dl>     | Le bouton est désactivé<br/>                                                                                                                                                                                      |



 

## <a name="remarks"></a>Notes

Si le style du bouton est différent de ceux indiqués dans la liste, la valeur de retour est zéro.

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

 

 





