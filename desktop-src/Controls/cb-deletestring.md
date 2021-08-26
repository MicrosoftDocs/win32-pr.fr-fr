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
ms.openlocfilehash: b0bed1d654b86ffeb4a02c780678822e1999847ef0e163e35ecba081af099f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063579"
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

## <a name="return-value"></a>Valeur retournée

La valeur de retour est le nombre de chaînes restantes dans la liste. Si le paramètre *wParam* spécifie un index supérieur au nombre d’éléments dans la liste, la valeur de retour est CB \_ Err.

## <a name="remarks"></a>Remarques

Si vous créez la zone de liste déroulante avec un style owner-drawn mais sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , le système envoie un message [**WM \_ DELETEITEM**](wm-deleteitem.md) au propriétaire de la zone de liste déroulante afin que l’application puisse libérer toutes les données supplémentaires associées à l’élément.

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

[**\_RESETCONTENT CB**](cb-resetcontent.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





