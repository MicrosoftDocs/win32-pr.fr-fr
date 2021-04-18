---
title: Message LVM_GETTEXTCOLOR (commctrl. h)
description: Récupère la couleur de texte d’un contrôle List View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetTextColor.
ms.assetid: 51685e61-dd0a-4c21-8c66-31cf72c2b3e4
keywords:
- LVM_GETTEXTCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7686e8f06f49dbfc14899f47ba52017daaf23c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106533573"
---
# <a name="lvm_gettextcolor-message"></a>\_Message GETTEXTCOLOR LVM

Récupère la couleur de texte d’un contrôle List View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextcolor) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la couleur du texte.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





