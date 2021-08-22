---
title: Message EM_GETTEXTLENGTHEX (RichEdit. h)
description: Calcule la longueur du texte de différentes façons. Elle est généralement appelée avant la création d’une mémoire tampon pour recevoir le texte du contrôle.
ms.assetid: 42c89b7b-e48d-4517-9993-ce58ff9e4e40
keywords:
- EM_GETTEXTLENGTHEX les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETTEXTLENGTHEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba6cf0a094edc2288dbeae6f735e8c10fb72f943f99f9a41b15fc1ef3136168d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540938"
---
# <a name="em_gettextlengthex-message"></a>\_Message GETTEXTLENGTHEX em

Calcule la longueur du texte de différentes façons. Elle est généralement appelée avant la création d’une mémoire tampon pour recevoir le texte du contrôle.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Pointeur vers une structure [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) qui reçoit les informations de longueur de texte.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Le message retourne le nombre de **TCHAR** s dans le contrôle d’édition, en fonction du paramètre des indicateurs dans la structure [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) . Si des indicateurs incompatibles ont été définis dans le membre **Flags** , le message retourne E \_ INVALIDARG.

## <a name="remarks"></a>Remarques

Ce message est un moyen rapide et facile de déterminer le nombre de caractères dans la version Unicode du contrôle Rich Edit. Toutefois, pour une page de codes cible non Unicode, vous allez potentiellement convertir en une combinaison de caractères codés sur un octet et sur deux octets.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
</dt> </dl>

 

 





