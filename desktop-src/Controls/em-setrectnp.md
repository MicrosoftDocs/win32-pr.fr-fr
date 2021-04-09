---
title: Message EM_SETRECTNP (winuser. h)
description: Définit le rectangle de mise en forme d’un contrôle d’édition multiligne.
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- EM_SETRECTNP les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETRECTNP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e017bd4737c843c2452382918d71ef63345917cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942661"
---
# <a name="em_setrectnp-message"></a>\_Message SETRECTNP em

Définit le [rectangle de mise en forme](about-edit-controls.md) d’un contrôle d’édition multiligne. Le **message em \_ SETRECTNP** est identique au message [**em \_ SETRECT**](em-setrect.md) , sauf que **em \_ SETRECTNP** ne redessine *pas* la fenêtre de contrôle d’édition.

Le rectangle de mise en forme est le rectangle de limitation dans lequel le contrôle dessine le texte. Le rectangle de limitation est indépendant de la taille de la fenêtre de contrôle d’édition.

Ce message est traité uniquement par les contrôles d’édition multiligne. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

**Édition enrichie 3,0 et versions ultérieures :** Indique si le nouveau rectangle contient des coordonnées absolues ou relatives. La valeur zéro indique des coordonnées absolues. La valeur 1 indique des décalages par rapport au rectangle de mise en forme actuel. (Les décalages peuvent être positifs ou négatifs.)

**Contrôles d’édition :** Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui spécifie les nouvelles dimensions du rectangle. Si ce paramètre a la **valeur null**, le rectangle de mise en forme est défini sur ses valeurs par défaut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

**Modification riche :** Pris en charge dans Microsoft Rich Edit 3,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

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

[**\_SETRECT em**](em-setrect.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**RECTANGULAIRE**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

