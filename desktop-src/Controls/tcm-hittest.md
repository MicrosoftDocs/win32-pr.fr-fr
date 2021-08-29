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
ms.openlocfilehash: 47f0e619303300c5d04fc26a4b32009923422aede2a97b8faeb2175297c87d72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104829"
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

## <a name="return-value"></a>Valeur retournée

Retourne l’index de l’onglet ou-1 si aucun onglet n’est à la position spécifiée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





