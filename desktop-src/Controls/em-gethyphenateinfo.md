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
ms.openlocfilehash: 5d083b4bbc4b6854f767395d51dd9899c2a185d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117893"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP1 uniquement\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETHYPHENATEINFO em**](em-sethyphenateinfo.md)
</dt> </dl>

 

 





