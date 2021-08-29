---
title: Message TCM_SETMINTABWIDTH (commctrl. h)
description: Définit la largeur minimale des éléments dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetMinTabWidth.
ms.assetid: c0be3d4e-774c-4233-820f-01ffbb69ecf0
keywords:
- TCM_SETMINTABWIDTH les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TCM_SETMINTABWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1136afa6952c30c51b619636e938b7887cd9dcf55da8d3f2d9c585ba9e1d82c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104699"
---
# <a name="tcm_setmintabwidth-message"></a>\_Message SETMINTABWIDTH TCM

Définit la largeur minimale des éléments dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ SetMinTabWidth**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Largeur minimale à définir pour un élément de contrôle d’onglet. Si ce paramètre a la valeur-1, le contrôle utilise la largeur d’onglet par défaut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur INT qui représente la largeur d’onglet minimale précédente.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





