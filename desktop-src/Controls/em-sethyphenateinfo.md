---
title: Message EM_SETHYPHENATEINFO (RichEdit. h)
description: Définit le mode de césure d’un contrôle RichEdit.
ms.assetid: 67126cb8-ab50-49a9-b32f-2245debf2fe3
keywords:
- EM_SETHYPHENATEINFO les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETHYPHENATEINFO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8369d463ae03e9410347ab58a50346625e3de47
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006390"
---
# <a name="em_sethyphenateinfo-message"></a>\_Message SETHYPHENATEINFO em

Définit le mode de césure d’un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Pointeur vers une structure [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) .

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé, doit être égal à zéro.

</dd> </dl>

## <a name="remarks"></a>Notes

> [!Note]  
> Pour activer la césure, le client doit appeler [**em \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md), en spécifiant à \_ ADVANCEDTYPOGRAPHY.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP1 uniquement\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETHYPHENATEINFO em**](em-gethyphenateinfo.md)
</dt> </dl>

 

 





