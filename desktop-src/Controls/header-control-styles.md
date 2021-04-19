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
ms.openlocfilehash: 0d8450ad39cdb965e3e4be15f0093ec4737a87c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545444"
---
# <a name="header-control-styles"></a>Styles de contrôle d’en-tête

Les contrôles Header ont plusieurs styles, décrits dans cette section, qui déterminent l’apparence et le comportement du contrôle. Vous définissez les styles initiaux lorsque vous créez le contrôle header.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_BUTTONS"></span><span id="hds_buttons"></span><dl> <dt><strong>HDS_BUTTONS</strong></dt> </dl></td>
<td style="text-align: left;">Chaque élément du contrôle apparaît et se comporte comme un bouton de commande. Ce style est utile si une application exécute une tâche quand l’utilisateur clique sur un élément dans le contrôle d’en-tête. Par exemple, une application peut trier les informations dans les colonnes différemment en fonction de l’élément sur lequel l’utilisateur clique. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_DRAGDROP"></span><span id="hds_dragdrop"></span><dl> <dt><strong>HDS_DRAGDROP</strong></dt> </dl></td>
<td style="text-align: left;">Autorise la réorganisation des éléments d’en-tête par glisser-déplacer. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FILTERBAR"></span><span id="hds_filterbar"></span><dl> <dt><strong>HDS_FILTERBAR</strong></dt> </dl></td>
<td style="text-align: left;">Ajoutez une barre de filtre dans le cadre du contrôle d’en-tête standard. Cette barre permet aux utilisateurs d’appliquer facilement un filtre à l’affichage. Les appels à <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> entraînent une nouvelle taille pour le contrôle et provoquent la mise à jour du mode liste. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_FLAT"></span><span id="hds_flat"></span><dl> <dt><strong>HDS_FLAT</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 6,0 et versions ultérieures</a>. Fait en sorte que le contrôle d’en-tête soit dessiné à plat lorsque le système d’exploitation s’exécute en mode classique. <br/>
<blockquote>
[!Note]<br />
Comctl32.dll version 6 n’est pas redistribuable, mais elle est incluse dans Windows. Pour utiliser Comctl32.dll version 6, spécifiez-la dans un manifeste. Pour plus d’informations sur les manifestes, consultez <a href="cookbook-overview.md">activation des styles visuels</a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FULLDRAG"></span><span id="hds_fulldrag"></span><dl> <dt><strong>HDS_FULLDRAG</strong></dt> </dl></td>
<td style="text-align: left;">Fait en sorte que le contrôle header affiche le contenu des colonnes même lorsque l’utilisateur redimensionne une colonne. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HIDDEN"></span><span id="hds_hidden"></span><dl> <dt><strong>HDS_HIDDEN</strong></dt> </dl></td>
<td style="text-align: left;">Indique un contrôle d’en-tête destiné à être masqué. Ce style ne masque pas le contrôle. Au lieu de cela, lorsque vous envoyez le message <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> à un contrôle d’en-tête avec le style HDS_HIDDEN, le contrôle retourne zéro dans le membre <strong>CY</strong> de la structure <a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>WINDOWPOS</strong></a> . Vous masquez ensuite le contrôle en affectant à sa hauteur la valeur zéro. Cela peut être utile lorsque vous souhaitez utiliser le contrôle comme conteneur d’informations au lieu d’un contrôle visuel. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_HORZ"></span><span id="hds_horz"></span><dl> <dt><strong>HDS_HORZ</strong></dt> </dl></td>
<td style="text-align: left;">Crée un contrôle d’en-tête avec une orientation horizontale. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HOTTRACK"></span><span id="hds_hottrack"></span><dl> <dt><strong>HDS_HOTTRACK</strong></dt> </dl></td>
<td style="text-align: left;">Active le suivi réactif. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_CHECKBOXES"></span><span id="hds_checkboxes"></span><dl> <dt><strong>HDS_CHECKBOXES</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 6,00 et versions ultérieures</a>. Autorise le placement de cases à cocher sur les éléments d’en-tête. Pour plus d’informations, consultez le membre <strong>fmt</strong> de <a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>HDITEM</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_NOSIZING"></span><span id="hds_nosizing"></span><dl> <dt><strong>HDS_NOSIZING</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 6,00 et versions ultérieures</a>. L’utilisateur ne peut pas faire glisser le séparateur sur le contrôle header.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_OVERFLOW"></span><span id="hds_overflow"></span><dl> <dt><strong>HDS_OVERFLOW</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 6,00 et versions ultérieures</a>. Un bouton s’affiche lorsque tous les éléments ne peuvent pas être affichés dans le rectangle du contrôle header. Lorsque vous cliquez dessus, ce bouton envoie une notification <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> .<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Notes

Pour récupérer et modifier les styles après avoir créé le contrôle, utilisez les fonctions [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) et [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



