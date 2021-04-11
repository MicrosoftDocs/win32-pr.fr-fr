---
title: Message LB_SELITEMRANGEEX (winuser. h)
description: Sélectionne un ou plusieurs éléments consécutifs dans une zone de liste à sélection multiple.
ms.assetid: aac85d72-43e2-4ab0-b9ee-c7a87e21d7a1
keywords:
- LB_SELITEMRANGEEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_SELITEMRANGEEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa3ca1335372b7a61c4dfcbc379c36e89ff933e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942659"
---
# <a name="lb_selitemrangeex-message"></a>\_Message SELITEMRANGEEX lb

Sélectionne un ou plusieurs éléments consécutifs dans une zone de liste à sélection multiple.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie l’index de base zéro du premier élément à sélectionner.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits. Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments. Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Spécifie l’index de base zéro du dernier élément à sélectionner.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une erreur se produit, la valeur de retour est LB \_ Err.

## <a name="remarks"></a>Notes

Si le paramètre *wParam* est inférieur au paramètre *lParam* , la plage d’éléments spécifiée est sélectionnée. Si *wParam* est supérieur ou égal à *lParam*, la plage est supprimée de la plage d’éléments spécifiée. Pour sélectionner un seul élément, sélectionnez deux éléments, puis désélectionnez l’élément indésirable.

Utilisez ce message uniquement avec les zones de liste à sélection multiple.

Ce message peut sélectionner une plage uniquement dans les 65 536 premiers éléments.

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

[**\_SELITEMRANGE lb**](lb-selitemrange.md)
</dt> <dt>

[**\_SETSEL lb**](lb-setsel.md)
</dt> </dl>

 

 





