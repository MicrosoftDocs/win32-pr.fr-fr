---
title: Message EM_SETTEXTEX (RichEdit. h)
description: Combine les fonctionnalités des messages WM \_ SETTEXT et em \_ REPLACESEL et ajoute la possibilité de définir du texte à l’aide d’une page de codes et d’utiliser du texte enrichi ou du texte brut.
ms.assetid: 1ba9e4c0-7870-4057-8a8b-d0e6577349ac
keywords:
- EM_SETTEXTEX les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227e88fc489c274a5c1b194aa79b4b031ad5f0c07bab4110e5b28b3c7cffbf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048039"
---
# <a name="em_settextex-message"></a>\_Message SETTEXTEX em

Combine les fonctionnalités des messages [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) et [**em \_ REPLACESEL**](em-replacesel.md) et ajoute la possibilité de définir du texte à l’aide d’une page de codes et d’utiliser du texte enrichi ou du texte brut.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Pointeur vers une structure [**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex) qui spécifie des indicateurs et une page de codes facultative à utiliser lors de la conversion en Unicode.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers le texte se terminant par null à insérer. Ce texte est une chaîne ANSI, sauf si la page de codes est 1200 (Unicode). Si *lParam* commence par une séquence ASCII RTF valide, par exemple « { \\ RTF » ou « {urtf », le texte est lu à l’aide du lecteur RTF.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération définit tout le texte et s’effectue correctement, la valeur de retour est 1.

Si l’opération définit la sélection et s’effectue correctement, la valeur de retour est le nombre d’octets ou de caractères copiés.

Si l’opération échoue, la valeur de retour est zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | Édition enrichie 3,0<br/>                                                              |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETTEXTEX em**](em-gettextex.md)
</dt> <dt>

[**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex)
</dt> </dl>

 

