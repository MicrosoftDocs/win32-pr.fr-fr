---
title: Message MCM_SETMONTHDELTA (commctrl. h)
description: Définit la vitesse de défilement pour un contrôle Month Calendar. La vitesse de défilement est le nombre de mois pendant lesquels le contrôle déplace son affichage lorsque l’utilisateur clique sur un bouton de défilement. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SetMonthDelta.
ms.assetid: 2d01b95f-3be8-4548-80b5-ac01d3e49e9f
keywords:
- MCM_SETMONTHDELTA les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_SETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 123eddb55a7ee8ddf8e3f6d8136e9ee57dfc8681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513827"
---
# <a name="mcm_setmonthdelta-message"></a>\_Message SETMONTHDELTA MCM

Définit la vitesse de défilement pour un contrôle Month Calendar. La vitesse de défilement est le nombre de mois pendant lesquels le contrôle déplace son affichage lorsque l’utilisateur clique sur un bouton de défilement. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur représentant le nombre de mois à définir comme taux de défilement du contrôle. Si cette valeur est égale à zéro, le delta du mois est rétabli à la valeur par défaut, qui est le nombre de mois affichés dans le contrôle.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur INT qui représente la vitesse de défilement précédente. Si la vitesse de défilement n’a pas été définie précédemment, la valeur de retour est zéro.

## <a name="remarks"></a>Notes

Les touches PAGE précédente et PAGE suivante, VK \_ avant et VK \_ suivant, modifient le mois sélectionné d’une unité, quel que soit le nombre de mois affichés ou la valeur définie par **MCM \_ SETMONTHDELTA**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





