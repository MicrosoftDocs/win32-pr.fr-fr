---
title: Message TCM_DESELECTALL (commctrl. h)
description: Réinitialise des éléments dans un contrôle onglet, en effaçant tous ceux qui ont été définis sur l' \_ État TCIS BUTTONPRESSED. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl DeselectAll.
ms.assetid: cc2e5131-3c1b-473a-a0ca-274a2d39a2f1
keywords:
- TCM_DESELECTALL les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_DESELECTALL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f606538075a9163d8b8dc8328b5585b51b769aa5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105748"
---
# <a name="tcm_deselectall-message"></a>\_Message DESELECTALL TCM

Réinitialise des éléments dans un contrôle onglet, en effaçant tous ceux qui ont été définis sur l’état [**TCIS \_ BUTTONPRESSED**](tab-control-item-states.md) . Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indicateur qui spécifie la portée de la désélection de l’élément. Si ce paramètre est défini sur **false**, tous les éléments d’onglet sont réinitialisés. S’il est défini sur **true**, tous les éléments d’onglet, à l’exception de celui qui est actuellement sélectionné, sont réinitialisés.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de ce message n’est pas utilisée.

## <a name="remarks"></a>Notes

Ce message est significatif uniquement si l’indicateur de style de [**\_ boutons TCS**](tab-control-styles.md) a été défini.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





