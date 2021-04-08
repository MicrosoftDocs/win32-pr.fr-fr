---
title: Message EM_EXSETSEL (RichEdit. h)
description: Sélectionne une plage de caractères ou des objets COM (Component Object Model) dans un contrôle Rich Edit Microsoft.
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- EM_EXSETSEL les contrôles de message Windows
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
ms.openlocfilehash: 6939156fb1a8f35e03527e64a4c6f5185180668d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843821"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





