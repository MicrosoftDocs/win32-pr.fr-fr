---
title: Message EM_PASTESPECIAL (RichEdit. h)
description: Colle un format de presse-papiers spécifique dans un contrôle RichEdit.
ms.assetid: b4b9c1a7-943d-4dc8-bcb9-054c984b82ba
keywords:
- EM_PASTESPECIAL les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_PASTESPECIAL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9375dd4a333f0e29d5e8f2721409244cf80f1233
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843817"
---
# <a name="em_pastespecial-message"></a>\_Message PASTESPECIAL em

Colle un format de presse-papiers spécifique dans un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie les [formats du presse-papiers](/windows/desktop/dataxchg/clipboard-formats).

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) ou **null**. Si un objet est collé, la structure **REPASTESPECIAL** est remplie avec l’aspect d’affichage souhaité. Si *lParam* a la **valeur null** ou si le membre **dwAspect** est égal à zéro, l’aspect d’affichage utilisé correspond au contenu du descripteur de l’objet.

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

[**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
</dt> </dl>

 

