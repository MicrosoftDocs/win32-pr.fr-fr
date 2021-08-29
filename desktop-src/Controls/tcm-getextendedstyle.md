---
title: Message TCM_GETEXTENDEDSTYLE (commctrl. h)
description: Récupère les styles étendus en cours d’utilisation pour le contrôle Tab. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl GetExtendedStyle.
ms.assetid: 983ffcbe-0d8d-4686-83de-fc564744390f
keywords:
- TCM_GETEXTENDEDSTYLE les contrôles de Windows de message
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
ms.openlocfilehash: be5c4618fe039fcd05a73e409f0e8ddd7042694d526f902d432d2513bbef96e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876569"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETEXTENDEDSTYLE TCM**](tcm-setextendedstyle.md)
</dt> </dl>

 

 





