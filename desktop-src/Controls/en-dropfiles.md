---
title: Code de notification EN_DROPFILES (RichEdit. h)
description: Avertit une fenêtre parente du contrôle RichEdit que l’utilisateur tente de déposer des fichiers dans le contrôle. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify lorsqu’il reçoit le \_ message WM DROPFILES.
ms.assetid: fcae0ff8-ce37-4c71-b14c-cbd6429b4ab3
keywords:
- Contrôles Windows de code de notification EN_DROPFILES
topic_type:
- apiref
api_name:
- EN_DROPFILES
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c0ed1a4a9b95348b1de20e54fcf3b167df19f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464426"
---
# <a name="en_dropfiles-notification-code"></a>\_Code de notification en DROPFILES

Avertit une fenêtre parente du contrôle RichEdit que l’utilisateur tente de déposer des fichiers dans le contrôle. Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) lorsqu’il reçoit le message [**WM \_ DROPFILES**](/windows/desktop/shell/wm-dropfiles) .


```C++
EN_DROPFILES

      penDropFiles = (ENDROPFILES *) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Structure [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) qui reçoit les informations sur les fichiers supprimés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro pour permettre l’opération de déplacement.

Retournez zéro pour ignorer l’opération de suppression.

## <a name="remarks"></a>Notes

Pour qu’un contrôle RichEdit reçoive les messages [**WM \_ DROPFILES**](/windows/desktop/shell/wm-dropfiles) , la fenêtre parente doit inscrire le contrôle en tant que cible de déplacement à l’aide de la fonction [**DragAcceptFiles**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) . Le contrôle ne s’inscrit pas lui-même.

Pour recevoir les \_ codes de notification en DROPFILES, spécifiez [**ENM \_ DROPFILES**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .

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

[**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles)
</dt> </dl>

 

