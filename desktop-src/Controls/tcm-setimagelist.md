---
title: Message TCM_SETIMAGELIST (commctrl. h)
description: Assigne une liste d’images à un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetImageList.
ms.assetid: b457c73c-4c38-4bc5-af5d-12bbd24504a6
keywords:
- TCM_SETIMAGELIST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59172c677998e816b295939c14effe45ff8aa961
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116161"
---
# <a name="tcm_setimagelist-message"></a>\_Message SETIMAGELIST TCM

Assigne une liste d’images à un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Handle de la liste d’images à assigner au contrôle onglet.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne le handle de la liste d’images précédente, ou **null** s’il n’existe aucune liste d’images précédente.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





