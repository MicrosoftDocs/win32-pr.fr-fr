---
description: Affichage des informations de topologie
ms.assetid: d687ecd3-9ad6-46d5-b927-d9b99af2002f
title: Affichage des informations de topologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fd1d7d28de3d7fa5420241abf793295323532dca29d3d68d1271545aa460dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237371"
---
# <a name="viewing-topology-information"></a>Affichage des informations de topologie

Dans TopoEdit, chaque élément de topologie, comme les nœuds, les entrées de nœud et les sorties de nœud, possède un magasin d’attributs associé qui gère le comportement du nœud. Pour afficher les attributs, sélectionnez l’élément, puis le **volet attributs** affiche les informations. Pour les topologies qui sont chargées à partir d’un fichier XML, certains des nœuds peuvent ne pas afficher l’intégralité du magasin d’attributs. Pour afficher l’intégralité du magasin d’attributs, résolvez la topologie. Pour plus d’informations, consultez [résolution d’une topologie à l’aide de TopoEdit](resolving-a-topology-with-topoedit.md).

Le tableau suivant montre l’élément de topologie et les attributs affichés dans le volet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Élément de topologie</th>
<th>Attributs</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Nœuds de topologie</td>
<td><ul>
<li><a href="topology-node-attributes.md">Attributs de nœud de topologie</a> pour tous les nœuds.<br/></li>
<li><a href="presentation-descriptor-attributes.md">Attributs du descripteur de présentation</a> pour les nœuds sources uniquement.<br/></li>
<li>Informations d’entrée et de sortie de l’autorité de confiance pour les nœuds de transformation et de sortie.<br/></li>
</ul></td>
</tr>
<tr class="even">
<td>Entrée de nœud</td>
<td><ul>
<li><a href="media-type-attributes.md">Attributs de type de média</a> pour tous les nœuds.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Sortie de nœud</td>
<td><ul>
<li><a href="stream-descriptor-attributes.md">Attributs du descripteur de flux</a> uniquement pour les nœuds sources.<br/></li>
<li><a href="media-type-attributes.md">Attributs de type de média</a> pour tous les nœuds.<br/></li>
</ul></td>
</tr>
</tbody>
</table>



 

Les valeurs d’attribut, à l’exception des références de pointeur et des valeurs de tableau, peuvent être modifiées. Pour modifier une valeur d’attribut, tapez la nouvelle valeur en regard de l’attribut, puis cliquez sur **Enregistrer** dans le **volet attributs**. La nouvelle valeur est mise à jour dans le magasin d’attributs et appliquée à la topologie uniquement après qu’elle a été résolue.

## <a name="to-add-a-new-attribute-for-a-node"></a>Pour ajouter un nouvel attribut pour un nœud

1.  Sélectionnez le nœud en cliquant dessus dans le **volet Topology**.

    Les attributs définis sur le nœud s’affichent dans le **volet attributs**.

2.  Dans le **volet attributs**, cliquez sur **Ajouter**.

    La boîte de dialogue **Ajouter un attribut** s’ouvre.

3.  Dans la première liste déroulante, choisissez la catégorie d’attribut.

    Les catégories dépendent du nœud de topologie. Par exemple, pour le nœud source, la liste déroulante affiche les attributs du **descripteur de présentation** et les **attributs de nœud** comme les catégories disponibles.

4.  Dans la deuxième liste déroulante, choisissez l’attribut que vous souhaitez définir sur le nœud.

5.  Dans la zone d’édition, ajoutez la valeur de l’attribut.

6.  Cliquez sur **Ajouter** pour ajouter l’attribut et revenir à la fenêtre principale, ou cliquez sur **Annuler** pour annuler l’opération.

7.  Dans le menu **topologie** , cliquez sur **résoudre la topologie** pour définir le nouvel attribut sur la topologie.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




