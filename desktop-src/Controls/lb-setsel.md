---
title: Message LB_SETSEL (winuser. h)
description: Sélectionne un élément dans une zone de liste à sélection multiple et, si nécessaire, fait défiler l’élément dans l’affichage.
ms.assetid: 643783f2-0e00-4b79-b957-47938bb9f8da
keywords:
- LB_SETSEL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd50f12c4190ba9ecafad11b167c1ac60adf691d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999844"
---
# <a name="lb_setsel-message"></a>\_Message SETSEL lb

Sélectionne un élément dans une zone de liste à sélection multiple et, si nécessaire, fait défiler l’élément dans l’affichage.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie comment définir la sélection. Si ce paramètre a la **valeur true**, l’élément est sélectionné et mis en surbrillance ; Si la **valeur est false**, la mise en surbrillance est supprimée et l’élément n’est plus sélectionné.

</dd> <dt>

*lParam* 
</dt> <dd>

Spécifie l’index de base zéro de l’élément à définir. Si ce paramètre a la valeur-1, la sélection est ajoutée ou supprimée de tous les éléments, en fonction de la valeur de *wParam*, et aucun défilement ne se produit.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si une erreur se produit, la valeur de retour est LB \_ Err.

## <a name="remarks"></a>Notes

Utilisez ce message uniquement avec les zones de liste à sélection multiple.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETSEL lb**](lb-getsel.md)
</dt> <dt>

[**\_SELITEMRANGE lb**](lb-selitemrange.md)
</dt> </dl>

 

 





