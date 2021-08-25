---
title: Message EM_EXSETSEL (RichEdit. h)
description: Sélectionne une plage de caractères ou des objets COM (Component Object Model) dans un contrôle Rich Edit Microsoft.
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- EM_EXSETSEL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_EXSETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e35840e404f295b7d3ed6ddd5dddf4c77076c236eb3260f6f719b152cef207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915649"
---
# <a name="em_exsetsel-message"></a>\_Message EXSETSEL em

Sélectionne une plage de caractères ou des objets COM (Component Object Model) dans un contrôle Rich Edit Microsoft.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Structure [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) qui spécifie la plage de sélection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est la sélection qui est réellement définie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





