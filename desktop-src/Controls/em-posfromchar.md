---
title: Message EM_POSFROMCHAR (winuser. h)
description: Récupère les coordonnées de la zone cliente d’un caractère spécifié dans un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: a32532fa-976f-4c19-ac6e-29e5614fc410
keywords:
- EM_POSFROMCHAR les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_POSFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d98968873ad006b2e91cf3add2429bf7630fae1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508710"
---
# <a name="em_posfromchar-message"></a>\_Message POSFROMCHAR em

Récupère les coordonnées de la zone cliente d’un caractère spécifié dans un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

**Édition enrichie 1,0 et 3,0 :** Pointeur vers une structure [**pointer**](/previous-versions//dd162807(v=vs.85)) qui reçoit les coordonnées de la zone cliente du caractère. Les coordonnées sont exprimées en unités d’écran et sont relatives au coin supérieur gauche de la zone cliente du contrôle.

**Edit Controls et Rich edit 2,0 :** Index de base zéro du caractère.

</dd> <dt>

*lParam* 
</dt> <dd>

**Édition enrichie 1,0 et 3,0 :** Index de base zéro du caractère.

**Edit Controls et Rich edit 2,0 :** Ce paramètre n’est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**Édition enrichie 1,0 et 3,0 :** La valeur de retour n’est pas utilisée.

**Edit Controls et Rich edit 2,0 :** La valeur de retour contient les coordonnées de la zone cliente du caractère. Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient la coordonnée horizontale et le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contient la coordonnée verticale.

## <a name="remarks"></a>Notes

Une coordonnée retournée peut être une valeur négative si le caractère spécifié n’est pas affiché dans la zone cliente du contrôle d’édition. Les coordonnées sont tronquées en valeurs entières.

Si le caractère est un délimiteur de ligne, les coordonnées retournées indiquent un point situé juste après le dernier caractère visible dans la ligne. Si l’index spécifié est supérieur à l’index du dernier caractère du contrôle, le contrôle retourne-1.

**Édition enrichie 3,0 et versions ultérieures :** Pour la compatibilité descendante, Microsoft Rich Edit 3,0 prend en charge la syntaxe utilisée par Microsoft Rich Edit 2,0. Si Microsoft Rich Edit 3,0 détecte que *wParam* n’est pas un pointeur [**pointer**](/previous-versions//dd162807(v=vs.85)) valide, il suppose que le message a été envoyé à l’aide de la syntaxe Microsoft Rich Edit 2,0. Dans ce cas, elle utilise la valeur de retour pour retourner les coordonnées.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

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

[**\_CHARFROMPOS em**](em-charfrompos.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**POINTer**](/previous-versions//dd162807(v=vs.85))
</dt> </dl>

 

