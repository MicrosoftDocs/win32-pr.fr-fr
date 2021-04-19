---
description: Ajout de nœuds de sortie avec TopoEdit
ms.assetid: 23d60fc7-547b-4ef5-b334-5f1b38e58e92
title: Ajout de nœuds de sortie avec TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84dc30631332e8138b35e4bbc0ccde75ec9b0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515230"
---
# <a name="adding-output-nodes-with-topoedit"></a>Ajout de nœuds de sortie avec TopoEdit

Dans une topologie, un nœud de sortie représente un récepteur multimédia qui reçoit des données multimédia à partir d’un nœud de transformation et le présente pour la lecture. Le type de nœud de sortie dépend du type de média du nœud source.

Le tableau suivant présente la commande de menu/barre d’outils permettant d’ajouter un nœud de sortie à la topologie.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Type de média source</th>
<th>Menu/commande de barre d’outils</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Flux audio</td>
<td>Dans le menu <strong>Topology (topologie</strong> ), cliquez sur <strong>Add SAR</strong>.</td>
<td>Crée un nœud de sortie pour le convertisseur audio en continu qui lit un flux audio via un périphérique audio tel qu’une carte son.</td>
</tr>
<tr class="even">
<td>Flux vidéo</td>
<td>Dans le menu <strong>Topology (topologie</strong> ), cliquez sur <strong>Add EVR</strong>.</td>
<td>Crée un nœud de sortie pour le convertisseur vidéo amélioré (EVR) qui affiche des frames pour un flux vidéo.</td>
</tr>
<tr class="odd">
<td>Récepteur multimédia personnalisé</td>
<td><ol>
<li>Dans le menu <strong>Topology (topologie</strong> ), cliquez sur <strong>Add Custom Sink</strong>.<br/> La boîte de dialogue <strong>GUID personnalisé d’entrée</strong> s’ouvre.<br/></li>
<li><p>Dans le champ <strong>GUID :</strong> , entrez le GUID de votre récepteur personnalisé que vous souhaitez ajouter à la topologie.<br/></p>
<blockquote>
[!Note]<br />
TopoEdit attend le GUID au format &quot; {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} &quot; . Dans le cas contraire, il ne parvient pas à ajouter le nœud et affiche un &quot; message d’erreur GUID non valide &quot; .
</blockquote>
<p><br/></p></li>
<li>Cliquez sur <strong>OK</strong>.<br/></li>
</ol></td>
<td>Crée un nœud de sortie pour le récepteur de flux pour une source de média personnalisée.<br/> Le récepteur personnalisé doit prendre en charge <strong>CoCreateInstance</strong> afin que le récepteur puisse être spécifié avec un CLSID.<br/></td>
</tr>
</tbody>
</table>



 

TopoEdit crée le nœud de sortie spécifié. Le **volet topologie** affiche le nœud sortie sous la forme d’une zone verte qui indique le nom du récepteur de flux.

Pour plus d’informations sur l’ajout par programme de nœuds de sortie à l’aide d’API Media Foundation, consultez [création de nœuds de sortie](creating-output-nodes.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de topologies à l’aide de TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[Convertisseur audio de streaming](streaming-audio-renderer.md)
</dt> <dt>

[Convertisseur vidéo amélioré](enhanced-video-renderer.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




