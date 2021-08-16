---
title: Message LVM_SUBITEMHITTEST (commctrl. h)
description: Détermine l’élément de vue de liste ou le sous-élément qui se trouve à une position donnée. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SubItemHitTest.
ms.assetid: 1468febb-af0d-4c04-b0b1-cda5ec77aa2c
keywords:
- LVM_SUBITEMHITTEST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SUBITEMHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 341f9b3f84646abe975c6543aef802450496154862353b7bbdd1af2c07c087ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830640"
---
# <a name="lvm_subitemhittest-message"></a>\_Message SUBITEMHITTEST LVM

Détermine l’élément de vue de liste ou le sous-élément qui se trouve à une position donnée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SubItemHitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être égal à 0. **Windows Vista.** Doit avoir la valeur-1 si le membre **iGroup** de *lParam* doit être récupéré.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) . La structure de [**points**](/previous-versions//dd162805(v=vs.85)) dans **LVHITTESTINFO** doit être définie sur les coordonnées clientes à tester.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index de l’élément ou du sous-élément testé, le cas échéant, ou-1 dans le cas contraire. Si un élément ou un sous-élément se trouve aux coordonnées données, les champs de la structure [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) seront remplis avec les informations de correspondance applicables.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

