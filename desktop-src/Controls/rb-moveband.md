---
title: Message RB_MOVEBAND (commctrl. h)
description: Déplace une bande d’un index vers un autre.
ms.assetid: bb5b45de-957e-46fb-b59a-18b55b69c395
keywords:
- RB_MOVEBAND les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_MOVEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 146103c4c3d70fc0514729a00eac152c4847b85c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464391"
---
# <a name="rb_moveband-message"></a>\_Message MOVEBAND RB

Déplace une bande d’un index vers un autre.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la bande à déplacer.

</dd> <dt>

*lParam* 
</dt> <dd>

Index de base zéro de la nouvelle position de la bande.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Notes

Ce message modifiera probablement l’index d’autres bandes dans le contrôle rebar. Si une bande est déplacée de l’index 6 à l’index 0, toutes les bandes comprises entre auront l’index incrémenté d’une unité.

*lParam* ne doit jamais être supérieur au nombre de bandes moins un. Le nombre de bandes peut être obtenu avec le message [**RB \_ GETBANDCOUNT**](rb-getbandcount.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





