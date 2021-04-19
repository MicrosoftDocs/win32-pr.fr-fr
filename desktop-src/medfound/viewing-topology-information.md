---
description: Affichage des informations de topologie
ms.assetid: d687ecd3-9ad6-46d5-b927-d9b99af2002f
title: Affichage des informations de topologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c4e6808fb2414de14817c63f9f4736acc9223f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517624"
---
# <a name="viewing-topology-information"></a><span data-ttu-id="ce20f-103">Affichage des informations de topologie</span><span class="sxs-lookup"><span data-stu-id="ce20f-103">Viewing Topology Information</span></span>

<span data-ttu-id="ce20f-104">Dans TopoEdit, chaque élément de topologie, comme les nœuds, les entrées de nœud et les sorties de nœud, possède un magasin d’attributs associé qui gère le comportement du nœud.</span><span class="sxs-lookup"><span data-stu-id="ce20f-104">In TopoEdit, each topology item, such as nodes, node inputs, and node outputs, has an associated attribute store that manages the behavior of the node.</span></span> <span data-ttu-id="ce20f-105">Pour afficher les attributs, sélectionnez l’élément, puis le **volet attributs** affiche les informations.</span><span class="sxs-lookup"><span data-stu-id="ce20f-105">To see the attributes, select the item, and the **Attributes Pane** displays the information.</span></span> <span data-ttu-id="ce20f-106">Pour les topologies qui sont chargées à partir d’un fichier XML, certains des nœuds peuvent ne pas afficher l’intégralité du magasin d’attributs.</span><span class="sxs-lookup"><span data-stu-id="ce20f-106">For topologies that are loaded from an XML file, some of the nodes may not display the entire attribute store.</span></span> <span data-ttu-id="ce20f-107">Pour afficher l’intégralité du magasin d’attributs, résolvez la topologie.</span><span class="sxs-lookup"><span data-stu-id="ce20f-107">To see the entire attribute store, resolve the topology.</span></span> <span data-ttu-id="ce20f-108">Pour plus d’informations, consultez [résolution d’une topologie à l’aide de TopoEdit](resolving-a-topology-with-topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="ce20f-108">For more information, see [Resolving a Topology with TopoEdit](resolving-a-topology-with-topoedit.md).</span></span>

<span data-ttu-id="ce20f-109">Le tableau suivant montre l’élément de topologie et les attributs affichés dans le volet.</span><span class="sxs-lookup"><span data-stu-id="ce20f-109">The following table shows the topology item and the attributes that the pane displays.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce20f-110">Élément de topologie</span><span class="sxs-lookup"><span data-stu-id="ce20f-110">Topology item</span></span></th>
<th><span data-ttu-id="ce20f-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="ce20f-111">Attributes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce20f-112">Nœuds de topologie</span><span class="sxs-lookup"><span data-stu-id="ce20f-112">Topology nodes</span></span></td>
<td><ul>
<li><span data-ttu-id="ce20f-113"><a href="topology-node-attributes.md">Attributs de nœud de topologie</a> pour tous les nœuds.</span><span class="sxs-lookup"><span data-stu-id="ce20f-113"><a href="topology-node-attributes.md">Topology Node Attributes</a> for all nodes.</span></span><br/></li>
<li><span data-ttu-id="ce20f-114"><a href="presentation-descriptor-attributes.md">Attributs du descripteur de présentation</a> pour les nœuds sources uniquement.</span><span class="sxs-lookup"><span data-stu-id="ce20f-114"><a href="presentation-descriptor-attributes.md">Presentation Descriptor Attributes</a> for source nodes only.</span></span><br/></li>
<li><span data-ttu-id="ce20f-115">Informations d’entrée et de sortie de l’autorité de confiance pour les nœuds de transformation et de sortie.</span><span class="sxs-lookup"><span data-stu-id="ce20f-115">Input and output trust authority information for transform and output nodes.</span></span><br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce20f-116">Entrée de nœud</span><span class="sxs-lookup"><span data-stu-id="ce20f-116">Node input</span></span></td>
<td><ul>
<li><span data-ttu-id="ce20f-117"><a href="media-type-attributes.md">Attributs de type de média</a> pour tous les nœuds.</span><span class="sxs-lookup"><span data-stu-id="ce20f-117"><a href="media-type-attributes.md">Media Type Attributes</a> for all nodes.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce20f-118">Sortie de nœud</span><span class="sxs-lookup"><span data-stu-id="ce20f-118">Node output</span></span></td>
<td><ul>
<li><span data-ttu-id="ce20f-119"><a href="stream-descriptor-attributes.md">Attributs du descripteur de flux</a> uniquement pour les nœuds sources.</span><span class="sxs-lookup"><span data-stu-id="ce20f-119"><a href="stream-descriptor-attributes.md">Stream Descriptor Attributes</a> for source nodes only.</span></span><br/></li>
<li><span data-ttu-id="ce20f-120"><a href="media-type-attributes.md">Attributs de type de média</a> pour tous les nœuds.</span><span class="sxs-lookup"><span data-stu-id="ce20f-120"><a href="media-type-attributes.md">Media Type Attributes</a> for all nodes.</span></span><br/></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ce20f-121">Les valeurs d’attribut, à l’exception des références de pointeur et des valeurs de tableau, peuvent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="ce20f-121">The attribute values, except for pointer references and array values, can be changed.</span></span> <span data-ttu-id="ce20f-122">Pour modifier une valeur d’attribut, tapez la nouvelle valeur en regard de l’attribut, puis cliquez sur **Enregistrer** dans le **volet attributs**.</span><span class="sxs-lookup"><span data-stu-id="ce20f-122">To change an attribute value, type in the new value next to the attribute and click **Save** on the **Attributes Pane**.</span></span> <span data-ttu-id="ce20f-123">La nouvelle valeur est mise à jour dans le magasin d’attributs et appliquée à la topologie uniquement après qu’elle a été résolue.</span><span class="sxs-lookup"><span data-stu-id="ce20f-123">The new value is updated in the attribute store and applied to the topology only after it is resolved.</span></span>

## <a name="to-add-a-new-attribute-for-a-node"></a><span data-ttu-id="ce20f-124">Pour ajouter un nouvel attribut pour un nœud</span><span class="sxs-lookup"><span data-stu-id="ce20f-124">To add a new attribute for a node</span></span>

1.  <span data-ttu-id="ce20f-125">Sélectionnez le nœud en cliquant dessus dans le **volet Topology**.</span><span class="sxs-lookup"><span data-stu-id="ce20f-125">Select the node by clicking it on the **Topology Pane**.</span></span>

    <span data-ttu-id="ce20f-126">Les attributs définis sur le nœud s’affichent dans le **volet attributs**.</span><span class="sxs-lookup"><span data-stu-id="ce20f-126">The attributes that are set on the node are shown on the **Attributes Pane**.</span></span>

2.  <span data-ttu-id="ce20f-127">Dans le **volet attributs**, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="ce20f-127">On the **Attributes Pane**, click **Add**.</span></span>

    <span data-ttu-id="ce20f-128">La boîte de dialogue **Ajouter un attribut** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="ce20f-128">This opens the **Add Attribute** dialog box.</span></span>

3.  <span data-ttu-id="ce20f-129">Dans la première liste déroulante, choisissez la catégorie d’attribut.</span><span class="sxs-lookup"><span data-stu-id="ce20f-129">From the first drop-down list, choose the Attribute category.</span></span>

    <span data-ttu-id="ce20f-130">Les catégories dépendent du nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="ce20f-130">The categories depend on the topology node.</span></span> <span data-ttu-id="ce20f-131">Par exemple, pour le nœud source, la liste déroulante affiche les attributs du **descripteur de présentation** et les **attributs de nœud** comme les catégories disponibles.</span><span class="sxs-lookup"><span data-stu-id="ce20f-131">For example, for the source node, the drop-down list shows **Presentation Descriptor Attributes** and **Node Attributes** as the available categories.</span></span>

4.  <span data-ttu-id="ce20f-132">Dans la deuxième liste déroulante, choisissez l’attribut que vous souhaitez définir sur le nœud.</span><span class="sxs-lookup"><span data-stu-id="ce20f-132">From the second drop-down list, choose the attribute that you want to set on the node.</span></span>

5.  <span data-ttu-id="ce20f-133">Dans la zone d’édition, ajoutez la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="ce20f-133">In the edit box, add the value for the attribute.</span></span>

6.  <span data-ttu-id="ce20f-134">Cliquez sur **Ajouter** pour ajouter l’attribut et revenir à la fenêtre principale, ou cliquez sur **Annuler** pour annuler l’opération.</span><span class="sxs-lookup"><span data-stu-id="ce20f-134">Click **Add** to add the attribute and return to the main window, or click **Cancel** to cancel the operation.</span></span>

7.  <span data-ttu-id="ce20f-135">Dans le menu **topologie** , cliquez sur **résoudre la topologie** pour définir le nouvel attribut sur la topologie.</span><span class="sxs-lookup"><span data-stu-id="ce20f-135">From the **Topology** menu, click **Resolve Topology** to set the new attribute to the topology.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce20f-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ce20f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce20f-137">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="ce20f-137">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 




