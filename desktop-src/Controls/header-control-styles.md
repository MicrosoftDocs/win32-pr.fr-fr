---
title: Styles de contrôle d’en-tête (CommCtrl. h)
description: Les contrôles Header ont plusieurs styles, décrits dans cette section, qui déterminent l’apparence et le comportement du contrôle. Vous définissez les styles initiaux lorsque vous créez le contrôle header.
ms.assetid: e47dc6c3-a1af-456c-9235-29ce63f1e13b
topic_type:
- apiref
api_name:
- HDS_BUTTONS
- HDS_DRAGDROP
- HDS_FILTERBAR
- HDS_FLAT
- HDS_FULLDRAG
- HDS_HIDDEN
- HDS_HORZ
- HDS_HOTTRACK
- HDS_CHECKBOXES
- HDS_NOSIZING
- HDS_OVERFLOW
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e93ce8ab766bd99b6cd7774511cb24db0553aed
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469176"
---
# <a name="header-control-styles"></a>Styles de contrôle d’en-tête

Les contrôles Header ont plusieurs styles, décrits dans cette section, qui déterminent l’apparence et le comportement du contrôle. Vous définissez les styles initiaux lorsque vous créez le contrôle header.




| Constante | Description | 
|----------|-------------|
| <span id="HDS_BUTTONS"></span><span id="hds_buttons"></span><dl><dt><strong>HDS_BUTTONS</strong></dt></dl> | Chaque élément du contrôle apparaît et se comporte comme un bouton de commande. Ce style est utile si une application exécute une tâche quand l’utilisateur clique sur un élément dans le contrôle d’en-tête. Par exemple, une application peut trier les informations dans les colonnes différemment en fonction de l’élément sur lequel l’utilisateur clique. <br /> | 
| <span id="HDS_DRAGDROP"></span><span id="hds_dragdrop"></span><dl><dt><strong>HDS_DRAGDROP</strong></dt></dl> | Autorise la réorganisation des éléments d’en-tête par glisser-déplacer. <br /> | 
| <span id="HDS_FILTERBAR"></span><span id="hds_filterbar"></span><dl><dt><strong>HDS_FILTERBAR</strong></dt></dl> | Ajoutez une barre de filtre dans le cadre du contrôle d’en-tête standard. Cette barre permet aux utilisateurs d’appliquer facilement un filtre à l’affichage. Les appels à <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> entraînent une nouvelle taille pour le contrôle et provoquent la mise à jour du mode liste. <br /> | 
| <span id="HDS_FLAT"></span><span id="hds_flat"></span><dl><dt><strong>HDS_FLAT</strong></dt></dl> | <a href="common-control-versions.md">Version 6,0 et versions ultérieures</a>. Fait en sorte que le contrôle d’en-tête soit dessiné à plat lorsque le système d’exploitation s’exécute en mode classique. <br /><blockquote>[!Note]<br />Comctl32.dll version 6 n’est pas redistribuable, mais elle est incluse dans Windows. Pour utiliser Comctl32.dll version 6, spécifiez-la dans un manifeste. Pour plus d’informations sur les manifestes, consultez <a href="cookbook-overview.md">activation des styles visuels</a>.</blockquote><br /> | 
| <span id="HDS_FULLDRAG"></span><span id="hds_fulldrag"></span><dl><dt><strong>HDS_FULLDRAG</strong></dt></dl> | Fait en sorte que le contrôle header affiche le contenu des colonnes même lorsque l’utilisateur redimensionne une colonne. <br /> | 
| <span id="HDS_HIDDEN"></span><span id="hds_hidden"></span><dl><dt><strong>HDS_HIDDEN</strong></dt></dl> | Indique un contrôle d’en-tête destiné à être masqué. Ce style ne masque pas le contrôle. Au lieu de cela, lorsque vous envoyez le message <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> à un contrôle d’en-tête avec le style HDS_HIDDEN, le contrôle retourne zéro dans le membre <strong>CY</strong> de la structure <a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>WINDOWPOS</strong></a> . Vous masquez ensuite le contrôle en affectant à sa hauteur la valeur zéro. Cela peut être utile lorsque vous souhaitez utiliser le contrôle comme conteneur d’informations au lieu d’un contrôle visuel. <br /> | 
| <span id="HDS_HORZ"></span><span id="hds_horz"></span><dl><dt><strong>HDS_HORZ</strong></dt></dl> | Crée un contrôle d’en-tête avec une orientation horizontale. <br /> | 
| <span id="HDS_HOTTRACK"></span><span id="hds_hottrack"></span><dl><dt><strong>HDS_HOTTRACK</strong></dt></dl> | Active le suivi réactif. <br /> | 
| <span id="HDS_CHECKBOXES"></span><span id="hds_checkboxes"></span><dl><dt><strong>HDS_CHECKBOXES</strong></dt></dl> | <a href="common-control-versions.md">Version 6,00 et versions ultérieures</a>. Autorise le placement de cases à cocher sur les éléments d’en-tête. Pour plus d’informations, consultez le membre <strong>fmt</strong> de <a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>HDITEM</strong></a>.<br /> | 
| <span id="HDS_NOSIZING"></span><span id="hds_nosizing"></span><dl><dt><strong>HDS_NOSIZING</strong></dt></dl> | <a href="common-control-versions.md">Version 6,00 et versions ultérieures</a>. L’utilisateur ne peut pas faire glisser le séparateur sur le contrôle header.<br /> | 
| <span id="HDS_OVERFLOW"></span><span id="hds_overflow"></span><dl><dt><strong>HDS_OVERFLOW</strong></dt></dl> | <a href="common-control-versions.md">Version 6,00 et versions ultérieures</a>. Un bouton s’affiche lorsque tous les éléments ne peuvent pas être affichés dans le rectangle du contrôle header. Lorsque vous cliquez dessus, ce bouton envoie une notification <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> .<br /> | 




## <a name="remarks"></a>Remarques

Pour récupérer et modifier les styles après avoir créé le contrôle, utilisez les fonctions [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) et [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



