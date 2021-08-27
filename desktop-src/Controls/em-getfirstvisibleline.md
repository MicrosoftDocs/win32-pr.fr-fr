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
ms.openlocfilehash: 11eb93c1c7dcce7f502945df4e063b22c29514bc79fe7310875e9de055e1d745
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049209"
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

## <a name="return-value"></a>Valeur retournée

La valeur de retour est l’index de base zéro de la ligne visible supérieure dans un contrôle d’édition multiligne.

**Contrôles d’édition :** Pour les contrôles d’édition sur une seule ligne, la valeur de retour est l’index de base zéro du premier caractère visible.

**Contrôles RichEdit :** Pour les contrôles RichEdit sur une seule ligne, la valeur de retour est zéro.

## <a name="remarks"></a>Remarques

Le nombre de lignes et la longueur des lignes d’un contrôle d’édition dépendent de la largeur du contrôle et du paramètre de WordWrap actuel.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



 

 





