---
title: États des boutons de barre d’outils (CommCtrl. h)
description: Cette section répertorie les États qu’un bouton de barre d’outils peut avoir.
ms.assetid: 422e0d81-bd80-45dc-b843-82fc5d5c2a9a
topic_type:
- apiref
api_name:
- TBSTATE_CHECKED
- TBSTATE_ELLIPSES
- TBSTATE_ENABLED
- TBSTATE_HIDDEN
- TBSTATE_INDETERMINATE
- TBSTATE_MARKED
- TBSTATE_PRESSED
- TBSTATE_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45262197c4432d9e3bb5c0884b3f76c986e4acfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525453"
---
# <a name="toolbar-button-states"></a>États des boutons de barre d’outils

Cette section répertorie les États qu’un bouton de barre d’outils peut avoir.



| Constante                                                                                                                                                                              | Description                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBSTATE_CHECKED"></span><span id="tbstate_checked"></span><dl> <dt>**TBSTATE \_ activé**</dt> </dl>                   | Le bouton a le style de [**\_ contrôle TBSTYLE**](toolbar-control-and-button-styles.md) et l’utilisateur clique dessus.<br/>                   |
| <span id="TBSTATE_ELLIPSES"></span><span id="tbstate_ellipses"></span><dl> <dt>**TBSTATE \_ ellipses**</dt> </dl>                | [Version 4,70](common-control-versions.md). Le texte du bouton est coupé et des points de suspension s’affichent.<br/>                                    |
| <span id="TBSTATE_ENABLED"></span><span id="tbstate_enabled"></span><dl> <dt>**TBSTATE \_ activé**</dt> </dl>                   | Le bouton accepte les entrées utilisateur. Un bouton qui n’a pas cet État est grisé.<br/>                                                           |
| <span id="TBSTATE_HIDDEN"></span><span id="tbstate_hidden"></span><dl> <dt>**TBSTATE \_ masqué**</dt> </dl>                      | Le bouton n’est pas visible et ne peut pas recevoir d’entrée d’utilisateur.<br/>                                                                                   |
| <span id="TBSTATE_INDETERMINATE"></span><span id="tbstate_indeterminate"></span><dl> <dt>**TBSTATE \_ indéterminé**</dt> </dl> | Le bouton est grisé.<br/>                                                                                                                      |
| <span id="TBSTATE_MARKED"></span><span id="tbstate_marked"></span><dl> <dt>**TBSTATE \_ marqué**</dt> </dl>                      | [Version 4,71](common-control-versions.md). Le bouton est marqué. L’interprétation d’un élément marqué dépend de l’application. <br/> |
| <span id="TBSTATE_PRESSED"></span><span id="tbstate_pressed"></span><dl> <dt>**TBSTATE \_ enfoncé**</dt> </dl>                   | L’utilisateur clique sur le bouton.<br/>                                                                                                               |
| <span id="TBSTATE_WRAP"></span><span id="tbstate_wrap"></span><dl> <dt>**\_Retour à la ligne TBSTATE**</dt> </dl>                            | Le bouton est suivi d’un saut de ligne. L’état du bouton doit également être \_ activé pour TBSTATE.<br/>                                              |



## <a name="remarks"></a>Notes

Une barre d’outils peut avoir une combinaison d’États.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





