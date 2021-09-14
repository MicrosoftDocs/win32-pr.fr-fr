---
title: Message CB_SETITEMHEIGHT (winuser. h)
description: Une application envoie un \_ message CB SETITEMHEIGHT pour définir la hauteur des éléments de liste ou le champ de sélection dans une zone de liste déroulante.
ms.assetid: 25a01170-5ffc-4d86-b696-706f5375570b
keywords:
- CB_SETITEMHEIGHT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e46be007cdea17857e5d8ec42a12228821539d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120061"
---
# <a name="cb_setitemheight-message"></a>\_Message SETITEMHEIGHT CB

Une application envoie un message **CB \_ SETITEMHEIGHT** pour définir la hauteur des éléments de liste ou le champ de sélection dans une zone de liste déroulante.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie le composant de la zone de liste déroulante pour laquelle la hauteur doit être définie.

Ce paramètre doit avoir la valeur 1 pour définir la hauteur du champ de sélection. Elle doit être égale à zéro pour définir la hauteur des éléments de liste, sauf si la zone de liste déroulante a le style [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) . Dans ce cas, le paramètre *wParam* est l’index de base zéro d’un élément de liste spécifique.

</dd> <dt>

*lParam* 
</dt> <dd>

Spécifie la hauteur, en pixels, du composant de zone de liste déroulante identifié par *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si l’index ou la hauteur n’est pas valide, la valeur de retour est CB \_ Err.

## <a name="remarks"></a>Notes

La hauteur du champ de sélection dans une zone de liste déroulante est définie indépendamment de la hauteur des éléments de la liste. Une application doit s’assurer que la hauteur du champ de sélection n’est pas inférieure à la hauteur d’un élément de liste particulier.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETITEMHEIGHT CB**](cb-getitemheight.md)
</dt> <dt>

[**\_MEASUREITEM WM**](wm-measureitem.md)
</dt> </dl>

 

 





