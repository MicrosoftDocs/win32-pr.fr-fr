---
title: Styles de contrôle d’onglet (CommCtrl. h)
description: Cette section répertorie les styles de contrôle onglets pris en charge.
ms.assetid: a01a6609-b02e-4ada-afa0-ed5ad8dde0d6
topic_type:
- apiref
api_name:
- TCS_BOTTOM
- TCS_BUTTONS
- TCS_FIXEDWIDTH
- TCS_FLATBUTTONS
- TCS_FOCUSNEVER
- TCS_FOCUSONBUTTONDOWN
- TCS_FORCEICONLEFT
- TCS_FORCELABELLEFT
- TCS_HOTTRACK
- TCS_MULTILINE
- TCS_MULTISELECT
- TCS_OWNERDRAWFIXED
- TCS_RAGGEDRIGHT
- TCS_RIGHT
- TCS_RIGHTJUSTIFY
- TCS_SCROLLOPPOSITE
- TCS_SINGLELINE
- TCS_TABS
- TCS_TOOLTIPS
- TCS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 352864fe71b5efc39529109bafb3bdc49cee68e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530495"
---
# <a name="tab-control-styles"></a>Styles du contrôle onglet

Cette section répertorie les styles de contrôle onglets pris en charge.



| Constante                                                                                                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_BOTTOM"></span><span id="tcs_bottom"></span><dl> <dt>**TC en \_ bas**</dt> </dl>                                  | [Version 4,70](common-control-versions.md). Les onglets s’affichent en bas du contrôle. Cette valeur est égale à TCS \_ Right. Ce style n’est pas pris en charge si vous utilisez ComCtl32.dll version 6.<br/>                                                                                                                                                                 |
| <span id="TCS_BUTTONS"></span><span id="tcs_buttons"></span><dl> <dt>**\_boutons TCS**</dt> </dl>                               | Les onglets s’affichent sous forme de boutons et aucune bordure n’est dessinée autour de la zone d’affichage.<br/>                                                                                                                                                                                                                                                                             |
| <span id="TCS_FIXEDWIDTH"></span><span id="tcs_fixedwidth"></span><dl> <dt>**TC \_ FIXEDWIDTH**</dt> </dl>                      | Tous les onglets ont la même largeur. Ce style ne peut pas être combiné avec le \_ style RIGHTJUSTIFY TCS.<br/>                                                                                                                                                                                                                                                        |
| <span id="TCS_FLATBUTTONS"></span><span id="tcs_flatbuttons"></span><dl> <dt>**\_FLATBUTTONS TCS**</dt> </dl>                   | [Version 4,71](common-control-versions.md). Les onglets sélectionnés apparaissent comme étant mis en retrait en arrière-plan, tandis que les autres onglets s’affichent sur le même plan que l’arrière-plan. Ce style affecte uniquement les contrôles onglet avec le \_ style boutons TCS.<br/>                                                                                                     |
| <span id="TCS_FOCUSNEVER"></span><span id="tcs_focusnever"></span><dl> <dt>**\_FOCUSNEVER TCS**</dt> </dl>                      | Le contrôle onglet ne reçoit pas le focus d’entrée lorsque l’utilisateur clique dessus.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="TCS_FOCUSONBUTTONDOWN"></span><span id="tcs_focusonbuttondown"></span><dl> <dt>**\_FOCUSONBUTTONDOWN TCS**</dt> </dl> | Le contrôle onglet reçoit le focus d’entrée lorsque l’utilisateur clique dessus.<br/>                                                                                                                                                                                                                                                                                              |
| <span id="TCS_FORCEICONLEFT"></span><span id="tcs_forceiconleft"></span><dl> <dt>**\_FORCEICONLEFT TCS**</dt> </dl>             | Les icônes sont alignées sur le bord gauche de chaque onglet à largeur fixe. Ce style ne peut être utilisé qu’avec le style de la fonction TCS \_ .<br/>                                                                                                                                                                                                                           |
| <span id="TCS_FORCELABELLEFT"></span><span id="tcs_forcelabelleft"></span><dl> <dt>**\_FORCELABELLEFT TCS**</dt> </dl>          | Les étiquettes sont alignées sur le bord gauche de chaque onglet à largeur fixe. autrement dit, l’étiquette s’affiche immédiatement à droite de l’icône au lieu d’être centrée. Ce style ne peut être utilisé qu’avec le \_ style des TCS et le style TCS \_ FORCEICONLEFT.<br/>                                                                             |
| <span id="TCS_HOTTRACK"></span><span id="tcs_hottrack"></span><dl> <dt>**\_HOTTRACK TCS**</dt> </dl>                            | [Version 4,70](common-control-versions.md). Les éléments sous le pointeur sont automatiquement mis en surbrillance. Vous pouvez vérifier si le suivi actif est activé en appelant [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). <br/>                                                                                                                              |
| <span id="TCS_MULTILINE"></span><span id="tcs_multiline"></span><dl> <dt>**\_multiligne TCS**</dt> </dl>                         | Plusieurs lignes d’onglets sont affichées, si nécessaire, tous les onglets sont visibles à la fois.<br/>                                                                                                                                                                                                                                                                 |
| <span id="TCS_MULTISELECT"></span><span id="tcs_multiselect"></span><dl> <dt>**multisélection TCS \_**</dt> </dl>                   | [Version 4,70](common-control-versions.md). Vous pouvez sélectionner plusieurs onglets en maintenant la touche CTRL enfoncée lorsque vous cliquez dessus. Ce style doit être utilisé avec le \_ style de boutons TCS.<br/>                                                                                                                                                                         |
| <span id="TCS_OWNERDRAWFIXED"></span><span id="tcs_ownerdrawfixed"></span><dl> <dt>**\_OWNERDRAWFIXED TCS**</dt> </dl>          | La fenêtre parente est chargée de dessiner les onglets.<br/>                                                                                                                                                                                                                                                                                                  |
| <span id="TCS_RAGGEDRIGHT"></span><span id="tcs_raggedright"></span><dl> <dt>**\_RAGGEDRIGHT TCS**</dt> </dl>                   | Les lignes d’onglets ne seront pas étirées pour remplir toute la largeur du contrôle. Ce style est la valeur par défaut.<br/>                                                                                                                                                                                                                                              |
| <span id="TCS_RIGHT"></span><span id="tcs_right"></span><dl> <dt>**à \_ droite de TCS**</dt> </dl>                                     | [Version 4,70](common-control-versions.md). Les onglets s’affichent verticalement sur le côté droit des contrôles qui utilisent le \_ style vertical TCS. Cette valeur est égale à TCS \_ Bottom. Ce style n’est pas pris en charge si vous utilisez des styles visuels.<br/>                                                                                                                            |
| <span id="TCS_RIGHTJUSTIFY"></span><span id="tcs_rightjustify"></span><dl> <dt>**\_RIGHTJUSTIFY TCS**</dt> </dl>                | La largeur de chaque onglet est augmentée, si nécessaire, afin que chaque ligne d’onglets remplisse toute la largeur du contrôle onglet. Ce style de fenêtre est ignoré, sauf si le \_ style multiligne TCS est également spécifié.<br/>                                                                                                                                               |
| <span id="TCS_SCROLLOPPOSITE"></span><span id="tcs_scrollopposite"></span><dl> <dt>**\_SCROLLOPPOSITE TCS**</dt> </dl>          | [Version 4,70](common-control-versions.md). Les onglets inutiles défilent vers le côté opposé du contrôle lorsqu’un onglet est sélectionné.<br/>                                                                                                                                                                                                                       |
| <span id="TCS_SINGLELINE"></span><span id="tcs_singleline"></span><dl> <dt>**\_Singleline**</dt> </dl>                      | Une seule ligne d’onglets s’affiche. L’utilisateur peut faire défiler pour voir d’autres onglets, si nécessaire. Ce style est la valeur par défaut.<br/>                                                                                                                                                                                                                                   |
| <span id="TCS_TABS"></span><span id="tcs_tabs"></span><dl> <dt>**\_onglets TCS**</dt> </dl>                                        | Les onglets s’affichent sous forme d’onglets et une bordure est dessinée autour de la zone d’affichage. Ce style est la valeur par défaut.<br/>                                                                                                                                                                                                                                                      |
| <span id="TCS_TOOLTIPS"></span><span id="tcs_tooltips"></span><dl> <dt>**\_info-bulles TCS**</dt> </dl>                            | Le contrôle onglet est associé à un contrôle ToolTip. <br/>                                                                                                                                                                                                                                                                                          |
| <span id="TCS_VERTICAL"></span><span id="tcs_vertical"></span><dl> <dt>**\_vertical TCS**</dt> </dl>                            | [Version 4,70](common-control-versions.md). Les onglets apparaissent sur le côté gauche du contrôle, avec le texte de l’onglet affiché verticalement. Ce style est valide uniquement lorsqu’il est utilisé avec le \_ style multiligne TCS. Pour faire apparaître les onglets sur le côté droit du contrôle, utilisez également le \_ style de clic TCS. Ce style n’est pas pris en charge si vous utilisez ComCtl32.dll version 6.<br/> |



## <a name="remarks"></a>Notes

Les styles suivants peuvent être modifiés après la création du contrôle.

-   TC en \_ bas
-   \_boutons TCS
-   TC \_ FIXEDWIDTH
-   \_FLATBUTTONS TCS
-   \_FORCEICONLEFT TCS
-   \_FORCELABELLEFT TCS
-   \_multiligne TCS
-   \_OWNERDRAWFIXED TCS
-   \_RAGGEDRIGHT TCS
-   à \_ droite de TCS
-   \_vertical TCS

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

