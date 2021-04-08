---
title: Message MCM_HITTEST (commctrl. h)
description: Détermine la partie d’un contrôle calendrier du mois qui se trouve à un point donné sur l’écran. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal HitTest.
ms.assetid: 51e74b07-4ed7-488d-ad5d-116f046577fc
keywords:
- MCM_HITTEST les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3670ac8ab663ceda1786f7136a50c4da255a76c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740285"
---
# <a name="mcm_hittest-message"></a>\_Message MCM HITTEST

Détermine la partie d’un contrôle calendrier du mois qui se trouve à un point donné sur l’écran. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_hittest) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) . Lors de l’envoi du message, le membre **cbSize** doit être défini sur la taille de la structure **MCHITTESTINFO** et **PT** doit être défini sur le point sur lequel vous souhaitez effectuer un test de positionnement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Définit des valeurs dans les membres du



| Code de retour                                                                                           | Description                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_calendrier MCHT**</dt> </dl>         | Le point donné était dans le calendrier.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>**MCHT \_ CALENDARBK**</dt> </dl>       | Le point donné se trouvait dans l’arrière-plan du calendrier.<br/>                                                                                                                                                                                                              |
| <dl> <dt>**MCHT \_ CALENDARDATE**</dt> </dl>     | Le point donné était à une date particulière dans le calendrier. La structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) au niveau de *lParam->St* est définie sur la date au point donné.<br/>                                                                                    |
| <dl> <dt>**MCHT \_ CALENDARDATENEXT**</dt> </dl> | Le point donné se trouvait au-dessus d’une date du mois suivant (affiché partiellement à la fin du mois affiché actuellement). Si l’utilisateur clique ici, le calendrier du mois défile vers le mois ou l’ensemble de mois suivant.<br/>                                 |
| <dl> <dt>**MCHT \_ CALENDARDATEPREV**</dt> </dl> | Le point donné se trouvait au-dessus d’une date du mois précédent (affiché partiellement à la fin du mois affiché actuellement). Si l’utilisateur clique ici, le calendrier du mois défile vers le mois ou l’ensemble de mois précédent.<br/>                         |
| <dl> <dt>**MCHT, \_ CALENDARDAY**</dt> </dl>      | Le point donné était au-dessus d’une abréviation de jour (« Ven », par exemple). La structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) au niveau de *lParam->St* est définie sur la date correspondante dans la ligne du haut.<br/>                                                                      |
| <dl> <dt>**MCHT \_ CALENDARWEEKNUM**</dt> </dl>  | Le point donné était supérieur à un numéro de semaine (uniquement le style [**MCS \_ WEEKNUMBERS**](month-calendar-control-styles.md) ). La structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) au niveau de *lParam->St* est définie sur la date correspondante dans la colonne la plus à gauche.<br/> |
| <dl> <dt>**MCHT \_ suivant**</dt> </dl>             | Le point donné se trouve dans une zone qui fait en sorte que le calendrier du mois défile vers le mois ou l’ensemble de mois suivant. Cet indicateur est utilisé pour modifier d’autres indicateurs de test de positionnement.<br/>                                                                                   |
| <dl> <dt>**MCHT \_ nulle**</dt> </dl>          | Le point donné n’était pas sur le contrôle Month Calendar, ou il était dans une partie inactive du contrôle.<br/>                                                                                                                                                        |
| <dl> <dt>**MCHT \_ préc**</dt> </dl>             | Le point donné se trouve dans une zone qui fera en sorte que le calendrier du mois défile vers le mois ou l’ensemble de mois précédent. Cet indicateur est utilisé pour modifier d’autres indicateurs de test de positionnement.<br/>                                                                               |
| <dl> <dt>**\_titre MCHT**</dt> </dl>            | Le point donné était sur le titre d’un mois.<br/>                                                                                                                                                                                                                      |
| <dl> <dt>**MCHT \_ TITLEBK**</dt> </dl>          | Le point donné se trouve au-dessus de l’arrière-plan du titre d’un mois.<br/>                                                                                                                                                                                                    |
| <dl> <dt>**MCHT \_ TITLEBTNNEXT**</dt> </dl>     | Le point donné était sur le bouton situé dans le coin supérieur droit du contrôle. Si l’utilisateur clique ici, le calendrier du mois défile vers le mois ou l’ensemble de mois suivant. <br/>                                                                           |
| <dl> <dt>**MCHT \_ TITLEBTNPREV**</dt> </dl>     | Le point donné était sur le bouton situé dans le coin supérieur gauche du contrôle. Si l’utilisateur clique ici, le calendrier du mois défile vers le mois ou l’ensemble de mois précédent. <br/>                                                                        |
| <dl> <dt>**MCHT \_ TITLEMONTH**</dt> </dl>       | Le point donné était dans la barre de titre d’un mois, sur un nom de mois.<br/>                                                                                                                                                                                                 |
| <dl> <dt>**MCHT \_ TITLEYEAR**</dt> </dl>        | Le point donné se trouvait dans la barre de titre d’un mois, sur la valeur de l’année.<br/>                                                                                                                                                                                               |
| <dl> <dt>**MCHT \_ TODAYLINK**</dt> </dl>        | Le point donné était sur le lien « aujourd’hui » en bas du contrôle Month Calendar.<br/> Le membre **uHit** de la structure [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) à *lParam* est égal à la valeur de retour. <br/>                                          |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

