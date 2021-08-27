---
title: Styles étendus de la barre d’outils (CommCtrl. h)
description: Cette section répertorie les styles étendus pris en charge par les contrôles ToolBar.
ms.assetid: da31dbbf-8d0a-4711-a1af-382c62e653cd
topic_type:
- apiref
api_name:
- TBSTYLE_EX_DRAWDDARROWS
- TBSTYLE_EX_HIDECLIPPEDBUTTONS
- TBSTYLE_EX_DOUBLEBUFFER
- TBSTYLE_EX_MIXEDBUTTONS
- TBSTYLE_EX_MULTICOLUMN
- TBSTYLE_EX_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e242426269d4049b913a41910d325c360886f3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476779"
---
# <a name="toolbar-extended-styles"></a>Styles étendus de la barre d’outils

Cette section répertorie les styles étendus pris en charge par les contrôles ToolBar.




| Constante | Description | 
|----------|-------------|
| <span id="TBSTYLE_EX_DRAWDDARROWS"></span><span id="tbstyle_ex_drawddarrows"></span><dl><dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt></dl> | <a href="common-control-versions.md">Version 4,71</a>. Ce style permet aux boutons d’avoir une flèche déroulante distincte. Les boutons qui ont le style <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> sont dessinés avec une flèche déroulante dans une section distincte, à droite du bouton. Si vous cliquez sur la flèche, seule la partie de la flèche du bouton est déenfoncée et le contrôle ToolBar envoie un <a href="tbn-dropdown.md">TBN_DROPDOWN</a> code de notification pour inviter l’application à afficher le menu déroulant. Si l’utilisateur clique sur la partie principale du bouton, le contrôle ToolBar envoie un message WM_COMMAND avec l’ID du bouton. L’application répond normalement en lançant la première commande dans le menu.<br /> Dans de nombreuses situations, vous pouvez souhaiter avoir uniquement certains des boutons déroulants dans une barre d’outils avec des flèches séparées. Pour ce faire, définissez le TBSTYLE_EX_DRAWDDARROWS style étendu. Donnez aux boutons qui n’ont pas de flèches séparées le style <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> . Les boutons avec ce style comporteront une flèche affichée en regard de l’image. Toutefois, la flèche n’est pas distincte et lorsqu’un utilisateur clique sur une partie du bouton, le contrôle ToolBar envoie un <a href="tbn-dropdown.md">TBN_DROPDOWN</a> code de notification. Pour éviter les problèmes de redessination, ce style doit être défini avant que le contrôle de barre d’outils ne devienne visible.<br /> | 
| <span id="TBSTYLE_EX_HIDECLIPPEDBUTTONS"></span><span id="tbstyle_ex_hideclippedbuttons"></span><dl><dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt></dl> | <a href="common-control-versions.md">Version 5,81</a>. Ce style masque les boutons partiellement découpés. L’utilisation la plus courante de ce style est pour les barres d’outils qui font partie d’un contrôle rebar. Si une bande adjacente couvre une partie d’un bouton, le bouton ne s’affiche pas. Toutefois, si la bande rebar a le style <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> , le bouton s’affiche dans le menu déroulant du Chevron. <br /> | 
| <span id="TBSTYLE_EX_DOUBLEBUFFER"></span><span id="tbstyle_ex_doublebuffer"></span><dl><dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt></dl> | <a href="common-control-versions.md">Version 6</a>. Ce style requiert la double mise en mémoire tampon de la barre d’outils. La double mise en mémoire tampon est un mécanisme qui détecte quand la barre d’outils a changé. <br /><blockquote>[!Note]<br />Comctl32.dll version 6 n’est pas redistribuable, mais elle est incluse dans Windows ou version ultérieure. Pour utiliser Comctl32.dll version 6, spécifiez-la dans un manifeste. Pour plus d’informations sur les manifestes, consultez <a href="cookbook-overview.md">activation des styles visuels</a>.</blockquote><br /> | 
| <span id="TBSTYLE_EX_MIXEDBUTTONS"></span><span id="tbstyle_ex_mixedbuttons"></span><dl><dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt></dl> | <a href="common-control-versions.md">Version 5,81</a>. Ce style vous permet de définir du texte pour tous les boutons, mais uniquement de les afficher pour ces boutons avec le style de bouton <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> . Le style de <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> doit également être défini. Normalement, lorsqu’un bouton n’affiche pas de texte, votre application doit gérer <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> ou <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> pour afficher une info-bulle. Avec le style étendu TBSTYLE_EX_MIXEDBUTTONS, le texte qui est défini mais qui n’est pas affiché sur un bouton sera automatiquement utilisé comme texte info-bulle du bouton. Votre application doit uniquement gérer TBN_GETINFOTIP ou ou TTN_GETDISPINFO si elle a besoin d’une plus grande flexibilité pour la spécification du texte d’info-bulle. <br /> | 
| <span id="TBSTYLE_EX_MULTICOLUMN"></span><span id="tbstyle_ex_multicolumn"></span><dl><dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt></dl> | <a href="common-control-versions.md">Version 5,82</a>. <strong>Destiné à un usage interne ; non recommandé pour une utilisation dans les applications.</strong> Ce style donne à la barre d’outils un orientation verticale et organise les boutons de la barre d’outils en colonnes. Les boutons s’affichent verticalement jusqu’à ce qu’un bouton ait dépassé la hauteur limite de la barre d’outils (voir <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>), puis qu’une nouvelle colonne est créée. La barre d’outils repasse les boutons de cette manière jusqu’à ce que tous les boutons soient positionnés. Pour utiliser ce style, le style de TBSTYLE_EX_VERTICAL doit également être défini. <br /><blockquote>[!Note]<br />Ce style n’est peut-être pas pris en charge dans les versions ultérieures de Comctl32.dll. En outre, ce style n’est pas défini dans commctrl. h. Ajoutez la définition suivante aux fichiers sources de votre application pour utiliser ce style : <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code></blockquote><br /> | 
| <span id="TBSTYLE_EX_VERTICAL"></span><span id="tbstyle_ex_vertical"></span><dl><dt><strong>TBSTYLE_EX_VERTICAL</strong></dt></dl> | <a href="common-control-versions.md">Version 5,82</a>. <strong>Destiné à un usage interne ; non recommandé pour une utilisation dans les applications.</strong> Ce style donne une orientation verticale à la barre d’outils. Les boutons de la barre d’outils se déplacent de haut en bas et non horizontalement. <br /><blockquote>[!Note]<br />Ce style n’est peut-être pas pris en charge dans les versions ultérieures de Comctl32.dll. En outre, ce style n’est pas défini dans commctrl. h. Ajoutez la définition suivante aux fichiers sources de votre application pour utiliser ce style : <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code></blockquote><br /> | 




## <a name="remarks"></a>Remarques

Pour définir un style étendu, envoyez le contrôle de barre d’outils à un message [**\_ SETEXTENDEDSTYLE to**](tb-setextendedstyle.md) . Pour déterminer les styles étendus actuellement définis, envoyez un message [**to \_ GETEXTENDEDSTYLE**](tb-getextendedstyle.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





