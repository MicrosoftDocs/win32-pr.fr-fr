---
title: Message EM_GETMARGINS (winuser. h)
description: Obtient les largeurs des marges gauche et droite d’un contrôle d’édition.
ms.assetid: 2482354b-aae0-4abd-8287-65c423f30abb
keywords:
- EM_GETMARGINS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33746bc44a7b1b0aadd11c573675fedd51e565a557da7601ebe35a4442ddc96c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541069"
---
# <a name="em_getmargins-message"></a>\_Message GETMARGINS em

Obtient les largeurs des marges gauche et droite d’un contrôle d’édition.

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

Retourne la largeur de la marge de gauche dans le LOWORD et la largeur de la marge droite dans le HIWORD.

## <a name="remarks"></a>Remarques

**Modification riche :** Le **message \_ GETMARGINS em** n’est pas pris en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_setMargins em**](em-setmargins.md)
</dt> </dl>

 

 





