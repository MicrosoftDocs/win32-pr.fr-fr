---
title: Message TCM_DELETEALLITEMS (commctrl. h)
description: Supprime tous les éléments d’un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl DeleteAllItems.
ms.assetid: 733494c4-38f4-44ba-98d2-c33a8d63c3b7
keywords:
- TCM_DELETEALLITEMS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a67a8e2fdf1137b51a1baf0097be3a555f404d13851a0e58fe301d3eafd5c64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434149"
---
# <a name="tcm_deleteallitems-message"></a>\_Message DELETEALLITEMS TCM

Supprime tous les éléments d’un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteallitems) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

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



 

 





