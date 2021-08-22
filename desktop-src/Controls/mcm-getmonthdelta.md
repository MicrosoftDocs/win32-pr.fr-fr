---
title: Message MCM_GETMONTHDELTA (commctrl. h)
description: Récupère la vitesse de défilement pour un contrôle Month Calendar. La vitesse de défilement est le nombre de mois pendant lesquels le contrôle déplace son affichage lorsque l’utilisateur clique sur un bouton de défilement. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetMonthDelta.
ms.assetid: 6db02993-b22c-430f-8928-8bd5768b2151
keywords:
- MCM_GETMONTHDELTA les contrôles de Windows de message
topic_type:
- apiref
api_name:
- MCM_GETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c13a13d75a1655c1082b4b4611517915be14e27b0fb1c5f94fb5a17f6db973e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319609"
---
# <a name="mcm_getmonthdelta-message"></a>\_Message GETMONTHDELTA MCM

Récupère la vitesse de défilement pour un contrôle Month Calendar. La vitesse de défilement est le nombre de mois pendant lesquels le contrôle déplace son affichage lorsque l’utilisateur clique sur un bouton de défilement. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le delta du mois a été défini précédemment à l’aide du message [**MCM \_ SETMONTHDELTA**](mcm-setmonthdelta.md) , retourne une valeur int qui représente la vitesse de défilement actuelle du calendrier du mois. Si le delta du mois n’a pas été défini précédemment à l’aide du message **MCM \_ SETMONTHDELTA** ou si le delta du mois a été réinitialisé à la valeur par défaut, retourne une valeur int qui représente le nombre actuel de mois visibles.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





