---
title: Message EM_GETTHUMB (winuser. h)
description: Obtient la position de la case de défilement (Thumb) dans la barre de défilement verticale d’un contrôle d’édition multiligne. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 04bd0102-1652-405b-8c42-50e138abaf75
keywords:
- EM_GETTHUMB les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETTHUMB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e6689c530794e11897f1f88a7d5864058d53aa8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105112"
---
# <a name="em_getthumb-message"></a>\_Message GETTHUMB em

Obtient la position de la case de défilement (Thumb) dans la barre de défilement verticale d’un contrôle d’édition multiligne. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

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

La valeur de retour correspond à la position de la case de défilement.

## <a name="remarks"></a>Notes

**Modification riche :** Pris en charge dans Microsoft Rich Edit 2,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



 

 





