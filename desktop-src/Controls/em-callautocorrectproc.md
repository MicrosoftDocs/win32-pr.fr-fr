---
title: Message EM_CALLAUTOCORRECTPROC (RichEdit. h)
description: Appelle la fonction de rappel de correction automatique stockée par le \_ message em SETAUTOCORRECTPROC, à condition que le texte qui précède le point d’insertion soit candidat à la correction automatique.
ms.assetid: 93116467-B345-4FD9-9162-3E01CF3C6F20
keywords:
- EM_CALLAUTOCORRECTPROC les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465914"
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

## <a name="return-value"></a>Valeur retournée

La valeur de retour est égale à zéro si le message a été correctement effectué, ou différent de zéro si une erreur se produit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[**\_GETAUTOCORRECTPROC em**](em-getautocorrectproc.md)
</dt> <dt>

[**\_SETAUTOCORRECTPROC em**](em-setautocorrectproc.md)
</dt> </dl>

 

 





