---
title: Message EM_GETHYPHENATEINFO (RichEdit. h)
description: Récupère des informations sur la césure pour un contrôle Rich Edit Microsoft.
ms.assetid: 70ccb698-e440-493b-8f38-2bf7f32e4b26
keywords:
- EM_GETHYPHENATEINFO les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETHYPHENATEINFO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd9bbb6eb156bd2a5af1b69ecaad800f721aebb68b3d8ccfcb7bf8cb9ba465e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019617"
---
# <a name="em_gethyphenateinfo-message"></a>\_Message GETHYPHENATEINFO em

Récupère des informations sur la césure pour un contrôle Rich Edit Microsoft.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Structure [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) .

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP1 uniquement\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETHYPHENATEINFO em**](em-sethyphenateinfo.md)
</dt> </dl>

 

 





