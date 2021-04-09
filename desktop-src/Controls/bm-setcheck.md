---
title: Message BM_SETCHECK (winuser. h)
description: Définit l’état d’activation d’une case d’option ou d’une case à cocher. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro Button SetCheck.
ms.assetid: 8294e6c4-caac-4c60-85ff-38698a1d2ae4
keywords:
- BM_SETCHECK les contrôles de message Windows
topic_type:
- apiref
api_name:
- BM_SETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c298fb865fe34946bfedc9f1d6d1924f6d32202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032440"
---
# <a name="bm_setcheck-message"></a>\_Message SETCHECK BM

Définit l’état d’activation d’une case d’option ou d’une case à cocher. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**Button \_ SetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

État d’activation. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                     | Signification                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BST_CHECKED"></span><span id="bst_checked"></span><dl> <dt>**BST \_ vérifié**</dt> </dl>                   | Définit l’état du bouton sur activé.<br/>                                                                                                                                                                                           |
| <span id="BST_INDETERMINATE"></span><span id="bst_indeterminate"></span><dl> <dt>**BST \_ indéterminé**</dt> </dl> | Définit l’état du bouton sur grisé, ce qui indique un état indéterminé. Utilisez cette valeur uniquement si le bouton a le style [**BS \_ 3STATE**](button-styles.md) ou [**BS \_ AUTO3STATE**](button-styles.md) .<br/> |
| <span id="BST_UNCHECKED"></span><span id="bst_unchecked"></span><dl> <dt>**BST \_ désactivé**</dt> </dl>             | Définit l’état du bouton sur effacé.<br/>                                                                                                                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message retourne toujours la valeur zéro.

## <a name="remarks"></a>Notes

Le **message \_ SETCHECK BM** n’a aucun effet sur les boutons de commande.

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

[**\_GETCHECK BM**](bm-getcheck.md)
</dt> <dt>

[**\_GETSTATE BM**](bm-getstate.md)
</dt> <dt>

[**BM \_ SETSTATE**](bm-setstate.md)
</dt> </dl>

 

 





