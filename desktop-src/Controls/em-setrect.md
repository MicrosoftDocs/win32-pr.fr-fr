---
title: Message EM_SETRECT (winuser. h)
description: 'EM_SETRECT message : définit le rectangle de mise en forme d’un contrôle d’édition multiligne.'
ms.assetid: 4f576e94-3bd3-4416-a960-b7f22da963ea
keywords:
- EM_SETRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042428a236b8e9a23f03cdcceaf5d76eb977efd8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006362"
---
# <a name="em_setrect-message"></a>\_Message SETRECT em

Définit le [rectangle de mise en forme](about-edit-controls.md) d’un contrôle d’édition multiligne. Le rectangle de mise en forme est le rectangle de limitation dans lequel le contrôle dessine le texte. Le rectangle de limitation est indépendant de la taille de la fenêtre de contrôle d’édition.

Ce message est traité uniquement par les contrôles d’édition multiligne. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

**Édition enrichie 2,0 et versions ultérieures :** Indique si *lParam* spécifie des coordonnées absolues ou relatives. La valeur zéro indique des coordonnées absolues. La valeur 1 indique des décalages par rapport au rectangle de mise en forme actuel. (Les décalages peuvent être positifs ou négatifs.)

**Edit Controls et Rich edit 1,0 :** Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui spécifie les nouvelles dimensions du rectangle. Si ce paramètre a la **valeur null**, le rectangle de mise en forme est défini sur ses valeurs par défaut.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

L’affectation de la **valeur null** à *lParam* n’a aucun effet si un appareil tactile est installé, ou si **em \_ SETRECT** est envoyé à partir d’un thread sur lequel un raccordement est installé (voir [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)). Dans ces cas, *lParam* doit contenir un pointeur valide vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) .

Le message **em \_ SETRECT** provoque le redessin du texte du contrôle d’édition. Pour modifier la taille du rectangle de mise en forme sans redessiner le texte, utilisez le message [**em \_ SETRECTNP**](em-setrectnp.md) .

Lorsqu’un contrôle d’édition est créé pour la première fois, le rectangle de mise en forme est défini sur une taille par défaut. Vous pouvez utiliser le **message \_ SETRECT em** pour agrandir ou réduire la taille du rectangle de mise en forme par rapport à la fenêtre Modifier le contrôle.

Si le contrôle d’édition n’a pas de barre de défilement horizontale et que le rectangle de mise en forme est plus grand que la fenêtre de contrôle d’édition, les lignes de texte qui dépassent la largeur de la fenêtre de contrôle d’édition (mais inférieure à la largeur du rectangle de mise en forme) sont découpées au lieu d’être encapsulées.

Si le contrôle d’édition contient une bordure, le rectangle de mise en forme est réduit de la taille de la bordure. Si vous ajustez le rectangle retourné par un message [**em \_ GETRECT**](em-getrect.md) , vous devez supprimer la taille de la bordure avant d’utiliser le rectangle avec le message **em \_ SETRECT** .

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Le rectangle de mise en forme n’inclut pas la barre de sélection, qui est une zone non marquée à gauche de chaque paragraphe. Lorsque l’utilisateur clique dans la barre de sélection, la ligne correspondante est sélectionnée. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

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

[**\_GETRECT em**](em-getrect.md)
</dt> <dt>

[**\_SETRECTNP em**](em-setrectnp.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**RECTANGULAIRE**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

