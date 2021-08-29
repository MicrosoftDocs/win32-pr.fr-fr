---
title: Message LVM_GETHEADER (commctrl. h)
description: Obtient le handle du contrôle d’en-tête utilisé par le contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetHeader.
ms.assetid: 4708b493-4449-4844-bf0d-e6969bcf0246
keywords:
- LVM_GETHEADER les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETHEADER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d372085a6b8c81b61bc375bade7f4c9c502fc5cba38cc7c44039a881af2ada9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062589"
---
# <a name="lvm_getheader-message"></a>\_Message GETHEADER LVM

Obtient le handle du contrôle d’en-tête utilisé par le contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetHeader**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle du contrôle header.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





