---
title: Message CB_DELETESTRING (winuser. h)
description: Supprime une chaîne dans la zone de liste d’une zone de liste déroulante.
ms.assetid: 8d526796-04ef-4c01-94d6-fb50e6fef27b
keywords:
- CB_DELETESTRING les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0d3900c86874db1113c219fd9f7967c5f6bb6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123921"
---
# <a name="cb_deletestring-message"></a>\_Message DELETESTRING CB

Supprime une chaîne dans la zone de liste d’une zone de liste déroulante.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la chaîne à supprimer.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est le nombre de chaînes restantes dans la liste. Si le paramètre *wParam* spécifie un index supérieur au nombre d’éléments dans la liste, la valeur de retour est CB \_ Err.

## <a name="remarks"></a>Notes

Si vous créez la zone de liste déroulante avec un style owner-drawn mais sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , le système envoie un message [**WM \_ DELETEITEM**](wm-deleteitem.md) au propriétaire de la zone de liste déroulante afin que l’application puisse libérer toutes les données supplémentaires associées à l’élément.

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

[**\_RESETCONTENT CB**](cb-resetcontent.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





