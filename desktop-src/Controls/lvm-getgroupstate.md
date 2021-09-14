---
title: Message LVM_GETGROUPSTATE (commctrl. h)
description: Obtient l’état d’un groupe spécifié. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetGroupState.
ms.assetid: f087d17f-9066-44fb-b21b-ac7ceb56eb45
keywords:
- LVM_GETGROUPSTATE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETGROUPSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17b5bb25fd517816afd04bb700211222e6985f5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999821"
---
# <a name="lvm_getgroupstate-message"></a>\_Message GETGROUPSTATE LVM

Obtient l’état d’un groupe spécifié. Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ GetGroupState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Spécifie le groupe par **iGroupId** (voir structure [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ).

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Spécifie les valeurs d’État à récupérer. Il s’agit d’une combinaison des indicateurs listés pour le membre d' **État** de [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la combinaison des valeurs d’état définies. Par exemple, si *lParam* est LVGS \_ réduit et que la valeur retournée est zéro, l' \_ État réduit LVGS n’est pas défini. La valeur zéro est retournée si le groupe est introuvable.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





