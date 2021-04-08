---
title: Message EM_GETTEXTLENGTHEX (RichEdit. h)
description: Calcule la longueur du texte de différentes façons. Elle est généralement appelée avant la création d’une mémoire tampon pour recevoir le texte du contrôle.
ms.assetid: 42c89b7b-e48d-4517-9993-ce58ff9e4e40
keywords:
- EM_GETTEXTLENGTHEX les contrôles de message Windows
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
ms.openlocfilehash: de2d91674e07ef60c2ce95535983a31cf380f9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843481"
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

## <a name="remarks"></a>Notes

Ce message est un moyen rapide et facile de déterminer le nombre de caractères dans la version Unicode du contrôle Rich Edit. Toutefois, pour une page de codes cible non Unicode, vous allez potentiellement convertir en une combinaison de caractères codés sur un octet et sur deux octets.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
</dt> </dl>

 

 





