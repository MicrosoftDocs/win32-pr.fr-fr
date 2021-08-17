---
title: Constantes TF_LBI_STYLE_ (Ctfutb. h)
description: Les \_ \_ constantes TF IFA style \_ \ sont utilisées dans le membre dwStyle de la \_ structure TF LANGBARITEMINFO pour spécifier le style d’un élément de la barre de langue.
ms.assetid: 9180a666-774f-401b-bea3-68d5396fab30
topic_type:
- apiref
api_name:
- TF_LBI_STYLE_HIDDENSTATUSCONTROL
- TF_LBI_STYLE_SHOWNINTRAY
- TF_LBI_STYLE_HIDEONNOOTHERITEMS
- TF_LBI_STYLE_SHOWNINTRAYONLY
- TF_LBI_STYLE_HIDDENBYDEFAULT
- TF_LBI_STYLE_TEXTCOLORICON
- TF_LBI_STYLE_BTN_BUTTON
- TF_LBI_STYLE_BTN_MENU
- TF_LBI_STYLE_BTN_TOGGLE
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9954c416d9ad28f0ba0b2ddd6853b125039bf4db24adb3b3ff41f8722b2ba494
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950794"
---
# <a name="tf_lbi_style_-constants"></a>\_ \_ Constantes de style IFA \_ de l’TF \*

Les **\_ \_ constantes TF IFA style \_ \* *_ sont utilisées dans le membre _* dwStyle** de la structure [tf \_ LANGBARITEMINFO](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo) pour spécifier le style d’un élément de la barre de langue.

Si ce style est combiné avec \_ \_ le bouton TF IFA style \_ BTN \_ , une flèche de déroulement s’affiche pour l’élément en plus du texte. La flèche déroulante fonctionne comme un bouton de menu et son clic entraîne l’appel de **ITfLangBarItemButton :: InitMenu** . Le fait de cliquer sur la partie texte du bouton entraîne l’appel de **ITfLangBarItemButton :: OnClick** .



| Constante/valeur                                                                                                                                                                                                                                                                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STYLE_HIDDENSTATUSCONTROL"></span><span id="tf_lbi_style_hiddenstatuscontrol"></span><dl> <dt>**Tf \_ \_ \_ HIDDENSTATUSCONTROL style IFA**</dt> <dt>0x00000001</dt> </dl> | L’élément peut être masqué ou affiché de manière dynamique à l’aide de la \_ \_ valeur du statut masqué TF IFA \_ dans la méthode [ITfLangBarItem :: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) . Si cette valeur n’est pas présente, l’élément ne peut pas être masqué de cette manière.<br/>                                                                                                                                                                                                                                                                         |
| <span id="TF_LBI_STYLE_SHOWNINTRAY"></span><span id="tf_lbi_style_shownintray"></span><dl> <dt>**Tf \_ \_ \_ SHOWNINTRAY de style IFA**</dt> <dt>0x00000002</dt> </dl>                         | L’élément s’affiche dans la barre d’état des icônes de notification en plus de la barre de langue. Cet indicateur n’est pas pris en charge actuellement.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="TF_LBI_STYLE_HIDEONNOOTHERITEMS"></span><span id="tf_lbi_style_hideonnootheritems"></span><dl> <dt>**Tf \_ \_Style IFA \_ HIDEONNOOTHERITEMS**</dt> <dt>0x00000004</dt> </dl>    | La barre de langue est masquée si tous les éléments de la barre de langue contiennent ce style. Si un élément de la barre de langue ne contient pas ce style, la barre de langue s’affiche.<br/>                                                                                                                                                                                                                                                                                                                                  |
| <span id="TF_LBI_STYLE_SHOWNINTRAYONLY"></span><span id="tf_lbi_style_shownintrayonly"></span><dl> <dt>**Tf \_ \_ \_ SHOWNINTRAYONLY de style IFA**</dt> <dt>0x00000008</dt> </dl>             | L’élément s’affiche uniquement dans la barre d’état des icônes de notification et non dans la barre de langue. Cet indicateur n’est pas pris en charge actuellement.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="TF_LBI_STYLE_HIDDENBYDEFAULT"></span><span id="tf_lbi_style_hiddenbydefault"></span><dl> <dt>**Tf \_ \_ \_ HIDDENBYDEFAULT de style IFA**</dt> <dt>0x00000010</dt> </dl>             | L’élément n’est pas affiché dans la barre d’outils tant qu’il n’est pas sélectionné dans le menu options de la barre de langue. Cet indicateur est ignoré si le \_ HIDDENSTATUSCONTROL de \_ style IFA TF \_ est défini ou si l’utilisateur a déjà modifié l’état masqué/affiché à l’aide du menu options de la barre de langue.<br/>                                                                                                                                                                                                                                         |
| <span id="TF_LBI_STYLE_TEXTCOLORICON"></span><span id="tf_lbi_style_textcoloricon"></span><dl> <dt>**Tf \_ \_Style IFA \_ TEXTCOLORICON**</dt> <dt>0x00000020</dt> </dl>                   | Tout pixel noir au sein de l’icône sera converti dans la couleur du texte du thème sélectionné. L’icône doit être monochrome.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="TF_LBI_STYLE_BTN_BUTTON"></span><span id="tf_lbi_style_btn_button"></span><dl> <dt>**Tf \_ \_ \_ \_ Bouton de style IFA BTN**</dt> <dt>0x00010000</dt> </dl>                           | L’élément est un bouton de commande. [ITfLangBarItemButton :: OnClick](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onclick) est appelé lorsque l’élément est enfoncé.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="TF_LBI_STYLE_BTN_MENU"></span><span id="tf_lbi_style_btn_menu"></span><dl> <dt>**Tf \_ \_ \_ \_ Menu de style IFA BTN**</dt> <dt>0x00020000</dt> </dl>                                 | L’élément est un menu. [ITfLangBarItemButton :: InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu) est appelé lorsque l’élément est enfoncé.<br/> Si ce style est combiné avec \_ \_ le bouton TF IFA style \_ BTN \_ , une flèche de déroulement s’affiche pour l’élément en plus du texte. La flèche déroulante fonctionne comme un bouton de menu et son clic entraîne l’appel de **ITfLangBarItemButton :: InitMenu** . Le fait de cliquer sur la partie texte du bouton entraîne l’appel de **ITfLangBarItemButton :: OnClick** .<br/> |
| <span id="TF_LBI_STYLE_BTN_TOGGLE"></span><span id="tf_lbi_style_btn_toggle"></span><dl> <dt>**Tf \_ \_Style IFA \_ BTN \_ basculer**</dt> <dt>0x00040000</dt> </dl>                           | L’élément est un bouton bascule qui fonctionne de la même manière qu’une case à cocher. **ITfLangBarItemButton :: OnClick** est appelé lorsque l’élément est enfoncé.<br/>                                                                                                                                                                                                                                                                                                                                                                       |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 Professional<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Ctfutb. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Ctfutb. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[TF \_ LANGBARITEMINFO](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> <dt>

[ITfLangBarItem :: GetInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getinfo)
</dt> <dt>

[ITfLangBarItem :: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





