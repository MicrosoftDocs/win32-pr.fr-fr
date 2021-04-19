---
title: Styles de contrôles communs (CommCtrl. h)
description: Cette section répertorie les styles de contrôle courants. Sauf indication contraire, ces styles s’appliquent aux contrôles rebar, aux contrôles ToolBar et aux fenêtres d’État.
ms.assetid: aab0cd68-ede7-474b-8695-c75805669716
topic_type:
- apiref
api_name:
- CCS_ADJUSTABLE
- CCS_BOTTOM
- CCS_LEFT
- CCS_NODIVIDER
- CCS_NOMOVEX
- CCS_NOMOVEY
- CCS_NOPARENTALIGN
- CCS_NORESIZE
- CCS_RIGHT
- CCS_TOP
- CCS_VERT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1a50b28a95d94a97da2fb6ac3522dbc568af111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528726"
---
# <a name="common-control-styles"></a>Styles de contrôles communs

Cette section répertorie les styles de contrôle courants. Sauf indication contraire, ces styles s’appliquent aux contrôles rebar, aux contrôles ToolBar et aux fenêtres d’État.



| Constante                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CCS_ADJUSTABLE"></span><span id="ccs_adjustable"></span><dl> <dt>**\_ajustable CCS**</dt> </dl>          | Active les fonctionnalités de personnalisation intégrées d’une barre d’outils, qui permettent à l’utilisateur de faire glisser un bouton vers une nouvelle position ou de supprimer un bouton en le faisant glisser en dehors de la barre d’outils. En outre, l’utilisateur peut double-cliquer sur la barre d’outils pour afficher la boîte de dialogue **personnaliser la barre** d’outils, qui permet à l’utilisateur d’ajouter, de supprimer et de réorganiser les boutons de la barre d’outils.<br/> |
| <span id="CCS_BOTTOM"></span><span id="ccs_bottom"></span><dl> <dt>**CCS en \_ bas**</dt> </dl>                      | Fait en sorte que le contrôle se positionne en bas de la zone cliente de la fenêtre parente et affecte à la largeur la même que la largeur de la fenêtre parente. Les fenêtres d’État ont ce style par défaut.<br/>                                                                                                                                          |
| <span id="CCS_LEFT"></span><span id="ccs_left"></span><dl> <dt>**CCS \_ gauche**</dt> </dl>                            | [Version 4,70](common-controls-intro.md). Fait en sorte que le contrôle s’affiche verticalement sur le côté gauche de la fenêtre parente.<br/>                                                                                                                                                                                                            |
| <span id="CCS_NODIVIDER"></span><span id="ccs_nodivider"></span><dl> <dt>**CCS \_ diviseur**</dt> </dl>             | Empêche une mise en surbrillance à deux pixels d’être dessinée en haut du contrôle. <br/>                                                                                                                                                                                                                                                                |
| <span id="CCS_NOMOVEX"></span><span id="ccs_nomovex"></span><dl> <dt>**CCS \_ NOMOVEX**</dt> </dl>                   | [Version 4,70](common-controls-intro.md). Fait en sorte que le contrôle se redimensionne et se déplace verticalement, mais pas horizontalement, en réponse à un message de [**\_ taille WM**](/windows/desktop/winmsg/wm-size) . Si CCS \_ NORESIZE est utilisé, ce style ne s’applique pas.<br/>                                                                                                    |
| <span id="CCS_NOMOVEY"></span><span id="ccs_nomovey"></span><dl> <dt>**CCS \_ NOdéplacement**</dt> </dl>                   | Fait en sorte que le contrôle se redimensionne et se déplace horizontalement, mais pas verticalement, en réponse à un message de [**\_ taille WM**](/windows/desktop/winmsg/wm-size) . Si CCS \_ NORESIZE est utilisé, ce style ne s’applique pas. Les fenêtres d’en-tête ont ce style par défaut.<br/>                                                                                                    |
| <span id="CCS_NOPARENTALIGN"></span><span id="ccs_noparentalign"></span><dl> <dt>**CCS \_ NOPARENTALIGN**</dt> </dl> | Empêche le contrôle de se déplacer automatiquement en haut ou en bas de la fenêtre parente. Au lieu de cela, le contrôle conserve sa position dans la fenêtre parente malgré les modifications apportées à la taille du parent. Si CCS \_ Top ou CCS \_ Bottom est également utilisé, la hauteur est ajustée à la valeur par défaut, mais la position et la largeur restent inchangées. <br/>        |
| <span id="CCS_NORESIZE"></span><span id="ccs_noresize"></span><dl> <dt>**CCS \_ NORESIZE**</dt> </dl>                | Empêche le contrôle d’utiliser la largeur et la hauteur par défaut lors de la définition de sa taille initiale ou d’une nouvelle taille. Au lieu de cela, le contrôle utilise la largeur et la hauteur spécifiées dans la demande de création ou de dimensionnement. <br/>                                                                                                                                 |
| <span id="CCS_RIGHT"></span><span id="ccs_right"></span><dl> <dt>**CCS \_ droite**</dt> </dl>                         | [Version 4,70](common-controls-intro.md). Fait en sorte que le contrôle s’affiche verticalement sur le côté droit de la fenêtre parente.<br/>                                                                                                                                                                                                           |
| <span id="CCS_TOP"></span><span id="ccs_top"></span><dl> <dt>**CCS \_ haut**</dt> </dl>                               | Fait en sorte que le contrôle se positionne en haut de la zone cliente de la fenêtre parente et affecte à la largeur la même que la largeur de la fenêtre parente. Les barres d’outils ont ce style par défaut. <br/>                                                                                                                                                  |
| <span id="CCS_VERT"></span><span id="ccs_vert"></span><dl> <dt>**CCS \_ vert**</dt> </dl>                            | [Version 4,70](common-controls-intro.md). Provoque l’affichage vertical du contrôle.<br/>                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Notes

Les rubriques suivantes décrivent des styles de contrôle supplémentaires :

-   [**Styles de contrôle d’animation**](animation-control-styles.md)
-   [**Styles de bouton**](button-styles.md)
-   [**Styles de zone de liste déroulante**](combo-box-styles.md)
-   [**Styles étendus de contrôle ComboBoxEx**](comboboxex-control-extended-styles.md)
-   [**Styles de contrôle de sélecteur de date et d’heure**](date-and-time-picker-control-styles.md)
-   [**Modifier les styles de contrôle**](edit-control-styles.md)
-   [**Styles de contrôle d’en-tête**](header-control-styles.md)
-   [**Styles de zone de liste**](list-box-styles.md)
-   [**Styles de fenêtre d’affichage de liste**](list-view-window-styles.md)
-   [**Styles du contrôle calendrier du mois**](month-calendar-control-styles.md)
-   [**Styles de contrôle de pagineur**](pager-control-styles.md)
-   [**Styles de contrôle de barre de progression**](progress-bar-control-styles.md)
-   [**Styles de contrôle rebar**](rebar-control-styles.md)
-   [**Styles de contrôle RichEdit**](rich-edit-control-styles.md)
-   [**Styles de contrôle de barre de défilement**](scroll-bar-control-styles.md)
-   [Styles de contrôle statiques](static-control-styles.md)
-   [**Styles de barre d’État**](status-bar-styles.md)
-   [**Styles de contrôle SysLink**](syslink-control-styles.md)
-   [**Styles du contrôle onglet**](tab-control-styles.md)
-   [**Styles de contrôle et de bouton de barre d’outils**](toolbar-control-and-button-styles.md)
-   [**Styles d’info-bulle**](tooltip-styles.md)
-   [**Styles de contrôle TrackBar**](trackbar-control-styles.md)
-   [**Styles de fenêtre de contrôle d’arborescence**](tree-view-control-window-styles.md)
-   [**Styles de contrôle up-up**](up-down-control-styles.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

