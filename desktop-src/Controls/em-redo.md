---
title: Message EM_REDO (RichEdit. h)
description: Envoie un \_ message de rétablissement em à un contrôle RichEdit pour rétablir l’action suivante dans la file d’attente de restauration par progression du contrôle.
ms.assetid: 28ec1ec2-a56d-442f-b3cb-9feeb92edaeb
keywords:
- EM_REDO les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_REDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d39b679e8bf7e78cf7ce028d0bb440438770d0d0123516313fb418b2136ebc11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437859"
---
# <a name="em_redo-message"></a>\_Message de rétablissement em

Envoie un message de **\_ rétablissement em** à un contrôle RichEdit pour rétablir l’action suivante dans la file d’attente de restauration par progression du contrôle.

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

Si l’opération de **rétablissement** échoue, la valeur de retour est une valeur différente de zéro.

Si l’opération de **rétablissement** échoue, la valeur de retour est zéro.

## <a name="remarks"></a>Remarques

Pour déterminer s’il existe des actions dans la file d’attente de restauration par progression du contrôle, envoyez le message de la valeur [**em \_**](em-canredo.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**EM- \_ CANREDO**](em-canredo.md)
</dt> <dt>

[**\_GETREDONAME em**](em-getredoname.md)
</dt> <dt>

[**\_GETUNDONAME em**](em-getundoname.md)
</dt> <dt>

[**\_Effacer em**](em-undo.md)
</dt> </dl>

 

 





