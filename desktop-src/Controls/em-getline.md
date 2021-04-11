---
title: Message EM_GETLINE (winuser. h)
description: Copie une ligne de texte à partir d’un contrôle d’édition et la place dans une mémoire tampon spécifiée. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- EM_GETLINE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e014eaccba65b4ea1fc96e26872954a9cfc06e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941745"
---
# <a name="em_getline-message-winuserh"></a>Message EM_GETLINE (winuser. h)

Copie une ligne de texte à partir d’un contrôle d’édition et la place dans une mémoire tampon spécifiée. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la ligne à récupérer à partir d’un contrôle d’édition multiligne. La valeur zéro spécifie la ligne la plus grande. Ce paramètre est ignoré par un contrôle d’édition sur une seule ligne.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la mémoire tampon qui reçoit une copie de la ligne. Avant d’envoyer le message, définissez le premier mot de cette mémoire tampon sur la taille, dans **TCHAR** s, de la mémoire tampon. Pour le texte ANSI, il s’agit du nombre d’octets ; pour le texte Unicode, il s’agit du nombre de caractères. La taille dans le premier mot est remplacée par la ligne copiée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est le nombre de **TCHAR** s copié. La valeur de retour est égale à zéro si le numéro de ligne spécifié par le paramètre *wParam* est supérieur au nombre de lignes dans le contrôle d’édition.

## <a name="remarks"></a>Notes

**Contrôles d’édition :** La ligne copiée ne contient pas de caractère null de fin.

**Contrôles RichEdit :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. La ligne copiée ne contient pas de caractère null de fin, sauf si aucun texte n’a été copié. Si aucun texte n’a été copié, le message place un caractère null au début de la mémoire tampon. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_LINELENGTH em**](em-linelength.md)
</dt> <dt>

[**Modifier \_ getline**](/windows/desktop/api/Windowsx/nf-windowsx-edit_getline)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

