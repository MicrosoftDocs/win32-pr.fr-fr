---
title: Message HDM_GETFOCUSEDITEM (commctrl. h)
description: Obtient l’élément dans un contrôle d’en-tête qui a le focus. Envoyez ce message de manière explicite ou à l’aide de la macro GetFocusedItem d’en-tête \_ .
ms.assetid: 9ad8e497-6f81-4226-b138-d1101f2fd8b3
keywords:
- HDM_GETFOCUSEDITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_GETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c21fcb29f5f431e32ca3f07265b7e96620d5a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465887"
---
# <a name="hdm_getfocuseditem-message"></a>\_Message HDM GETFOCUSEDITEM

Obtient l’élément dans un contrôle d’en-tête qui a le focus. Envoyez ce message de manière explicite ou à l’aide de la macro [**\_ GetFocusedItem d’en-tête**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Non utilisé. Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Non utilisé. Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index de l’élément dans le focus.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[À propos des contrôles Header](header-controls.md)
</dt> </dl>

 

 





