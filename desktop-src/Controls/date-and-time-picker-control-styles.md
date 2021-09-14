---
title: Styles de contrôle de sélecteur de date et d’heure (CommCtrl. h)
description: Les styles de fenêtre répertoriés ici sont spécifiques aux contrôles de sélecteur de date et d’heure.
ms.assetid: d3b95521-75ef-4cca-b801-94c6f749aa47
topic_type:
- apiref
api_name:
- DTS_APPCANPARSE
- DTS_LONGDATEFORMAT
- DTS_RIGHTALIGN
- DTS_SHOWNONE
- DTS_SHORTDATEFORMAT
- DTS_SHORTDATECENTURYFORMAT
- DTS_TIMEFORMAT
- DTS_UPDOWN
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d24e7543e4e843fc70e0ccacdab670e18e46cf3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127124121"
---
# <a name="date-and-time-picker-control-styles"></a>Styles de contrôle de sélecteur de date et d’heure

Les styles de fenêtre répertoriés ici sont spécifiques aux contrôles de sélecteur de date et d’heure.



| Constante                                                                                                                                                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DTS_APPCANPARSE"></span><span id="dts_appcanparse"></span><dl> <dt>**\_APPCANPARSE Dts**</dt> </dl>                                  | Permet au propriétaire d’analyser l’entrée d’utilisateur et de prendre les mesures nécessaires. Elle permet aux utilisateurs de modifier dans la zone cliente du contrôle lorsqu’ils appuient sur la touche F2. Le contrôle envoie des codes de notification [DTN \_ USERSTRING](dtn-userstring.md) lorsque les utilisateurs sont terminés.<br/>                                                                                                                                                                                                                                                                    |
| <span id="DTS_LONGDATEFORMAT"></span><span id="dts_longdateformat"></span><dl> <dt>**\_LONGDATEFORMAT Dts**</dt> </dl>                         | Affiche la date au format long. La chaîne de format par défaut pour ce style est définie par les paramètres régionaux \_ SLONGDATEFORMAT, ce qui produit une sortie comme « vendredi 19 avril 1996 ». Quand ce style est utilisé, le bouton déroulant n’affiche pas d’icône.<br/>                                                                                                                                                                                                                                                                                     |
| <span id="DTS_RIGHTALIGN"></span><span id="dts_rightalign"></span><dl> <dt>**\_RIGHTALIGN Dts**</dt> </dl>                                     | Le calendrier du mois déroulant sera aligné à droite avec le contrôle au lieu de aligné à gauche, ce qui correspond à la valeur par défaut. <br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DTS_SHOWNONE"></span><span id="dts_shownone"></span><dl> <dt>**\_SHOWNONE Dts**</dt> </dl>                                           | Il est possible de n’avoir aucune date actuellement sélectionnée dans le contrôle. Avec ce style, le contrôle affiche une case à cocher qui est automatiquement sélectionnée chaque fois qu’une date est prélevée ou entrée. Si la case à cocher est désélectionnée par la suite, l’application ne peut pas récupérer la date du contrôle, car, par essence, le contrôle n’a pas de date. L’état de la case à cocher peut être défini avec le message [**DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md) ou interrogé avec le message [**DTM \_ GETSYSTEMTIME**](dtm-getsystemtime.md) .<br/> |
| <span id="DTS_SHORTDATEFORMAT"></span><span id="dts_shortdateformat"></span><dl> <dt>**\_SHORTDATEFORMAT Dts**</dt> </dl>                      | Affiche la date au format abrégé. La chaîne de format par défaut pour ce style est définie par les paramètres régionaux \_ SSHORTDATE, ce qui produit une sortie comme « 4/19/96 ».<br/>                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DTS_SHORTDATECENTURYFORMAT"></span><span id="dts_shortdatecenturyformat"></span><dl> <dt>**\_SHORTDATECENTURYFORMAT Dts**</dt> </dl> | **Version 5,80.** Semblable au style **DTS \_ SHORTDATEFORMAT** , sauf que year est un champ à quatre chiffres. La chaîne de format par défaut pour ce style est basée sur les paramètres régionaux \_ SSHORTDATE. La sortie ressemble à ceci : « 4/19/1996 ».<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="DTS_TIMEFORMAT"></span><span id="dts_timeformat"></span><dl> <dt>**DTS \_ TimeFormat**</dt> </dl>                                     | Affiche l’heure. La chaîne de format par défaut pour ce style est définie par les paramètres régionaux \_ sTimeFormat par, ce qui produit une sortie comme « 5:31:42 PM ».<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="DTS_UPDOWN"></span><span id="dts_updown"></span><dl> <dt>**déverrouillage DTS \_**</dt> </dl>                                                 | Place un contrôle up-out à droite du contrôle PAO pour modifier les valeurs de date et d’heure. Ce style peut être utilisé à la place du calendrier du mois déroulant, qui est le style par défaut.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="remarks"></a>Notes

Les \_ styles XXXFORMAT DTS qui définissent le format d’affichage ne peuvent pas être combinés. Si aucun des styles de mise en forme ne convient, utilisez un message [**DTM \_ SETFORMAT**](dtm-setformat.md) pour définir un format personnalisé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





