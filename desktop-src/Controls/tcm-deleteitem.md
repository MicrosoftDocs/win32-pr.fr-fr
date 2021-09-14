---
title: Message TCM_DELETEITEM (commctrl. h)
description: Supprime un élément d’un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl DeleteItem.
ms.assetid: 54bfa446-580a-4ea7-b5e9-9429f4ee1c2b
keywords:
- TCM_DELETEITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TCM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ad4f57b63c154ee98fc48a59ac81bf4fd61ba5a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116237"
---
# <a name="tcm_deleteitem-message"></a>\_Message TCM DELETEITEM

Supprime un élément d’un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’élément à supprimer.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





