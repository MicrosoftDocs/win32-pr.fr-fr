---
title: Message EM_CHARFROMPOS (winuser. h)
description: Obtient des informations sur le caractère le plus proche d’un point spécifié dans la zone cliente d’un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: fe9f96f2-5b3c-4039-befd-5e9a456ba32d
keywords:
- EM_CHARFROMPOS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_CHARFROMPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a133907b29857abdc1663d3283bc4b4164878f3fa0976769e6d42daef2c4cb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915959"
---
# <a name="em_charfrompos-message"></a>\_Message CHARFROMPOS em

Obtient des informations sur le caractère le plus proche d’un point spécifié dans la zone cliente d’un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Coordonnées d’un point dans la zone cliente du contrôle. Les coordonnées sont exprimées en unités d’écran et sont relatives au coin supérieur gauche de la zone cliente du contrôle.

**Contrôles RichEdit :** Pointeur vers une structure de [**pointeurs**](/previous-versions//dd162807(v=vs.85)) qui contient les coordonnées horizontales et verticales.

**Contrôles d’édition :** [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient la coordonnée horizontale. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contient la coordonnée verticale.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**Contrôles RichEdit :** La valeur de retour spécifie l’index de caractère de base zéro du caractère le plus proche du point spécifié. La valeur de retour indique le dernier caractère dans le contrôle d’édition si le point spécifié est au-delà du dernier caractère dans le contrôle.

**Contrôles d’édition :** [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie l’index de base zéro du caractère le plus proche du point spécifié. Cet index est relatif au début du contrôle, et non au début de la ligne. Si le point spécifié est au-delà du dernier caractère du contrôle d’édition, la valeur de retour indique le dernier caractère dans le contrôle. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie l’index de base zéro de la ligne qui contient le caractère. Pour les contrôles d’édition sur une seule ligne, cette valeur est égale à zéro. L’index indique le séparateur de lignes si le point spécifié est au-delà du dernier caractère visible d’une ligne.

## <a name="remarks"></a>Remarques

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

Si un point est passé à **em \_ CHARFROMPOS** comme *lParam* et que le point se trouve en dehors des limites du contrôle d’édition, la *LRESULT* est (65535, 65535).

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

[**\_POSFROMCHAR em**](em-posfromchar.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**POINTer**](/previous-versions//dd162807(v=vs.85))
</dt> </dl>

 

