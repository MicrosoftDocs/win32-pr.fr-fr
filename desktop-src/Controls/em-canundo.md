---
title: Message EM_CANUNDO (winuser. h)
description: Détermine s’il existe des actions dans la file d’attente d’annulation d’un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: ae7ff372-b1f8-4ab7-9a7e-450aed3e0bc5
keywords:
- EM_CANUNDO les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_CANUNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345367b25790051a444363bb9bbc02af3d6fb0fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104503"
---
# <a name="em_canundo-message"></a>\_Message em CANUNDO

Détermine s’il existe des actions dans la file d’attente d’annulation d’un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

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

S’il y a des actions dans la file d’attente d’annulation du contrôle, la valeur de retour est différente de zéro.

Si la file d’attente d’annulation est vide, la valeur de retour est zéro.

## <a name="remarks"></a>Notes

Si la file d’attente d’annulation n’est pas vide, vous pouvez envoyer le message d' [**\_ annulation em**](em-undo.md) au contrôle pour annuler l’opération la plus récente.

**Edit Controls et Rich edit 1,0 :** La file d’attente d’annulation contient uniquement l’opération la plus récente.

**Édition enrichie 2,0 et versions ultérieures :** La file d’attente d’annulation peut contenir plusieurs opérations.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Effacer em**](em-undo.md)
</dt> </dl>

 

 





