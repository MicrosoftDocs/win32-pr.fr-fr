---
title: Styles étendus de contrôle Tree-View (CommCtrl. h)
description: Cette section répertorie les styles étendus utilisés lors de la création de contrôles d’arborescence. La valeur des styles étendus est une combinaison d’opérations de bits de ces styles.
ms.assetid: b45e7b7c-2c7b-49fa-8679-57c478b2f796
topic_type:
- apiref
api_name:
- TVS_EX_AUTOHSCROLL
- TVS_EX_DIMMEDCHECKBOXES
- TVS_EX_DOUBLEBUFFER
- TVS_EX_DRAWIMAGEASYNC
- TVS_EX_EXCLUSIONCHECKBOXES
- TVS_EX_FADEINOUTEXPANDOS
- TVS_EX_MULTISELECT
- TVS_EX_NOINDENTSTATE
- TVS_EX_NOSINGLECOLLAPSE
- TVS_EX_PARTIALCHECKBOXES
- TVS_EX_RICHTOOLTIP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eed135e5c1cfd335333251c183b408a59d2768ac
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477385"
---
# <a name="tree-view-control-extended-styles"></a>Styles étendus de contrôle Tree-View

Cette section répertorie les styles étendus utilisés lors de la création de contrôles d’arborescence. La valeur des styles étendus est une combinaison d’opérations de bits de ces styles.




| Constante | Description | 
|----------|-------------|
| <span id="TVS_EX_AUTOHSCROLL"></span><span id="tvs_ex_autohscroll"></span><dl><dt><strong>TVS_EX_AUTOHSCROLL</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Supprimer la barre de défilement horizontale et le défilement automatique en fonction de la position de la souris.<br /> | 
| <span id="TVS_EX_DIMMEDCHECKBOXES"></span><span id="tvs_ex_dimmedcheckboxes"></span><dl><dt><strong>TVS_EX_DIMMEDCHECKBOXES</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Inclure l’état de case à cocher estompée si le contrôle a le style de <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> .<br /> | 
| <span id="TVS_EX_DOUBLEBUFFER"></span><span id="tvs_ex_doublebuffer"></span><dl><dt><strong>TVS_EX_DOUBLEBUFFER</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Spécifie la manière dont l’arrière-plan est effacé ou rempli.<br /> | 
| <span id="TVS_EX_DRAWIMAGEASYNC"></span><span id="tvs_ex_drawimageasync"></span><dl><dt><strong>TVS_EX_DRAWIMAGEASYNC</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Récupère les informations de grille du calendrier.<br /> | 
| <span id="TVS_EX_EXCLUSIONCHECKBOXES"></span><span id="tvs_ex_exclusioncheckboxes"></span><dl><dt><strong>TVS_EX_EXCLUSIONCHECKBOXES</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Inclure l’état de la case à cocher d’exclusion si le contrôle a le style <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> .<br /> | 
| <span id="TVS_EX_FADEINOUTEXPANDOS"></span><span id="tvs_ex_fadeinoutexpandos"></span><dl><dt><strong>TVS_EX_FADEINOUTEXPANDOS</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Les boutons d’agrandissement et d’extraction de la souris s’affichent à l’intérieur ou à l’extérieur du contrôle.<br /> | 
| <span id="TVS_EX_MULTISELECT"></span><span id="tvs_ex_multiselect"></span><dl><dt><strong>TVS_EX_MULTISELECT</strong></dt></dl> | Non pris en charge. Ne pas utiliser.<br /> | 
| <span id="TVS_EX_NOINDENTSTATE"></span><span id="tvs_ex_noindentstate"></span><dl><dt><strong>TVS_EX_NOINDENTSTATE</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Ne mettez pas en retrait l’arborescence pour les boutons expando.<br /> | 
| <span id="TVS_EX_NOSINGLECOLLAPSE"></span><span id="tvs_ex_nosinglecollapse"></span><dl><dt><strong>TVS_EX_NOSINGLECOLLAPSE</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. <strong>Destiné à un usage interne ; non recommandé pour une utilisation dans les applications.</strong> Ne réduisez pas l’élément d’arborescence précédemment sélectionné, sauf s’il a le même parent que la nouvelle sélection. Ce style doit être utilisé avec le style <a href="tree-view-control-window-styles.md"><strong>TVS_SINGLEEXPAND</strong></a> . <br /><blockquote>[!Note]<br />Ce style n’est peut-être pas pris en charge dans les versions ultérieures de Comctl32.dll. En outre, ce style n’est pas défini dans commctrl. h. Ajoutez la définition suivante aux fichiers sources de votre application pour utiliser ce style : <code>#define TVS_EX_NOSINGLECOLLAPSE 0x0001</code></blockquote><br /> | 
| <span id="TVS_EX_PARTIALCHECKBOXES"></span><span id="tvs_ex_partialcheckboxes"></span><dl><dt><strong>TVS_EX_PARTIALCHECKBOXES</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Inclure l’état de case à cocher partiel si le contrôle a le style de <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> .<br /> | 
| <span id="TVS_EX_RICHTOOLTIP"></span><span id="tvs_ex_richtooltip"></span><dl><dt><strong>TVS_EX_RICHTOOLTIP</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Autorisez les info-bulles enrichies dans l’arborescence (dessin personnalisé avec icône et texte).<br /> | 




## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





