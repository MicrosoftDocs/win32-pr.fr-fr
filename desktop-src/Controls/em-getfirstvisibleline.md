---
title: Message EM_GETFIRSTVISIBLELINE (winuser. h)
description: Obtient l’index de base zéro de la ligne visible supérieure dans un contrôle d’édition multiligne. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 022838d2-7948-4c5a-92ca-655822c4f672
keywords:
- EM_GETFIRSTVISIBLELINE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETFIRSTVISIBLELINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb759be166b69b3cfa488e9e23d61d9e0ec42d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117897"
---
# <a name="em_getfirstvisibleline-message"></a>\_Message GETFIRSTVISIBLELINE em

Obtient l’index de base zéro de la ligne visible supérieure dans un contrôle d’édition multiligne. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

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

## <a name="return-value"></a>Valeur de retour

La valeur de retour est l’index de base zéro de la ligne visible supérieure dans un contrôle d’édition multiligne.

**Contrôles d’édition :** Pour les contrôles d’édition sur une seule ligne, la valeur de retour est l’index de base zéro du premier caractère visible.

**Contrôles RichEdit :** Pour les contrôles RichEdit sur une seule ligne, la valeur de retour est zéro.

## <a name="remarks"></a>Notes

Le nombre de lignes et la longueur des lignes d’un contrôle d’édition dépendent de la largeur du contrôle et du paramètre de WordWrap actuel.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



 

 





