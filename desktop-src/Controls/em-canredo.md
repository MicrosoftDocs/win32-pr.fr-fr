---
title: Message EM_CANREDO (RichEdit. h)
description: Détermine s’il existe des actions dans la file d’attente de restauration par progression des contrôles.
ms.assetid: 4a76adc8-f815-4cf7-8742-b7695e5a0f64
keywords:
- EM_CANREDO les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_CANREDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d8898ba469d52e4098c2430dff5234a3522a6fbd3569bec823ff776a3f1c420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916049"
---
# <a name="em_canredo-message"></a>Message de la \_ CANREDO em

Détermine s’il existe des actions dans la file d’attente de restauration par progression des contrôles.

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

S’il y a des actions dans la file d’attente de rétablissement des contrôles, la valeur de retour est une valeur différente de zéro.

Si la file d’attente de restauration par progression est vide, la valeur de retour est zéro.

## <a name="remarks"></a>Remarques

Pour rétablir l’opération d’annulation la plus récente, envoyez le message [**em \_ Redo**](em-redo.md) .

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

[**\_GETREDONAME em**](em-getredoname.md)
</dt> <dt>

[**\_GETUNDONAME em**](em-getundoname.md)
</dt> <dt>

[**\_rétablissement em**](em-redo.md)
</dt> <dt>

[**\_Effacer em**](em-undo.md)
</dt> </dl>

 

 





