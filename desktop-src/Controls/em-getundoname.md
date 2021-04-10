---
title: Message EM_GETUNDONAME (RichEdit. h)
description: Microsoft Rich Edit 2,0 et ultérieur récupère le type de la prochaine action d’annulation, le cas échéant. Édition enrichie de Microsoft 1,0 ce message n’est pas pris en charge.
ms.assetid: 43351909-f8bc-425a-9d9b-655e3b47eb75
keywords:
- EM_GETUNDONAME les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETUNDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c29b5815da5569059ba80c007d6af39d1e389f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942560"
---
# <a name="em_getundoname-message"></a>\_Message GETUNDONAME em

Rich Edit 2,0 et versions ultérieures de Microsoft : récupère le type de la prochaine action d’annulation, le cas échéant.

Édition enrichie de Microsoft 1,0 : ce message n’est pas pris en charge.

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

S’il existe une action d’annulation, la valeur retournée est une valeur d’énumération [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) qui indique le type de l’action suivante dans la file d’attente d’annulation du contrôle.

Si aucune action ne peut être annulée ou si le type de l’action d’annulation suivante est inconnu, la valeur de retour est zéro.

## <a name="remarks"></a>Notes

Les types d’actions qui peuvent être annulés ou réexécutés incluent les opérations de frappe, de suppression, de glisser-déplacer, de couper et de coller. Ces informations peuvent être utiles pour les applications qui fournissent une interface utilisateur étendue pour les opérations d’annulation et de rétablissement, telles qu’une zone de liste déroulante d’actions qui peuvent être annulées.

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

[**\_GETREDONAME em**](em-getredoname.md)
</dt> <dt>

[**\_rétablissement em**](em-redo.md)
</dt> <dt>

[**\_Effacer em**](em-undo.md)
</dt> <dt>

[**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





