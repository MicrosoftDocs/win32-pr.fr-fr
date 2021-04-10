---
title: Message HDM_GETITEMCOUNT (commctrl. h)
description: Obtient le nombre d’éléments dans un contrôle header. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ GetItemCount.
ms.assetid: 0e6d2131-53b4-4927-bd0f-577b8eaf237a
keywords:
- HDM_GETITEMCOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ac0e647a675adf2bf29b9ff1f204bbd8b040d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104485"
---
# <a name="hdm_getitemcount-message"></a>\_Message HDM GETITEMCOUNT

Obtient le nombre d’éléments dans un contrôle header. Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le nombre d’éléments en cas de réussite, ou-1 dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





