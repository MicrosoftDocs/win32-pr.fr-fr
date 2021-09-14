---
title: Message TB_GETRECT (commctrl. h)
description: Récupère le rectangle englobant d’un bouton de barre d’outils spécifié.
ms.assetid: a93885eb-7eb7-4434-ad51-80fb30d3bfa1
keywords:
- TB_GETRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 889d067eb282e3d834ba4dc0cf6711c0561d86e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116722"
---
# <a name="tb_getrect-message"></a>TO \_ GETRECT message

Récupère le rectangle englobant d’un bouton de barre d’outils spécifié.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur de commande du bouton.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui recevra les informations de rectangle englobant.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Notes

Ce message ne récupère pas le rectangle englobant pour les boutons dont l’État est défini sur la valeur [**\_ masquée TBSTATE**](toolbar-button-states.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

