---
title: Message RB_GETPALETTE (commctrl. h)
description: Récupère la palette actuelle du contrôle rebar.
ms.assetid: f9eeefb3-8308-45bf-89e4-4f282ee6d935
keywords:
- RB_GETPALETTE les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_GETPALETTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36dd2764b6a8951a337c990dcbcfb8e5aff9c56b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104446"
---
# <a name="rb_getpalette-message"></a>\_Message GETPALETTE RB

Récupère la palette actuelle du contrôle rebar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un **HPALETTE** qui spécifie la palette actuelle du contrôle rebar.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETPALETTE RB**](rb-setpalette.md)
</dt> </dl>

 

 





