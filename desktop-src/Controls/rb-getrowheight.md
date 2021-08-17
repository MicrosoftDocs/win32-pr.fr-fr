---
title: Message RB_GETROWHEIGHT (commctrl. h)
description: Récupère la hauteur d’une ligne spécifiée dans un contrôle rebar.
ms.assetid: 1ff6a32e-b344-4dbc-b4a4-fb13f11a9d8c
keywords:
- RB_GETROWHEIGHT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- RB_GETROWHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ac650fb50f1b6594964ec0bf10d23a8c8b6b75ff82e14af44bb63e2c9cf8af8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409413"
---
# <a name="rb_getrowheight-message"></a>\_Message GETROWHEIGHT RB

Récupère la hauteur d’une ligne spécifiée dans un contrôle rebar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro d’une bande. La hauteur de la ligne qui contient la bande spécifiée est récupérée.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **uint** qui représente la hauteur de ligne, en pixels.

## <a name="remarks"></a>Remarques

Pour récupérer le nombre de lignes dans un contrôle rebar, utilisez le message [**RB \_ GETROWCOUNT**](rb-getrowcount.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





