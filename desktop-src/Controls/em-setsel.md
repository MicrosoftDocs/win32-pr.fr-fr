---
title: Message EM_SETSEL (winuser. h)
description: Sélectionne une plage de caractères dans un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- EM_SETSEL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 190d8a62b874d3449e0a9bf5d334a515000fb0436ba73753a8657936363071b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062889"
---
# <a name="em_setsel-message"></a>\_Message SETSEL em

Sélectionne une plage de caractères dans un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Position du caractère de début de la sélection.

</dd> <dt>

*lParam* 
</dt> <dd>

Position du caractère de fin de la sélection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La valeur de début peut être supérieure à la valeur de fin. La plus petite des deux valeurs spécifie la position de caractère du premier caractère dans la sélection. La valeur la plus élevée spécifie la position du premier caractère au-delà de la sélection.

La valeur de début est le point d’ancrage de la sélection, et la valeur de fin est l’extrémité active. Si l’utilisateur utilise la touche Maj pour ajuster la taille de la sélection, l’extrémité active peut se déplacer, mais le point d’ancrage reste le même.

Si le début est égal à 0 et que la fin est égale à-1, tout le texte du contrôle d’édition est sélectionné. Si le début est-1, toute sélection actuelle est désélectionnée.

**Contrôles d’édition :** Le contrôle affiche un signe insertion clignotant à la position de fin, quelles que soient les valeurs relatives de début et de fin.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

Si le contrôle d’édition a le style [**es \_ NOHIDESEL**](edit-control-styles.md) , le texte sélectionné est mis en surbrillance, que le contrôle ait le focus ou non. Sans le style **es \_ NOHIDESEL** , le texte sélectionné est mis en surbrillance uniquement lorsque le contrôle d’édition a le focus.

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

[**\_GETSEL em**](em-getsel.md)
</dt> <dt>

[**\_REPLACESEL em**](em-replacesel.md)
</dt> <dt>

[**\_SCROLLCARET em**](em-scrollcaret.md)
</dt> <dt>

[**\_EXSETSEL em**](em-exsetsel.md)
</dt> </dl>

 

 





