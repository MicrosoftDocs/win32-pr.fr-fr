---
title: Message CB_GETEXTENDEDUI (winuser. h)
description: Détermine si une zone de liste déroulante possède l’interface utilisateur par défaut ou l’interface utilisateur étendue.
ms.assetid: 4f5580e0-68b1-4584-bf79-561fb8222fe0
keywords:
- CB_GETEXTENDEDUI les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_GETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d90550bf341fc8586174c7ec57eb77fad08c59
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006834"
---
# <a name="cb_getextendedui-message"></a>\_Message GETEXTENDEDUI CB

Détermine si une zone de liste déroulante possède l’interface utilisateur par défaut ou l’interface utilisateur étendue.

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

## <a name="return-value"></a>Valeur de retour

Si la zone de liste déroulante possède l’interface utilisateur étendue, la valeur de retour est **true**. Sinon, la **valeur est false**.

## <a name="remarks"></a>Notes

Par défaut, la touche F4 ouvre ou ferme la liste et la flèche vers le bas modifie la sélection actuelle. Dans une zone de liste déroulante avec l’interface utilisateur étendue, la touche F4 est désactivée et l’appui sur la touche bas ouvre la liste déroulante.

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

[**\_SETEXTENDEDUI CB**](cb-setextendedui.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Fonctionnalités de zone de liste modifiable](combo-box-features.md)
</dt> </dl>

 

 





