---
title: Message EM_SETEDITSTYLE (RichEdit. h)
description: Définit les indicateurs de style de modification actuels pour un contrôle RichEdit.
ms.assetid: e48de6b3-0fd2-4791-9863-a6dcdafa3642
keywords:
- EM_SETEDITSTYLE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06789b1d1fedfc76af205ac46aac7d3ea4bb882f2460676df96cd018d5a216b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048589"
---
# <a name="em_seteditstyle-message"></a>\_Message SETEDITSTYLE em

Définit les indicateurs de style de modification actuels pour un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie un ou plusieurs indicateurs de style de modification. Pour obtenir la liste des valeurs possibles, consultez [**em \_ GETEDITSTYLE**](em-geteditstyle.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Masque composé d’une ou plusieurs des valeurs *wParam* . Seules les valeurs spécifiées dans ce masque seront définies ou désactivées. Cela permet de définir ou d’effacer un seul indicateur sans lire les États de l’indicateur actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est l’état des indicateurs de style de modification après que le contrôle RichEdit a tenté d’implémenter vos modifications de style de modification. Les indicateurs de style de modification sont un ensemble d’indicateurs qui indiquent le style d’édition actuel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | Édition enrichie 3,0<br/>                                                              |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**EM \_ GETEDITSTYLE**](em-geteditstyle.md)
</dt> </dl>

 

 





