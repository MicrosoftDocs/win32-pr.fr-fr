---
title: Message LVM_GETHEADER (commctrl. h)
description: Obtient le handle du contrôle d’en-tête utilisé par le contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetHeader.
ms.assetid: 4708b493-4449-4844-bf0d-e6969bcf0246
keywords:
- LVM_GETHEADER les contrôles de message Windows
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
ms.openlocfilehash: 3d53082092118cad373005743849498791f0e1ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032428"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





