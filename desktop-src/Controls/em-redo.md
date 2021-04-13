---
title: Message EM_REDO (RichEdit. h)
description: Envoie un \_ message de rétablissement em à un contrôle RichEdit pour rétablir l’action suivante dans la file d’attente de restauration par progression du contrôle.
ms.assetid: 28ec1ec2-a56d-442f-b3cb-9feeb92edaeb
keywords:
- EM_REDO les contrôles de message Windows
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
ms.openlocfilehash: bba7a684db0d40ebcfeec4a540989c4dab4c5dd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465898"
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

## <a name="remarks"></a>Notes

Pour déterminer s’il existe des actions dans la file d’attente de restauration par progression du contrôle, envoyez le message de la valeur [**em \_**](em-canredo.md) .

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

[**EM- \_ CANREDO**](em-canredo.md)
</dt> <dt>

[**\_GETREDONAME em**](em-getredoname.md)
</dt> <dt>

[**\_GETUNDONAME em**](em-getundoname.md)
</dt> <dt>

[**\_Effacer em**](em-undo.md)
</dt> </dl>

 

 





