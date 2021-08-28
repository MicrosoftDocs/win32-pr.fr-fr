---
title: Message LVM_DELETEITEM (commctrl. h)
description: Supprime un élément d’un contrôle List-View. Vous pouvez envoyer ce message de manière explicite ou à l’aide de la macro de ListView \_ .
ms.assetid: 0eddd4c1-7786-4a8c-a16d-9fd83cce98b3
keywords:
- LVM_DELETEITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88520e7d4f9d0d3ff22f90d7cea033b7674cfcbadbf55358f7ced8cc36c2399a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958418"
---
# <a name="lvm_deleteitem-message"></a>Message de LVM. \_

Supprime un élément d’un contrôle List-View. Vous pouvez envoyer ce message de manière explicite ou à l’aide de la macro de [**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteitem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’élément de vue de liste à supprimer.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





