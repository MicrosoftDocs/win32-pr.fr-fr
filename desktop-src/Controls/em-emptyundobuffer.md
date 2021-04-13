---
title: Message EM_EMPTYUNDOBUFFER (winuser. h)
description: Réinitialise l’indicateur d’annulation d’un contrôle d’édition. L’indicateur Undo est défini chaque fois qu’une opération dans le contrôle d’édition peut être annulée. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: a4ff7bd9-f8ae-4f18-8429-4ceaaeeb0f94
keywords:
- EM_EMPTYUNDOBUFFER les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_EMPTYUNDOBUFFER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abbdc067b603a032b8d311ddd7930a8ca6de01c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465899"
---
# <a name="em_emptyundobuffer-message"></a>\_Message EMPTYUNDOBUFFER em

Réinitialise l’indicateur d’annulation d’un contrôle d’édition. L’indicateur Undo est défini chaque fois qu’une opération dans le contrôle d’édition peut être annulée. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

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

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

L’indicateur d’annulation est automatiquement réinitialisé chaque fois que le contrôle d’édition reçoit un message [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) ou [**em \_ SETHANDLE**](em-sethandle.md) .

**Edit Controls et Rich edit 1,0 :** Le contrôle peut uniquement annuler ou rétablir l’opération la plus récente.

**Édition enrichie 2,0 et versions ultérieures :** Le message **em \_ EMPTYUNDOBUFFER** vide toutes les mémoires tampons d’annulation et de rétablissement. Les contrôles RichEdit permettent à l’utilisateur d’annuler ou de rétablir plusieurs opérations.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

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

[**EM \_ CANUNDO**](em-canundo.md)
</dt> <dt>

[**\_SETHANDLE em**](em-sethandle.md)
</dt> <dt>

[**\_Effacer em**](em-undo.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**WM, \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

