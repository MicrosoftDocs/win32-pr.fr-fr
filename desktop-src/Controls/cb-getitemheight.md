---
title: Message CB_GETITEMHEIGHT (winuser. h)
description: Détermine la hauteur des éléments de liste ou le champ de sélection dans une zone de liste déroulante.
ms.assetid: 72fba6ca-0a51-4801-bd45-5f5a7d5ebee2
keywords:
- CB_GETITEMHEIGHT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6e3ad9636c32e40bfa95f1f3b2c209eab42023205e0a967cc91804ec314a103
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089189"
---
# <a name="cb_getitemheight-message"></a>\_Message GETITEMHEIGHT CB

Détermine la hauteur des éléments de liste ou le champ de sélection dans une zone de liste déroulante.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Composant de zone de liste déroulante dont la hauteur doit être récupérée. Ce paramètre doit avoir la valeur-1 pour récupérer la hauteur du champ de sélection. Elle doit être égale à zéro pour récupérer la hauteur des éléments de liste, sauf si la zone de liste déroulante a le style [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) . Dans ce cas, le paramètre *wParam* est l’index de base zéro d’un élément de liste spécifique.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour correspond à la hauteur, en pixels, des éléments de liste dans une zone de liste déroulante. Si la zone de liste déroulante a le style [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) , il s’agit de la hauteur de l’élément spécifié par le paramètre *wParam* . Si *wParam* a la valeur-1, la valeur de retour est la hauteur de la partie de contrôle d’édition (ou de texte statique) de la zone de liste déroulante. Si une erreur se produit, la valeur de retour est CB \_ Err.

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

[**\_SETITEMHEIGHT CB**](cb-setitemheight.md)
</dt> <dt>

[**\_MEASUREITEM WM**](wm-measureitem.md)
</dt> </dl>

 

 





