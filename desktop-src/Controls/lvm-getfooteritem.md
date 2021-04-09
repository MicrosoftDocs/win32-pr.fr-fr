---
title: Message LVM_GETFOOTERITEM (commctrl. h)
description: Obtient des informations sur un élément de pied de page dans un contrôle List-View. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetFooterItem.
ms.assetid: 92f55719-c265-433f-84fc-a673680c7ad9
keywords:
- LVM_GETFOOTERITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e642c9d853ae11edcd9199e48de61592de4883c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032352"
---
# <a name="lvm_getfooteritem-message"></a>\_Message GETFOOTERITEM LVM

Obtient des informations sur un élément de pied de page dans un contrôle List-View. Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ GetFooterItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Index de l'élément.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [**LVFOOTERITEM**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) pour recevoir une valeur pour l' **État** et/ou les membres **pszText** en fonction de la valeur du membre de **masque** . Le processus appelant est chargé d’allouer cette structure et de définir ses membres pour indiquer au destinataire les informations à retourner. Pour plus d’informations, consultez **LVFOOTERITEM**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





