---
title: Message EM_GETSEL (winuser. h)
description: Obtient les positions des caractères de début et de fin (en TCHARs) de la sélection actuelle dans un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- EM_GETSEL les contrôles de message Windows
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
ms.openlocfilehash: d28ba97c9043866c3e97c1c51389447498562455
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032800"
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

## <a name="remarks"></a>Notes

S’il n’y a aucune sélection, les valeurs de début et de fin sont à la fois la position du signe insertion.

**Contrôles RichEdit :** Vous pouvez également utiliser le [**message \_ EXGETSEL em**](em-exgetsel.md) pour récupérer les mêmes informations. **Em \_ EXGETSEL** retourne également les positions des caractères de début et de fin en tant que valeurs 32 bits.

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

[**\_EXGETSEL em**](em-exgetsel.md)
</dt> <dt>

[**\_SETSEL em**](em-setsel.md)
</dt> </dl>

 

