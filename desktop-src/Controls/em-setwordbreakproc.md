---
title: Message EM_SETWORDBREAKPROC (winuser. h)
description: Remplace la fonction WordWrap par défaut d’un contrôle d’édition par une fonction WordWrap définie par l’application. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: e5029b75-5f35-43a5-876d-24e81605bb49
keywords:
- EM_SETWORDBREAKPROC les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e85335562c9e9881093d89293e7e2ace9cf43b0a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006345"
---
# <a name="em_setwordbreakproc-message"></a>\_Message SETWORDBREAKPROC em

Remplace la fonction WordWrap par défaut d’un contrôle d’édition par une fonction WordWrap définie par l’application. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Adresse de la fonction WordWrap définie par l’application. Pour plus d’informations sur les lignes de rupture, consultez la description de la fonction de rappel [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Une fonction WordWrap analyse une mémoire tampon de texte qui contient du texte à envoyer à l’écran, en recherchant le premier mot qui ne tient pas sur la ligne active de l’écran. La fonction WordWrap place ce mot au début de la ligne suivante à l’écran.

Une fonction WordWrap définit le point auquel le système doit couper une ligne de texte pour les contrôles d’édition multiligne, généralement à un espace qui sépare deux mots. Un contrôle d’édition multiligne ou à une seule ligne peut appeler cette fonction lorsque l’utilisateur appuie sur les touches de direction en combinaison avec la touche CTRL pour déplacer le signe insertion vers le mot suivant ou le mot précédent. La fonction WordWrap par défaut divise une ligne de texte en un espace. La fonction définie par l’application peut définir le renvoi à la ligne au niveau d’un trait d’Union ou d’un caractère autre que le caractère d’espace.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[**\_FMTLINES em**](em-fmtlines.md)
</dt> <dt>

[**\_GETWORDBREAKPROC em**](em-getwordbreakproc.md)
</dt> </dl>

 

