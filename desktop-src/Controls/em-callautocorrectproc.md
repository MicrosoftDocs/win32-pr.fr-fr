---
title: Message EM_CALLAUTOCORRECTPROC (RichEdit. h)
description: Appelle la fonction de rappel de correction automatique stockée par le \_ message em SETAUTOCORRECTPROC, à condition que le texte qui précède le point d’insertion soit candidat à la correction automatique.
ms.assetid: 93116467-B345-4FD9-9162-3E01CF3C6F20
keywords:
- EM_CALLAUTOCORRECTPROC les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_CALLAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73109d2499fc01a1d811066dc6059593c7ed5e0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195699"
---
# <a name="em_callautocorrectproc-message"></a>\_Message CALLAUTOCORRECTPROC em

Appelle la fonction de rappel de correction automatique stockée par le message [**em \_ SETAUTOCORRECTPROC**](em-setautocorrectproc.md) , à condition que le texte qui précède le point d’insertion soit candidat à la correction automatique.


```C++
#define EM_CALLAUTOCORRECTPROC       (WM_USER + 255)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Caractère de type **WCHAR**. Si ce caractère est une tabulation (U + 0009) et que le caractère qui précède le point d’insertion n’est pas un onglet, alors le caractère qui précède le point d’insertion est traité dans le cadre de la chaîne du candidat à la correction automatique et non sous la forme d’un délimiteur de chaîne. Sinon, *wParam* n’a aucun effet.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est égale à zéro si le message a été correctement effectué, ou différent de zéro si une erreur se produit.

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

[**\_GETAUTOCORRECTPROC em**](em-getautocorrectproc.md)
</dt> <dt>

[**\_SETAUTOCORRECTPROC em**](em-setautocorrectproc.md)
</dt> </dl>

 

 





