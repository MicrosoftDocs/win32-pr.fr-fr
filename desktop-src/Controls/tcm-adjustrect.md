---
title: Message TCM_ADJUSTRECT (commctrl. h)
description: Calcule la zone d’affichage d’un contrôle onglet en fonction d’un rectangle de fenêtre, ou calcule le rectangle de la fenêtre qui correspondrait à une zone d’affichage spécifiée. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl AdjustRect.
ms.assetid: 2f14201a-e4a3-4ae5-b9cf-4a674c52f24a
keywords:
- TCM_ADJUSTRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TCM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c1612a4f6c2fc436f858807fca59112c376a35
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116242"
---
# <a name="tcm_adjustrect-message"></a>\_Message ADJUSTRECT TCM

Calcule la zone d’affichage d’un contrôle onglet en fonction d’un rectangle de fenêtre, ou calcule le rectangle de la fenêtre qui correspondrait à une zone d’affichage spécifiée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Opération à effectuer. Si ce paramètre a la **valeur true**, *lParam* spécifie un rectangle d’affichage et reçoit le rectangle de fenêtre correspondant. Si ce paramètre a la **valeur false**, *lParam* spécifie un rectangle de fenêtre et reçoit la zone d’affichage correspondante.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui spécifie le rectangle donné et reçoit le rectangle calculé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Ce message s’applique uniquement aux contrôles d’onglet situés en haut. Elle ne s’applique pas aux contrôles d’onglet situés sur les côtés ou en bas.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

