---
title: Code de notification EN_DRAGDROPDONE (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit que l’opération de glisser-déplacer est terminée. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 3c8b95cc-86ef-4aec-b551-11dca50ea5c5
keywords:
- EN_DRAGDROPDONE les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- EN_DRAGDROPDONE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb498361de04184823ab0d0652cc32adc9cbb1978bd6f303b7b215417f99f552
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436869"
---
# <a name="en_dragdropdone-notification-code"></a>\_Code de notification en DRAGDROPDONE

Avertit une fenêtre parente d’un contrôle RichEdit que l’opération de glisser-déplacer est terminée. Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
EN_DRAGDROPDONE

    pnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce code de notification ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Pour recevoir un \_ Code de notification en DRAGDROPDONE, spécifiez l’indicateur [**ENM \_ DRAGDROPDONE**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .

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

[**EM \_ SETEVENTMASK**](em-seteventmask.md)
</dt> </dl>

 

 





