---
title: Message EM_GETREDONAME (RichEdit. h)
description: Récupère le type de l’action suivante, le cas échéant, dans la file d’attente de restauration par progression du contrôle RichEdit.
ms.assetid: 8649236f-32dc-45d3-847e-c9f65ffba44c
keywords:
- EM_GETREDONAME les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETREDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea44257344b9ebdb8ffe91ad97e939aae0db9b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942240"
---
# <a name="em_getredoname-message"></a>\_Message GETREDONAME em

Récupère le type de l’action suivante, le cas échéant, dans la file d’attente de restauration par progression du contrôle RichEdit.

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

Si la file d’attente de restauration par progression pour le contrôle n’est pas vide, la valeur retournée est une valeur d’énumération [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) qui indique le type de l’action suivante dans la file d’attente de restauration par progression du contrôle.

S’il n’y a pas d’actions rétablies ou si le type de l’action retablie suivante est inconnu, la valeur de retour est zéro.

## <a name="remarks"></a>Notes

Les types d’actions qui peuvent être annulés ou réexécutés incluent les opérations de frappe, de suppression, de glisser-déplacer, de couper et de coller. Ces informations peuvent être utiles pour les applications qui fournissent une interface utilisateur étendue pour les opérations d’annulation et de rétablissement, telles qu’une zone de liste déroulante d’actions rétablies.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETUNDONAME em**](em-getundoname.md)
</dt> <dt>

[**\_rétablissement em**](em-redo.md)
</dt> <dt>

[**\_Effacer em**](em-undo.md)
</dt> <dt>

[**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





