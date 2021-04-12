---
title: Message LVM_SUBITEMHITTEST (commctrl. h)
description: Détermine l’élément de vue de liste ou le sous-élément qui se trouve à une position donnée. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SubItemHitTest.
ms.assetid: 1468febb-af0d-4c04-b0b1-cda5ec77aa2c
keywords:
- LVM_SUBITEMHITTEST les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464407"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

