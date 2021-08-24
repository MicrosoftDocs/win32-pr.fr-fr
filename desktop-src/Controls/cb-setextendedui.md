---
title: Message CB_SETEXTENDEDUI (winuser. h)
description: Une application envoie un \_ message CB SETEXTENDEDUI pour sélectionner l’interface utilisateur par défaut ou l’interface utilisateur étendue pour une zone de liste déroulante avec le \_ style déroulant CBS ou le \_ style DropDownList SCC.
ms.assetid: c489e484-777e-4afa-996b-1ec3eb6552ab
keywords:
- CB_SETEXTENDEDUI les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_SETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b77e67e555628475b9e40e78b7b0391d0b631fd77e6ff7f549700a553fa507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118414221"
---
# <a name="cb_setextendedui-message"></a>\_Message SETEXTENDEDUI CB

Une application envoie un message **CB \_ SETEXTENDEDUI** pour sélectionner l’interface utilisateur par défaut ou l’interface utilisateur étendue pour une zone de liste déroulante avec le style [**\_ déroulant CBS**](combo-box-styles.md) ou le style [**\_ DropDownList SCC**](combo-box-styles.md) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur **booléenne** qui spécifie si la zone de liste déroulante utilise l’interface utilisateur étendue (**true**) ou l’interface utilisateur par défaut (**false**).

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération a échoué, la valeur de retour est CB \_ OK. Si une erreur se produit, il s’agit de CB \_ Err.

## <a name="remarks"></a>Remarques

Par défaut, la touche F4 ouvre ou ferme la liste et la flèche vers le bas modifie la sélection actuelle. Dans l’interface utilisateur étendue, la touche F4 est désactivée et la touche de direction bas ouvre la liste déroulante. La roulette de la souris, qui fait normalement défiler les éléments de la liste, n’a aucun effet lorsque l’interface utilisateur étendue est définie.

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

[**\_GETEXTENDEDUI CB**](cb-getextendedui.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Fonctionnalités de zone de liste modifiable](combo-box-features.md)
</dt> </dl>

 

 





