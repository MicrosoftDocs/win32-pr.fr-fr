---
title: Message TCM_SETITEMEXTRA (commctrl. h)
description: Définit le nombre d’octets par onglet réservé pour les données définies par l’application dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetItemExtra.
ms.assetid: 8315f1fd-8eca-48bd-bb4a-71b09e8aa2c4
keywords:
- TCM_SETITEMEXTRA les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102856"
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

## <a name="remarks"></a>Notes

Par défaut, le nombre d’octets supplémentaires est de quatre. Une application qui modifie le nombre d’octets supplémentaires ne peut pas utiliser la structure [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) pour récupérer et définir les données définies par l’application pour un onglet. Au lieu de cela, vous devez définir une nouvelle structure qui se compose de la structure [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) suivie de membres définis par l’application.

Une application doit uniquement modifier le nombre d’octets en trop lorsqu’un contrôle onglet ne contient pas d’onglets.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





