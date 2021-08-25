---
title: Message EM_UNDO (winuser. h)
description: Ce message annule la dernière opération de contrôle d’édition dans la file d’attente d’annulation du contrôle. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: c4bff128-0383-40c5-8f29-7738f7f26871
keywords:
- EM_UNDO les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 452d82e6d0685314a79f1f95cff487ee3f52e2d1b70925c3e6e72f9263f442e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047919"
---
# <a name="em_undo-message"></a>\_Message d’annulation em

Ce message annule la dernière opération de contrôle d’édition dans la file d’attente d’annulation du contrôle. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

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

Dans le cas d’un contrôle d’édition sur une seule ligne, la valeur de retour est toujours **true**.

Pour un contrôle d’édition multiligne, la valeur de retour est **true** si l’opération d’annulation réussit, ou **false** si l’opération d’annulation échoue.

## <a name="remarks"></a>Remarques

**Edit Controls et Rich edit 1,0 :** Une opération d’annulation peut également être annulée. Par exemple, vous pouvez restaurer le texte supprimé avec le premier message d' **\_ annulation d’em** , puis supprimer le texte avec un deuxième message d' **\_ annulation em** tant qu’il n’y a pas d’opération de modification intermédiaire.

**Édition enrichie 2,0 et versions ultérieures :** La fonctionnalité d’annulation est multiniveau et l’envoi de deux messages d' **\_ annulation em** annule les deux dernières opérations dans la file d’attente d’annulation. Pour rétablir une opération, envoyez le message de [**\_ rétablissement em**](em-redo.md) .

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**EM \_ CANUNDO**](em-canundo.md)
</dt> </dl>

 

 





