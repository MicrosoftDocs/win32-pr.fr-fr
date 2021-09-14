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
ms.openlocfilehash: c811a3ed85b9eb157920f700b34d5d9c99597e67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012329"
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

## <a name="return-value"></a>Valeur de retour

Retourne l’index de l’élément ou du sous-élément testé, le cas échéant, ou-1 dans le cas contraire. Si un élément ou un sous-élément se trouve aux coordonnées données, les champs de la structure [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) seront remplis avec les informations de correspondance applicables.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

