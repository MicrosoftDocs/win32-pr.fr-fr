---
title: Message EM_GETBIDIOPTIONS (RichEdit. h)
description: Indique l’état actuel des options bidirectionnelles dans le contrôle Rich Edit.
ms.assetid: 055581c0-ae59-4601-a3e9-416705af429a
keywords:
- EM_GETBIDIOPTIONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fade63ac94007bedbf58642dc7a9451eb158fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104047"
---
# <a name="em_getbidioptions-message"></a>\_Message GETBIDIOPTIONS em

Indique l’état actuel des options bidirectionnelles dans le contrôle Rich Edit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Structure [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) qui reçoit l’état actuel des options bidirectionnelles dans le contrôle Rich Edit.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Ce message définit les valeurs des membres **wMask** et **wEffects** sur la valeur de l’état actuel des options bidirectionnelles dans le contrôle Rich Edit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | Édition enrichie 3,0<br/>                                                              |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[**\_SETBIDIOPTIONS em**](em-setbidioptions.md)
</dt> </dl>

 

 





