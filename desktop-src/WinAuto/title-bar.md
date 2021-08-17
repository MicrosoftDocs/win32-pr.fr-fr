---
title: Barre de titre (référence des éléments d’interface utilisateur MSAA)
description: La barre de titre en haut d’une fenêtre affiche une icône et une ligne de texte définies par l’application.
ms.assetid: f41ab777-6c94-4d8e-b743-c635e93df396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9183e4c4f5364fb45ba2a73dd2d40509c03c7838bbb248e1d95765b675f50cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993999"
---
# <a name="title-bar-msaa-ui-element-reference"></a>Barre de titre (référence des éléments d’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit les objets de **barre de titre** à des fins de référence d’élément d’interface utilisateur MSAA. La procédure de création d’objets de **barre de titre** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

La barre de titre en haut d’une fenêtre affiche une icône et une ligne de texte définies par l’application. Le texte spécifie le nom de l’application et indique l’objectif de la fenêtre. La barre de titre permet également à l’utilisateur de déplacer la fenêtre à l’aide d’une souris ou d’un autre dispositif de pointage.

Les barres de titre contiennent au moins trois petits boutons qui permettent de réduire, d’agrandir ou de restaurer et de fermer la fenêtre associée à la barre de titre. Les barres de titre contiennent également un bouton d’aide contextuelle. les Applications qui s’exécutent dans la Far-East version du système d’exploitation Windows peuvent également contenir des boutons de l’éditeur de méthode d’entrée (IME). Microsoft Active Accessibility expose ces boutons en tant qu’éléments enfants de la barre de titre.

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Les barres de titre prennent en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Les barres de titre prennent en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propriété</th>
<th>Commentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></td>
<td>La propriété <strong>ChildCount</strong> est cinq. La propriété <strong>ChildCount</strong> comprend l’éditeur IME et les boutons d’aide contextuelle, même lorsqu’ils ne sont pas affichés. Les boutons qui ne sont pas affichés ont la propriété <strong>State</strong> <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>.</td>
</tr>
<tr class="even">
<td><strong>get_accDescription</strong></td>
<td>La propriété <strong>Description</strong> de la barre de titre elle-même est : &quot; affiche le nom de la fenêtre et contient des contrôles pour la manipuler. &quot; Les boutons enfants de la barre de titre présentent les descriptions suivantes :<br/>
<ul>
<li>&quot;Déplace la fenêtre en dehors de</li>
<li>&quot;Rend la fenêtre complète</li>
<li>&quot;Place un réduit ou un</li>
<li>&quot;Ferme la fenêtre&quot;</li>
<li>&quot;Entrée ou sortie du contexte-</li>
<li>&quot;Affiche le clavier quand vous appuyez sur&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>get_accName</strong></td>
<td>La barre de titre elle-même ne prend pas en charge la propriété <strong>Name</strong> . Les boutons enfants de la barre de titre portent les noms suivants :
<ul>
<li>&quot;Réduire&quot;</li>
<li>&quot;Agrandir &quot; ou &quot; restaurer &quot; ,</li>
<li>&quot;Close&quot;</li>
<li>&quot;Aide contextuelle&quot;</li>
<li>&quot;IME&quot;</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>get_accParent</strong></td>
<td>La propriété <strong>parent</strong> de la barre de titre est la fenêtre d’application principale ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ) qui a le même nom de classe de fenêtre définie par l’application que la barre de titre.</td>
</tr>
<tr class="odd">
<td><strong>get_accRole</strong></td>
<td>La propriété de <strong>rôle</strong> est <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>. Les boutons enfants de la barre de titre ont la propriété <strong>Role</strong> <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>.</td>
</tr>
<tr class="even">
<td><strong>get_accState</strong></td>
<td>La propriété <strong>State</strong> pour la barre de titre et les boutons enfants peuvent être une combinaison d’une ou plusieurs des <a href="object-state-constants.md">valeurs</a>suivantes : <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a><br/></td>
</tr>
<tr class="odd">
<td><strong>get_accValue</strong></td>
<td>La propriété <strong>valeur</strong> est une chaîne qui est identique au texte affiché dans la barre de titre.</td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a>Remarques

-   Bien que la barre de titre d’une application ait la propriété **État** indicateur de l’état du système, elle n’a jamais le [**\_ \_ focus**](object-state-constants.md)sur le système d’état de l’indicateur d' **État** . [**\_ \_**](object-state-constants.md) La définition du focus sur un objet de barre de titre est axée sur la fenêtre d’application.
-   Étant donné que l’objet de barre de titre ne prend pas en charge l' [**affichage des \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild), les boutons de la barre de titre sont des éléments simples. Ils ne prennent pas en charge l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) proprement dit. L’objet barre de titre fournit des informations sur ces boutons enfants.
-   Comme les barres de titre n’obtiennent pas le focus et n’ont pas d’action par défaut, les méthodes [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) et [**\_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) ne sont pas prises en charge pour ce contrôle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





