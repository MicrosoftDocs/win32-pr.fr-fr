---
title: Routines de vérification
description: Cette section décrit les routines de vérification que l’outil de vérification de l’accessibilité de l’interface utilisateur peut exécuter pour tester l’implémentation de l’accessibilité d’une application.
ms.assetid: 0ff38f83-5741-4c0e-a070-a8385f95eba3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 352a56b15a376af3d378def6fd49f04775063f4928fb87444107f7671c9d51ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997659"
---
# <a name="verification-routines"></a>Routines de vérification

Cette section décrit les routines de vérification que l’outil de vérification de l’accessibilité de l’interface utilisateur peut exécuter pour tester l’implémentation de l’accessibilité d’une application.



<table>
<thead>
<tr class="header">
<th>Category</th>
<th>Routine</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><strong>Cohérence</strong>$ {Remove} $<br />
</td>
<td><strong>ScreenReader</strong></td>
<td>Compile tous les éléments visibles dans la cible de vérification et les affiche dans un contrôle ListView dans l’ordre dans lequel un lecteur d’écran standard les annonce à un utilisateur.</td>
</tr>
<tr class="even">
<td><strong>UiaScreenReader</strong></td>
<td>Identique à <strong>Screenreader</strong>, mais pour les implémentations de UIA.</td>

</tr>
<tr class="odd">
<td rowspan="2"><strong>Navigation</strong>$ {Remove} $<br />
</td>
<td><strong>CheckTreeDepth</strong></td>
<td>Envoie les caractères de tabulation (ou Maj + Tab) comme entrée à la cible de vérification pour confirmer que l’interface utilisateur de la cible n’est pas trop complexe ou inaccessible à l’aide de la navigation au clavier standard.</td>
</tr>
<tr class="even">
<td><strong>CheckTabbingUia</strong></td>
<td>Envoie les caractères de tabulation (ou Maj + Tab) comme entrée à la cible de vérification pour confirmer que tous les éléments pouvant être activés dans l’interface utilisateur sont accessibles de façon ordonnée et logique à l’aide de la navigation au clavier standard.</td>

</tr>
<tr class="odd">
<td rowspan="5"><strong>Propriétés</strong>$ {Remove} $<br />
</td>
<td><strong>CheckRole</strong></td>
<td>Confirme que chaque élément pouvant être actif dans l’interface utilisateur signale un rôle MSAA logique et valide, et que le contrôle a une valeur comme requis par ce rôle.</td>
</tr>
<tr class="even">
<td><strong>CheckState</strong></td>
<td>Confirme que chaque élément pouvant être actif dans l’interface utilisateur signale un État MSAA logique valide.</td>

</tr>
<tr class="odd">
<td><strong>CheckName</strong></td>
<td>Confirme que chaque élément pouvant être actif dans l’interface utilisateur signale un nom MSAA logique valide.</td>

</tr>
<tr class="even">
<td><strong>CheckAccessKeys</strong></td>
<td>Confirme que les clés d’accès qui sont assignées aux éléments de la cible de vérification sont uniques dans la cible de vérification.</td>

</tr>
<tr class="odd">
<td><strong>CheckBoundingRect</strong></td>
<td>Confirme que chaque élément pouvant être actif dans l’interface utilisateur possède un rectangle englobant qui peut être utilisé comme cible pour le test de positionnement.</td>

</tr>
<tr class="even">
<td rowspan="2"><strong>Arborescence</strong>$ {Remove} $<br />
</td>
<td><strong>CheckParentChild</strong></td>
<td>Les relations parent et enfant dans l’arborescence d’éléments sont cohérentes et prévisibles.</td>
</tr>
<tr class="odd">
<td><strong>CheckOrphanChildren</strong></td>
<td>Confirme que chaque élément pouvant être actif dans l’interface utilisateur signale un parent MSAA valide.</td>

</tr>
<tr class="even">
<td rowspan="6"><strong>Propriétés de UIA</strong>$ {Remove} $<br />
</td>
<td><strong>CheckNameUIA</strong></td>
<td>Confirme que chaque élément pouvant être actif dans l’interface utilisateur signale un nom UIA logique valide.</td>
</tr>
<tr class="odd">
<td><strong>CheckTreeDepthUIA</strong></td>
<td>Envoie les caractères de tabulation (ou Maj + Tab) comme entrée à la cible de vérification pour confirmer que les éléments UIA de l’interface utilisateur de la cible ne sont pas trop complexes ou inaccessibles à l’aide de la navigation au clavier standard.</td>

</tr>
<tr class="even">
<td><strong>CheckStateUIA</strong></td>
<td>Confirme que chaque élément pouvant être actif dans l’interface utilisateur signale un État UIA logique valide.</td>

</tr>
<tr class="odd">
<td><strong>CheckAccessKeysUIA</strong></td>
<td>Confirme que les éléments frères n’ont pas les mêmes accès et/ou touche accélérateur.</td>

</tr>
<tr class="even">
<td><strong>CheckBoundingRectUIA</strong></td>
<td>Confirme que chaque élément UIA pouvant être actif dans l’interface utilisateur possède un rectangle englobant qui peut être utilisé comme cible pour le test de positionnement.</td>

</tr>
<tr class="odd">
<td><strong>CheckControlTypeUIA</strong></td>
<td>Confirme que chaque élément pouvant être actif dans l’interface utilisateur signale un type de contrôle UIA logique valide.</td>

</tr>
<tr class="even">
<td rowspan="3"><strong>Arborescence UIA</strong>$ {Remove} $<br />
</td>
<td><strong>CheckNavigateUia</strong></td>
<td>Confirme que le TreeWalker UIA peut naviguer dans les enfants d’un élément.</td>
</tr>
<tr class="odd">
<td><strong>CheckOrphanChildrenUia</strong></td>
<td>Confirme que chaque élément pouvant être actif dans l’interface utilisateur signale un parent UIA valide.</td>

</tr>
<tr class="even">
<td><strong>CheckSiblingsUia</strong></td>
<td>Confirme que les éléments frères n’ont pas le même nom : les paires ControlType, ni les mêmes AutomationId.</td>

</tr>
<tr class="odd">
<td><strong>Vérifications Web</strong>de $ {ROWSPAN9} $ Aria $ {Remove} $<br />
</td>
<td><strong>CheckARIARole</strong></td>
<td>Confirme que tous les éléments ont un rôle ARIA valide. La balise HTML et le rôle ARIA associés sont des éléments d’information dont les rôles non valides sont signalés comme des erreurs.</td>
</tr>
<tr class="even">
<td><strong>CheckLabel</strong></td>
<td>Confirme que chaque élément avec un rôle d’entrée, de bouton, d’image ou de repère a une étiquette.</td>

</tr>
<tr class="odd">
<td><strong>CheckRangeControls</strong></td>
<td>Confirme que les contrôles de plage avec le curseur ou le rôle de barre de progression ont des attributs ARIA appropriés définis.</td>

</tr>
<tr class="even">
<td><strong>CheckContainerRole</strong></td>
<td>Confirme qu’un élément, ou au moins un de ses enfants, a l’élément OnKeyDown/OnKeyPress défini.</td>

</tr>
<tr class="odd">
<td><strong>CheckLayoutTable</strong></td>
<td>Confirme qu’une mise en page de table a un résumé/th/Aria-DescribedBy inclus.</td>

</tr>
<tr class="even">
<td><strong>CheckGridStructure</strong></td>
<td>Confirme qu’un élément qui n’est pas une table avec un rôle de grille a une structure de grille>ligne>GridCell avec des attributs associés.</td>

</tr>
<tr class="odd">
<td><strong>CheckDataTable</strong></td>
<td>Confirme les propriétés des tables de données.</td>

</tr>
<tr class="even">
<td><strong>CheckActiveDescendants</strong></td>
<td>Confirme les propriétés des éléments avec un descendant actif défini.</td>

</tr>
<tr class="odd">
<td><strong>CheckElementsWithClickHandler</strong></td>
<td>Confirme l’index de tabulation des éléments avec des gestionnaires de clic.</td>

</tr>
<tr class="even">
<td rowspan="3"><strong>Vérifications Web</strong>$ {Remove} $<br />
</td>
<td><strong>CheckHtml (Web)</strong></td>
<td>Confirme différentes caractéristiques HTML, telles que les en-têtes, le nom, les cadres et les titres.</td>
</tr>
<tr class="odd">
<td><strong>CheckName (Web)</strong></td>
<td>Confirme les caractéristiques de nom, telles que la longueur, les caractères non valides et l’inclusion de rôle.</td>

</tr>
<tr class="even">
<td><strong>CheckRole (Web)</strong></td>
<td>Confirme les rôles non valides, les rôles qui doivent avoir des valeurs, et/ou les rôles qui ne sont pas implémentés.</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vérificateur d’accessibilité de l’interface utilisateur](ui-accessibility-checker.md)
</dt> </dl>

 

 




