---
title: Message LVM_UPDATE (commctrl. h)
description: Met à jour un élément d’affichage de liste. Si le contrôle List-View a le \_ style de réorganisation LVS, cette macro provoque la disposition du contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro Update de ListView.
ms.assetid: 81b332e9-4bea-481e-a7c5-613371103550
keywords:
- LVM_UPDATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_UPDATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cf2a4316e3ae3fc4dbab5e1afe780b03829b30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843145"
---
# <a name="lvm_update-message"></a>\_Message de mise à jour LVM

Met à jour un élément d’affichage de liste. Si le contrôle List-View a le style de [**\_ réorganisation LVS**](list-view-window-styles.md) , cette macro provoque la disposition du contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ Update de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’élément à mettre à jour.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





