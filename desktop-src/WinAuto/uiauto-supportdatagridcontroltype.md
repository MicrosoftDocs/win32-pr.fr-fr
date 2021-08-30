---
title: DataGrid (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle DataGrid.
ms.assetid: 2381b302-37d6-4159-bb7d-862ae41af695
keywords:
- UI Automation, prise en charge du type de contrôle DataGrid
- UI Automation, type de contrôle DataGrid
- UI Automation, arborescence pour le type de contrôle DataGrid
- UI Automation, propriétés du type de contrôle DataGrid
- UI Automation, modèles de contrôle pour le type de contrôle DataGrid
- UI Automation, événements pour le type de contrôle DataGrid
- arborescences, type de contrôle DataGrid
- Propriétés, DataGrid (type de contrôle)
- modèles de contrôle, type de contrôle DataGrid
- événements, type de contrôle DataGrid
- prise en charge du type de contrôle DataGrid
- DataGrid (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle DataGrid
- types de contrôles, modèles de contrôle pour le type de contrôle DataGrid
- types de contrôles, prise en charge de DataGrid
- types de contrôles, DataGrid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a87f8c3f7e8e5039440741a0f2dfff5b20fbac9a46864611fedaf967094e7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098242"
---
# <a name="datagrid-control-type"></a>DataGrid (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **DataGrid** .

Le type de contrôle **DataGrid** permet à un utilisateur de travailler facilement avec des éléments qui contiennent des données ou des éléments d’automatisation présentés dans des colonnes ou des lignes. Les contrôles de grille de données présentent des lignes d’éléments et des colonnes d’informations sur ces éléments. un contrôle list-view dans Windows l’explorateur Vista est un exemple qui prend en charge le type de contrôle **DataGrid** .

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **DataGrid** . Les exigences d’UI Automation s’appliquent à tous les contrôles de grille de données où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Exemple de type de contrôle DataGrid](#datagrid-control-type-example)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation relative aux contrôles de grille de données, et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Affichage de contrôle</th>
<th>Affichage de contenu</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>DataGrid
<ul>
<li>Header (0, 1 ou 2)
<ul>
<li>HeaderItem (nombre de lignes ou colonnes)</li>
</ul></li>
<li>DataItem (0 ou plus ; peut être structuré dans une hiérarchie)</li>
</ul></li>
</ul></td>
<td><ul>
<li>DataGrid
<ul>
<li>DataItem (0 ou plus ; peut être structuré dans une hiérarchie)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **DataGrid** . Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur        | Remarques                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques.   | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                                                                                                                                 |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.   | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                                                                                                                                     |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques.   | Pris en charge s’il existe un rectangle englobant. Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable.                                                                                                         |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **DataGrid** |                                                                                                                                                                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | La valeur de cette propriété doit toujours être **true**. Cela signifie que le contrôle de grille de données doit toujours être dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | La valeur de cette propriété doit toujours être **true**. Cela signifie que le contrôle de grille de données doit toujours être inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                                                |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques.   | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                                                                                                                                    |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consultez les remarques.   | S’il existe une étiquette de texte statique, cette propriété doit exposer une référence à ce contrôle.                                                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.   | Chaîne localisée correspondant au type de contrôle **DataGrid** . La valeur par défaut est « Data Grid » pour en-US ou anglais (États-Unis).                                                                                                                                                                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques.   | Le contrôle de grille de données obtient généralement la valeur de sa propriété **Name** à partir d’une étiquette de texte statique. S’il n’y a pas d’étiquette de texte statique, un développeur d’applications doit attribuer une valeur à pour la propriété **Name** . La valeur de la propriété **Name** ne doit jamais être le contenu textuel du contrôle d’édition. |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles de grille de données. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle                                         | Support  | Notes                                                                                                                                                                             |
|---------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Obligatoire | Le contrôle de grille de données lui-même prend toujours en charge le modèle de contrôle [Grid](uiauto-implementinggrid.md) , car les éléments qu’il contient ont des métadonnées disposées dans une grille. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Dépend  | La possibilité de faire défiler la grille de données dépend du contenu et de la présence de barres de défilement.                                                                                       |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | Dépend  | La possibilité de sélectionner la grille de données dépend du contenu.                                                                                                                           |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Dépend  | Un contrôle de grille de données qui possède un en-tête doit prendre en charge le modèle de contrôle [table](uiauto-implementingtable.md) .                                                                   |



 

Les éléments de données dans les conteneurs de grille de données prennent en charge au minimum ce qui suit :

-   Modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) (si la grille de données est sélectionnable)
-   Modèle de contrôle [ScrollItem](uiauto-implementingscrollitem.md) (si la grille de données est défilante)
-   [GridItem](uiauto-implementinggriditem.md) (modèle de contrôle)
-   Modèle de contrôle [TableItem](uiauto-implementingtableitem.md) (si la grille de données a un en-tête)

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de grille de données. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                                        | Remarques                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                                                          |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.                      |                                                                                                                                                          |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                                      | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.                                 |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.                                  | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.                               |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                          |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                          |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété MultipleViewCurrentViewPropertyId.             | Si le contrôle prend en charge la propriété CurrentView du modèle de contrôle [MultipleView](uiauto-implementingmultipleview.md) , il doit prendre en charge cet événement. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontallyScrollablePropertyId.   | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.                                         |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalScrollPercentPropertyId. | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.                                         |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalViewSizePropertyId.           | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.                                         |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalScrollPercentPropertyId.     | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.                                         |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticallyScrollablePropertyId.       | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.                                         |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalViewSizePropertyId.               | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.                                         |
| [**\_InvalidatedEventId de sélection UIA \_**](uiauto-event-ids.md)                                                            |                                                                                                                                                          |



 

## <a name="datagrid-control-type-example"></a>Exemple de type de contrôle DataGrid

L’image suivante illustre un contrôle List-View qui implémente le type de contrôle **DataGrid** .

![capture d’écran du contrôle List-View avec le type de contrôle DataGrid](images/datagridxmpl.jpg)

L’affichage de contrôle et l’affichage de contenu de l’arborescence UI Automation relative au contrôle d’affichage de liste sont affichés ci-dessous. Les modèles de contrôle de chaque élément Automation sont indiqués entre parenthèses.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Arborescence UI Automation-vue de contrôle</th>
<th>Arborescence UI Automation-affichage du contenu</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DataGrid (tri, table, sélection, grille)
<ul>
<li>En-tête
<ul>
<li>&quot;Nom &quot; de HeaderItem (Invoke)</li>
<li>HeaderItem &quot; date &quot; de modification (Invoke)</li>
<li>&quot;Taille HeaderItem &quot; (Invoke)</li>
</ul></li>
<li>Groupe &quot; Contoso &quot; (TableItem, GridItem, SelectionItem, table *, Grid*)
<ul>
<li>&quot;Receivable.docde comptes DataItem &quot; (SelectionItem, Invoke, TableItem *, GridItem*)</li>
<li>&quot;Payable.docde comptes DataItem &quot; (SelectionItem, Invoke, TableItem *, GridItem*)</li>
</ul></li>
</ul></td>
<td>DataGrid (Table, Grid, Selection)
<ul>
<li>Groupe &quot; Contoso &quot; (TableItem, GridItem, SelectionItem, table *, Grid*)
<ul>
<li>&quot;Receivable.docde comptes DataItem &quot; (SelectionItem, Invoke, TableItem *, GridItem*)</li>
<li>&quot;Payable.docde comptes DataItem &quot; (SelectionItem, Invoke, TableItem *, GridItem*)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

\*L’exemple précédent montre une grille de données qui contient plusieurs niveaux de contrôles. Le contrôle **Group** (« contoso ») contient deux contrôles **DataItem** (« Accounts Receivable.doc » et « Accounts Payable.doc »). Une paire **DataGrid de DataGrid** /  est indépendante d’une paire à un autre niveau. Les contrôles **DataItem** sous un **groupe** peuvent également être exposés en tant que type de contrôle [ListItem](uiauto-supportlistitemcontroltype.md) , ce qui leur permet d’être présentés plus clairement comme des objets sélectionnables, plutôt que comme des éléments de données simples. Cet exemple n’inclut pas les sous-éléments des éléments de données groupés. Pour un autre exemple de plusieurs niveaux de contrôles, consultez le type de contrôle [DataItem](uiauto-supportdataitemcontroltype.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




