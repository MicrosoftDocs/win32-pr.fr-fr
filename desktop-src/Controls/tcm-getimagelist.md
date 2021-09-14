---
title: Message TCM_GETIMAGELIST (commctrl. h)
description: Récupère la liste d’images associée à un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl GetImageList.
ms.assetid: 86a0d8c7-ff3d-4e16-994e-4c72d1e62e9f
keywords:
- TCM_GETIMAGELIST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c4d471ef4d072e4305507f4f5ebc4a8f2745ed9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116217"
---
# <a name="tcm_getimagelist-message"></a>\_Message GETIMAGELIST TCM

Récupère la liste d’images associée à un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getimagelist) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne le handle de la liste d’images en cas de réussite, ou **null** dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





