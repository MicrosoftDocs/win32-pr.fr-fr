---
title: Message EM_GETWORDBREAKPROC (winuser. h)
description: Obtient l’adresse de la fonction de WordWrap en cours. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 564b4b1b-913f-4040-bb28-eea50c0c3738
keywords:
- EM_GETWORDBREAKPROC les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f615721328ce0062d6bba9c282466744e7b47c78ad335b905343893f9c1b6343
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119438059"
---
# <a name="em_getwordbreakproc-message"></a>\_Message GETWORDBREAKPROC em

Obtient l’adresse de la fonction de WordWrap en cours. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

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

La valeur de retour spécifie l’adresse de la fonction WordWrap définie par l’application. La valeur de retour est **null** si aucune fonction de WordWrap n’existe.

## <a name="remarks"></a>Remarques

Une fonction WordWrap analyse une mémoire tampon de texte qui contient le texte à envoyer à l’écran, en recherchant le premier mot qui ne tient pas sur la ligne d’affichage actuelle. La fonction WordWrap place ce mot au début de la ligne suivante à l’écran. Une fonction WordWrap définit le point auquel le système doit couper une ligne de texte pour les contrôles d’édition multiligne, généralement à un espace qui sépare deux mots.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Configuration requise



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

[**\_SETWORDBREAKPROC em**](em-setwordbreakproc.md)
</dt> </dl>

 

