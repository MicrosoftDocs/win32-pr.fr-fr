---
title: Message EM_GETAUTOCORRECTPROC (RichEdit. h)
description: Obtient un pointeur vers la fonction AutoCorrectProc définie par l’application.
ms.assetid: 90821036-F27D-4AC3-9AB8-40A94486B938
keywords:
- EM_GETAUTOCORRECTPROC les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4d730d15ca8631e6d663e3d4f971f115d5c268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465574"
---
# <a name="em_getautocorrectproc-message"></a>\_Message GETAUTOCORRECTPROC em

Obtient un pointeur vers la fonction [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) définie par l’application.

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

Retourne un pointeur vers la fonction [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) définie par l’application.

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

[**\_CALLAUTOCORRECTPROC em**](em-callautocorrectproc.md)
</dt> <dt>

[**\_SETAUTOCORRECTPROC em**](em-setautocorrectproc.md)
</dt> </dl>

 

 





