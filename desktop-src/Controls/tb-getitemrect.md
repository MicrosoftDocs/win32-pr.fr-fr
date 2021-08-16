---
title: Message TB_GETITEMRECT (commctrl. h)
description: Récupère le rectangle englobant d’un bouton dans une barre d’outils.
ms.assetid: 42c2c86e-0002-4029-be6a-fdfdf405b78c
keywords:
- TB_GETITEMRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6dbfa4c7e305c4e2dfe53b45edaac1d6601631c920fa266c64292fd7e6d97e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829704"
---
# <a name="tb_getitemrect-message"></a>TO \_ GETITEMRECT message

Récupère le rectangle englobant d’un bouton dans une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro du bouton pour lequel des informations doivent être récupérées.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui reçoit les coordonnées clientes du rectangle englobant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Ce message ne récupère pas le rectangle englobant pour les boutons dont l’État est défini sur la valeur [**\_ masquée TBSTATE**](toolbar-button-states.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

