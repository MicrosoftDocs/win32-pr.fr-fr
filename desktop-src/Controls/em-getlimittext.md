---
title: Message EM_GETLIMITTEXT (winuser. h)
description: Obtient la limite de texte actuelle pour un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 778967f0-c090-46a2-9f27-194b17bbb1be
keywords:
- EM_GETLIMITTEXT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2066bf03fd8ea05851a9cef58f4e308db49f82bdee94c2d503cadf1c20a2c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831680"
---
# <a name="em_getlimittext-message"></a>\_Message GETLIMITTEXT em

Obtient la limite de texte actuelle pour un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

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

La valeur de retour est la limite de texte.

## <a name="remarks"></a>Remarques

**Contrôles d’édition, édition complète 2,0 et versions ultérieures :** La limite de texte correspond à la quantité maximale de texte, dans **TCHAR** s, que le contrôle peut contenir. Pour le texte ANSI, il s’agit du nombre d’octets ; pour le texte Unicode, il s’agit du nombre de caractères. Deux documents avec la même limite de caractères produisent la même limite de texte, même si l’un est ANSI et l’autre Unicode.

**Édition enrichie 1,0 :** La limite de texte correspond à la quantité maximale de texte, en octets, que le contrôle Rich Edit peut contenir.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETLIMITTEXT em**](em-setlimittext.md)
</dt> </dl>

 

 





