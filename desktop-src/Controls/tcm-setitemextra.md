---
title: Message TCM_SETITEMEXTRA (commctrl. h)
description: Définit le nombre d’octets par onglet réservé pour les données définies par l’application dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetItemExtra.
ms.assetid: 8315f1fd-8eca-48bd-bb4a-71b09e8aa2c4
keywords:
- TCM_SETITEMEXTRA les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TCM_SETITEMEXTRA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6c7fdb47483ae0ddc841ae5f79b8f913e6a4f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116157"
---
# <a name="tcm_setitemextra-message"></a>\_Message SETITEMEXTRA TCM

Définit le nombre d’octets par onglet réservé pour les données définies par l’application dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ SetItemExtra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre d’octets supplémentaires.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Par défaut, le nombre d’octets supplémentaires est de quatre. Une application qui modifie le nombre d’octets supplémentaires ne peut pas utiliser la structure [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) pour récupérer et définir les données définies par l’application pour un onglet. Au lieu de cela, vous devez définir une nouvelle structure qui se compose de la structure [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) suivie de membres définis par l’application.

Une application doit uniquement modifier le nombre d’octets en trop lorsqu’un contrôle onglet ne contient pas d’onglets.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





