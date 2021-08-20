---
title: Message EM_GETTEXTRANGE (RichEdit. h)
description: Récupère une plage de caractères spécifiée à partir d’un contrôle RichEdit.
ms.assetid: 18398963-eb2c-4f64-99f5-9614a5d34b52
keywords:
- EM_GETTEXTRANGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETTEXTRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e12282b970c38164e5b28a31ed778a3320f88bbdf16b6d182586e492e5e699eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006574"
---
# <a name="em_gettextrange-message"></a>\_Message GETTEXTRANGE em

Récupère une plage de caractères spécifiée à partir d’un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) qui spécifie la plage de caractères à récupérer et une mémoire tampon dans laquelle copier les caractères.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Le message retourne le nombre de caractères copiés, à l’exclusion du caractère null de fin.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea)
</dt> </dl>

 

 





