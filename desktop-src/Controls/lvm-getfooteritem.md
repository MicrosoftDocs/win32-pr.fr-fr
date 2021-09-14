---
title: Message LVM_GETFOOTERITEM (commctrl. h)
description: Obtient des informations sur un élément de pied de page dans un contrôle List-View. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetFooterItem.
ms.assetid: 92f55719-c265-433f-84fc-a673680c7ad9
keywords:
- LVM_GETFOOTERITEM les contrôles de Windows de message
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999835"
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

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





