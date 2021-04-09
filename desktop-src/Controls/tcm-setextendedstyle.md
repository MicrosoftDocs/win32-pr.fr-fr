---
title: Message TCM_SETEXTENDEDSTYLE (commctrl. h)
description: Définit les styles étendus que le contrôle onglet utilisera. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetExtendedStyle.
ms.assetid: 96ccebe1-2836-4198-8cd7-858401562c21
keywords:
- TCM_SETEXTENDEDSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c789b45eaae6cb3b1bc4fed6f216ec5010b463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032882"
---
# <a name="tcm_setextendedstyle-message"></a>\_Message SETEXTENDEDSTYLE TCM

Définit les styles étendus que le contrôle onglet utilisera. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur **DWORD** qui indique les styles de *lParam* à affecter. Seuls les styles étendus dans *wParam* seront modifiés. Tous les autres styles seront conservés tels quels. Si ce paramètre est égal à zéro, tous les styles de *lParam* sont affectés.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur qui spécifie les styles du contrôle onglet étendu. Cette valeur est une combinaison de [styles étendus](tab-control-extended-styles.md)de contrôle d’onglet.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **DWORD** qui contient les styles étendus du contrôle onglet précédent.

## <a name="remarks"></a>Notes

Le paramètre *wParam* vous permet de modifier un ou plusieurs styles étendus sans avoir à récupérer d’abord les styles existants. Par exemple, si vous transmettez des [**TCS \_ ex \_ FLATSEPARATORS**](tab-control-extended-styles.md) pour *wParam* et 0 pour *lParam*, le style **TCS \_ ex \_ FLATSEPARATORS** est effacé, mais tous les autres styles restent les mêmes.

Pour des raisons de compatibilité descendante, la macro [**TabCtrl \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) n’a pas été mise à jour pour utiliser *dwExMask*.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETEXTENDEDSTYLE TCM**](tcm-getextendedstyle.md)
</dt> </dl>

 

 





