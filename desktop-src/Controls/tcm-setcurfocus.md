---
title: Message TCM_SETCURFOCUS (commctrl. h)
description: Définit le focus sur un onglet spécifié dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetCurFocus.
ms.assetid: bcbd5f26-b54e-492b-aff3-357b8ae23969
keywords:
- TCM_SETCURFOCUS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TCM_SETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe566d1e1b3cc7d257c4756fe123423fc344a7f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116173"
---
# <a name="tcm_setcurfocus-message"></a>\_Message SETCURFOCUS TCM

Définit le focus sur un onglet spécifié dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ SetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’onglet qui obtient le focus.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Si le contrôle onglet a le style de [**\_ boutons TCS**](tab-control-styles.md) (mode bouton), l’onglet avec le focus peut être différent de l’onglet sélectionné. Par exemple, lorsqu’un onglet est sélectionné, l’utilisateur peut appuyer sur les touches de direction pour définir le focus sur un autre onglet sans modifier l’onglet sélectionné. En mode bouton, **TCM \_ SETCURFOCUS** définit le focus d’entrée sur le bouton associé à l’onglet spécifié, mais il ne modifie pas l’onglet sélectionné.

Si le contrôle onglet n’a pas le style de [**\_ boutons TCS**](tab-control-styles.md) , le fait de modifier le focus modifie également l’onglet sélectionné. Dans ce cas, le contrôle onglet envoie les codes de notification [TCN \_ SELCHANGING](tcn-selchanging.md) et [TCN \_ selChange](tcn-selchange.md) à sa fenêtre parente.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETCURFOCUS TCM**](tcm-getcurfocus.md)
</dt> </dl>

 

 





