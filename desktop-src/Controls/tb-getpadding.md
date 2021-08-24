---
title: Message TB_GETPADDING (commctrl. h)
description: Récupère le remplissage pour un contrôle de barre d’outils.
ms.assetid: dde0f44d-5d22-4cab-a7f8-48d84b8995d3
keywords:
- TB_GETPADDING les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f342e3322c0db60f46b0de353c2bbd2f6abe28717aa8ee23db8a3a9f26473113
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078323"
---
# <a name="tb_getpadding-message"></a>TO \_ GETPADDING message

Récupère le remplissage pour un contrôle de barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **DWORD** qui contient la marge intérieure horizontale dans le mot bas et la marge intérieure verticale dans le mot haut, en pixels.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TO \_ SETPADDING**](tb-setpadding.md)
</dt> </dl>

 

 





