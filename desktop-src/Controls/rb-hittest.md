---
title: Message RB_HITTEST (commctrl. h)
description: Détermine la partie d’une bande rebar située à un point donné sur l’écran, si une bande rebar existe à ce point.
ms.assetid: 8f27db21-50d8-438f-a44c-2e65dd93fa2a
keywords:
- RB_HITTEST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- RB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e17283bfce255672391ba9d8b6acd60fe41045b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117277"
---
# <a name="rb_hittest-message"></a>\_Message RB HITTEST

Détermine la partie d’une bande rebar située à un point donné sur l’écran, si une bande rebar existe à ce point.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo) . Avant d’envoyer le message, le membre **PT** de cette structure doit être initialisé au point qui fera l’élément d’un test de positionnement, en coordonnées clientes.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’index de base zéro de la bande au point donné, ou-1 si aucune bande de rebar n’était au point.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





