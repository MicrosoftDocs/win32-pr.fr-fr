---
title: Code de notification EN_CLIPFORMAT (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit qu’un collage a été effectué avec un format de presse-papiers particulier. Un contrôle RichEdit sans fenêtre envoie cette notification à l’aide de la méthode ITextHost TxNotify.
ms.assetid: 79FE1350-4D45-447B-B705-63E966AC7F0E
keywords:
- EN_CLIPFORMAT les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- EN_CLIPFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4ad87f1c05ac9f5461da8a4ee1d26295be0ae1baafd8991801efc0d90197a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437039"
---
# <a name="en_clipformat-notification-code"></a>\_Code de notification en CLIPFORMAT

Avertit une fenêtre parente d’un contrôle RichEdit qu’un collage a été effectué avec un format de presse-papiers particulier. Un contrôle RichEdit sans fenêtre envoie cette notification à l’aide de la méthode [**ITextHost :: TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) .


```C++
EN_CLIPFORMAT

      pClipboardFmt = (CLIPBOARDFORMAT *) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

ID de fenêtre récupéré en appelant la fonction [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) avec la \_ valeur d’ID GWL.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) qui contient des informations sur le format du presse-papiers.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="remarks"></a>Remarques

Pour recevoir les \_ codes de notification en CLIPFORMAT, spécifiez [**ENM \_ CLIPFORMAT**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
</dt> </dl>

 

