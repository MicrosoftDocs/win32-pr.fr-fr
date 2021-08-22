---
title: Code de notification EN_CORRECTTEXT (RichEdit. h)
description: Avertit une fenêtre parente du contrôle RichEdit qu’un \_ geste SyV correct s’est produit, donnant à la fenêtre parente la possibilité d’annuler la correction du texte. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: d6f6278f-ff63-4f6a-a352-2b4d70df3e1a
keywords:
- EN_CORRECTTEXT les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- EN_CORRECTTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48f03bf0d1bd31cc1f4139c24c6b0efa904f013231af4e108b0f97ef7f308bbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019417"
---
# <a name="en_correcttext-notification-code"></a>\_Code de notification en CORRECTTEXT

Avertit une fenêtre parente du contrôle RichEdit qu’un \_ geste SyV correct s’est produit, donnant à la fenêtre parente la possibilité d’annuler la correction du texte. Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
EN_CORRECTTEXT

    penCorrectText = (ENCORRECTTEXT *) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Structure [**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) spécifiant la sélection à corriger.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retournez zéro pour ignorer l’action.

Retourne une valeur différente de zéro pour traiter l’action.

## <a name="remarks"></a>Remarques

Ce code de notification est envoyé uniquement si les fonctionnalités du stylet sont disponibles.

Pour recevoir les \_ codes de notification en CORRECTTEXT, spécifiez [**ENM \_ CORRECTTEXT**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .

> [!Note]  
> Le \_ Code de notification en CORRECTTEXT est uniquement pris en charge dans la version Rich edit 1,0. Elle n’est pas prise en charge dans les versions ultérieures de la modification enrichie. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

 

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

[**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext)
</dt> </dl>

 

 





