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
ms.openlocfilehash: 5551aace3ab054c1c6fa322242ae06386ff19f5a44775bd6dcc6887d19c65c62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437559"
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

## <a name="remarks"></a>Remarques

> [!Note]  
> Pour activer la césure, le client doit appeler [**em \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md), en spécifiant à \_ ADVANCEDTYPOGRAPHY.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP1 uniquement\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETHYPHENATEINFO em**](em-gethyphenateinfo.md)
</dt> </dl>

 

 





