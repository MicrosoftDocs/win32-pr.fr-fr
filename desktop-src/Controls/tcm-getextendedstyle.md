---
title: Message TCM_GETEXTENDEDSTYLE (commctrl. h)
description: Récupère les styles étendus en cours d’utilisation pour le contrôle Tab. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl GetExtendedStyle.
ms.assetid: 983ffcbe-0d8d-4686-83de-fc564744390f
keywords:
- TCM_GETEXTENDEDSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8280b7043591dd4fdd0b453c5baea5fe014bd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942699"
---
# <a name="tcm_getextendedstyle-message"></a>\_Message GETEXTENDEDSTYLE TCM

Récupère les styles étendus en cours d’utilisation pour le contrôle Tab. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **DWORD** qui représente les styles étendus actuellement utilisés pour le contrôle Tab. Cette valeur est une combinaison de [styles étendus](tab-control-extended-styles.md)de contrôle d’onglet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETEXTENDEDSTYLE TCM**](tcm-setextendedstyle.md)
</dt> </dl>

 

 





