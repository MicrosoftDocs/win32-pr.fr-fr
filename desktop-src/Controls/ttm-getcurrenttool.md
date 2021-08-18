---
title: Message TTM_GETCURRENTTOOL (commctrl. h)
description: Récupère les informations de l’outil en cours dans un contrôle ToolTip.
ms.assetid: acb254cf-064c-4ed8-b488-a3138b648405
keywords:
- TTM_GETCURRENTTOOL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TTM_GETCURRENTTOOL
- TTM_GETCURRENTTOOLA
- TTM_GETCURRENTTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4558e582e4619cd7d96380a1e38e2efe68808b9241e4c627e12a74946965d8de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769339"
---
# <a name="ttm_getcurrenttool-message"></a>\_Message atténuation GETCURRENTTOOL

Récupère les informations de l’outil en cours dans un contrôle ToolTip.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) qui reçoit des informations sur l’outil en cours. Si cette valeur est **null**, la valeur de retour indique l’existence de l’outil actuel sans récupérer réellement les informations de l’outil. Si cette valeur n’est pas **null**, le membre **cbSize** de la structure **TOOLINFO** doit être rempli avant l’envoi de ce message.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire. Si *lParam* a la **valeur null**, retourne une valeur différente de zéro si un outil en cours existe, ou zéro dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **Atténuation \_ GETCURRENTTOOLW** (Unicode) et **atténuation \_ GETCURRENTTOOLA** (ANSI)<br/>     |



 

 





