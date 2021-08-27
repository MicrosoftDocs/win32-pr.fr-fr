---
title: Message TVM_HITTEST (commctrl. h)
description: Détermine l’emplacement du point spécifié par rapport à la zone cliente d’un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TreeView HitTest.
ms.assetid: 18ea3737-f429-4c10-9133-3b5729aa36fa
keywords:
- TVM_HITTEST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e564b6d82c04c0d007784aac39284db13b3776267d524d2f615353ede50eb945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060149"
---
# <a name="tvm_hittest-message"></a>\_Message TVM HITTEST

Détermine l’emplacement du point spécifié par rapport à la zone cliente d’un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TreeView \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) . Lorsque le message est envoyé, le membre **PT** spécifie les coordonnées du point à tester. Lorsque le message est retourné, le membre **hitem** est le handle de l’élément au point spécifié ou **null** si aucun élément n’occupe le point. En outre, lorsque le message retourne, le membre **indicateurs** est une valeur de test de positionnement qui indique l’emplacement du point spécifié. Pour obtenir la liste des valeurs de test de positionnement, consultez la description de la structure **TVHITTESTINFO** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle de l’élément d’arborescence qui occupe le point spécifié, ou **null** si aucun élément n’occupe le point.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





