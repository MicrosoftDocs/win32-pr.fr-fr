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
ms.openlocfilehash: f92fb85f7133053392bee39119c91b55240f84f0a51c8acc7dc9c732b596526c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104759"
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

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Par défaut, le nombre d’octets supplémentaires est de quatre. Une application qui modifie le nombre d’octets supplémentaires ne peut pas utiliser la structure [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) pour récupérer et définir les données définies par l’application pour un onglet. Au lieu de cela, vous devez définir une nouvelle structure qui se compose de la structure [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) suivie de membres définis par l’application.

Une application doit uniquement modifier le nombre d’octets en trop lorsqu’un contrôle onglet ne contient pas d’onglets.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





