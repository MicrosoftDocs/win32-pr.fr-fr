---
title: Styles du contrôle Month Calendar (CommCtrl. h)
description: Les constantes de style suivantes sont utilisées lors de la création de contrôles Month Calendar.
ms.assetid: 8d9b2239-fd13-4579-81a2-0385fd318e83
topic_type:
- apiref
api_name:
- MCS_DAYSTATE
- MCS_MULTISELECT
- MCS_WEEKNUMBERS
- MCS_NOTODAYCIRCLE
- MCS_NOTODAY
- MCS_NOTRAILINGDATES
- MCS_SHORTDAYSOFWEEK
- MCS_NOSELCHANGEONNAV
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45ccef4a3cc8e16851c0676b8b0dce8c53cfdd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528094"
---
# <a name="month-calendar-control-styles"></a>Styles du contrôle calendrier du mois

Les constantes de style suivantes sont utilisées lors de la création de contrôles Month Calendar.



| Constante                                                                                                                                                                           | Description                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_DAYSTATE"></span><span id="mcs_daystate"></span><dl> <dt>**\_DAYSTATE MCS**</dt> </dl>                         | [Version 4,70](common-control-versions.md). Le calendrier du mois envoie des notifications [ \_ GETDAYSTATE MCN](mcn-getdaystate.md) pour demander des informations sur les jours qui doivent s’afficher en gras.<br/>                                                                                                          |
| <span id="MCS_MULTISELECT"></span><span id="mcs_multiselect"></span><dl> <dt>**MCS \_ MULTIselect**</dt> </dl>                | [Version 4,70](common-control-versions.md). Le calendrier du mois permet à l’utilisateur de sélectionner une plage de dates dans le contrôle. Par défaut, la plage maximale est d’une semaine. Vous pouvez modifier la plage maximale pouvant être sélectionnée à l’aide du message [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) . <br/> |
| <span id="MCS_WEEKNUMBERS"></span><span id="mcs_weeknumbers"></span><dl> <dt>**\_WEEKNUMBERS MCS**</dt> </dl>                | [Version 4,70](common-control-versions.md). Le contrôle Month Calendar affiche les numéros de semaine (1-52) à gauche de chaque ligne de jours. La semaine 1 est définie comme la première semaine qui contient au moins quatre jours. <br/>                                                                                              |
| <span id="MCS_NOTODAYCIRCLE"></span><span id="mcs_notodaycircle"></span><dl> <dt>**\_NOTODAYCIRCLE MCS**</dt> </dl>          | [Version 4,70](common-control-versions.md). Le contrôle Month Calendar n’entoure pas la date « today ». <br/>                                                                                                                                                                                                |
| <span id="MCS_NOTODAY"></span><span id="mcs_notoday"></span><dl> <dt>**MCS \_ NOaujourd’hui**</dt> </dl>                            | [Version 4,70](common-control-versions.md). Le contrôle Month Calendar n’affiche pas la date « today » en bas du contrôle. <br/>                                                                                                                                                                   |
| <span id="MCS_NOTRAILINGDATES"></span><span id="mcs_notrailingdates"></span><dl> <dt>**\_NOTRAILINGDATES MCS**</dt> </dl>    | **Windows Vista.** Les dates des mois précédents et suivants ne sont pas affichées dans le calendrier du mois en cours.<br/>                                                                                                                                                                                              |
| <span id="MCS_SHORTDAYSOFWEEK"></span><span id="mcs_shortdaysofweek"></span><dl> <dt>**\_SHORTDAYSOFWEEK MCS**</dt> </dl>    | **Windows Vista.** Les noms de jours courts s’affichent dans l’en-tête.<br/>                                                                                                                                                                                                                                            |
| <span id="MCS_NOSELCHANGEONNAV"></span><span id="mcs_noselchangeonnav"></span><dl> <dt>**\_NOSELCHANGEONNAV MCS**</dt> </dl> | **Windows Vista.** La sélection n’est pas modifiée lorsque l’utilisateur navigue vers le haut ou vers le haut dans le calendrier. Cela permet à l’utilisateur de sélectionner une plage supérieure à celle qui est visible.<br/>                                                                                                                                  |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





