---
title: Message EM_GETSEL (winuser. h)
description: Obtient les positions des caractères de début et de fin (en TCHARs) de la sélection actuelle dans un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- EM_GETSEL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca5f3cf1fdaa3c40dd1bb25ebbabb672474e76ae621a05cf52247c216adca17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048799"
---
# <a name="em_getsel-message"></a>\_Message GETSEL em

Obtient les positions des caractères de début et de fin (dans **TCHAR** s) de la sélection actuelle dans un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Pointeur vers une valeur **DWORD** qui reçoit la position de départ de la sélection. Ce paramètre peut être **NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une valeur **DWORD** qui reçoit la position du premier caractère non sélectionné après la fin de la sélection. Ce paramètre peut être **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est une valeur de base zéro avec la position de départ de la sélection dans le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) et la position du premier **TCHAR** après le dernier **TCHAR** sélectionné dans le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Si l’une de ces valeurs dépasse 65 535, la valeur de retour est-1.

Il est préférable d’utiliser les valeurs retournées dans *wParam* et *lParam* , car il s’agit de valeurs 32 bits complètes.

## <a name="remarks"></a>Remarques

S’il n’y a aucune sélection, les valeurs de début et de fin sont à la fois la position du signe insertion.

**Contrôles RichEdit :** Vous pouvez également utiliser le [**message \_ EXGETSEL em**](em-exgetsel.md) pour récupérer les mêmes informations. **Em \_ EXGETSEL** retourne également les positions des caractères de début et de fin en tant que valeurs 32 bits.

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

[**\_EXGETSEL em**](em-exgetsel.md)
</dt> <dt>

[**\_SETSEL em**](em-setsel.md)
</dt> </dl>

 

