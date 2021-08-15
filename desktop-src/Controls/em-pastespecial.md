---
title: Message EM_PASTESPECIAL (RichEdit. h)
description: Colle un format de presse-papiers spécifique dans un contrôle RichEdit.
ms.assetid: b4b9c1a7-943d-4dc8-bcb9-054c984b82ba
keywords:
- EM_PASTESPECIAL les contrôles de Windows de message
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
ms.openlocfilehash: 2dc1af4dd0566cdf8e256b34f87fcc52ea855bc521c87cbe390e02b8b1cf7b06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412800"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
</dt> </dl>

 

