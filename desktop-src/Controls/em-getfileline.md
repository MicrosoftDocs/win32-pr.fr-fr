---
title: Message EM_GETFILELINE (CommCtrl. h)
description: Copie une ligne de texte à partir d’un contrôle d’édition, indépendamment de la façon dont les lignes sont affichées à l’écran, et les place dans une mémoire tampon spécifiée.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- EM_GETFILELINE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 6b3be3ea4ae883fc808f7ddc8fb60f0d93bcd6ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466110"
---
# <a name="em_getfileline-message-commctrlh"></a>Message EM_GETFILELINE (CommCtrl. h)

Copie une ligne de texte à partir d’un contrôle d’édition, indépendamment de la façon dont les lignes sont affichées à l’écran, et les place dans une mémoire tampon spécifiée.

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

La ligne copiée ne contient pas de caractère null de fin.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, 1809 \[ uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2019 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_FILELINELENGTH em**](em-filelinelength.md)
</dt> <dt>

[**Modifier \_ GetFileLine**](/windows/win32/api/commctrl/nf-commctrl-edit_getfileline)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

