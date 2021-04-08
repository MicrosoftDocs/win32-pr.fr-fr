---
title: Message EM_CANREDO (RichEdit. h)
description: Détermine s’il existe des actions dans la file d’attente de restauration par progression des contrôles.
ms.assetid: 4a76adc8-f815-4cf7-8742-b7695e5a0f64
keywords:
- EM_CANREDO les contrôles de message Windows
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
ms.openlocfilehash: ccfb12f8e72bdf5321151cd3a70b74f322a46591
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843897"
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

## <a name="remarks"></a>Notes

Pour rétablir l’opération d’annulation la plus récente, envoyez le message [**em \_ Redo**](em-redo.md) .

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

[**\_GETUNDONAME em**](em-getundoname.md)
</dt> <dt>

[**\_rétablissement em**](em-redo.md)
</dt> <dt>

[**\_Effacer em**](em-undo.md)
</dt> </dl>

 

 





