---
title: Message TCM_HITTEST (commctrl. h)
description: Détermine l’onglet, le cas échéant, à la position d’écran spécifiée. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl HitTest.
ms.assetid: 0334f616-8d39-4460-a7f8-692a9ffab012
keywords:
- TCM_HITTEST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04787662e417513d8c9c93e45cecd0d8bddc6cfa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116185"
---
# <a name="tcm_hittest-message"></a>\_Message TCM HITTEST

Détermine l’onglet, le cas échéant, à la position d’écran spécifiée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) qui spécifie la position à l’écran à tester.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’index de l’onglet ou-1 si aucun onglet n’est à la position spécifiée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





