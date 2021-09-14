---
title: Message TCM_SETCURSEL (commctrl. h)
description: Sélectionne un onglet dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetCurSel.
ms.assetid: cf709d8c-c522-47c8-8ff3-463dc8e924b5
keywords:
- TCM_SETCURSEL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90033c5a19b0eb7b73f9ed886e8dad8d1ca4c2ab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116169"
---
# <a name="tcm_setcursel-message"></a>\_Message SETCURSEL TCM

Sélectionne un onglet dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’onglet à sélectionner.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’index de l’onglet précédemment sélectionné en cas de réussite, ou-1 dans le cas contraire.

## <a name="remarks"></a>Notes

Un contrôle onglet n’envoie pas de code de notification [TCN \_ SELCHANGING](tcn-selchanging.md) ou [TCN \_ selChange](tcn-selchange.md) lorsqu’un onglet est sélectionné à l’aide de ce message.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





