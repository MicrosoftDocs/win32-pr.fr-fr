---
title: Message EM_SETAUTOCORRECTPROC (RichEdit. h)
description: Définit la procédure de rappel de correction automatique actuelle.
ms.assetid: 2FA48CFC-0D7C-41EF-8207-5EDC644FF3BC
keywords:
- EM_SETAUTOCORRECTPROC les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7359c86c3fdabe4c410f600d0af3100dde4c4ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006424"
---
# <a name="em_setautocorrectproc-message"></a>\_Message SETAUTOCORRECTPROC em

Définit la procédure de rappel de correction automatique actuelle.


```C++
#define EM_SETAUTOCORRECTPROC       (WM_USER + 234)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Fonction de rappel [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) .

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si l’opération a échoué, la valeur de retour est zéro. Si l’opération échoue, la valeur de retour est une valeur différente de zéro.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[**\_CALLAUTOCORRECTPROC em**](em-callautocorrectproc.md)
</dt> <dt>

[**\_GETAUTOCORRECTPROC em**](em-getautocorrectproc.md)
</dt> </dl>

 

 





