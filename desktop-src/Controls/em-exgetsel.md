---
title: Message EM_EXGETSEL (RichEdit. h)
description: Récupère les positions des caractères de début et de fin de la sélection dans un contrôle RichEdit.
ms.assetid: 60fcf13e-6c45-4f4e-9b54-70f0985122fb
keywords:
- EM_EXGETSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_EXGETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b97fb43a76f0f8ac91dd16c0cfa5700c5431eb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465894"
---
# <a name="em_exgetsel-message"></a>\_Message EXGETSEL em

Récupère les positions des caractères de début et de fin de la sélection dans un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Structure [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) qui reçoit la plage de sélection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> </dl>

 

 





