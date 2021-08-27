---
description: Ajout de nœuds de sortie avec TopoEdit
ms.assetid: 23d60fc7-547b-4ef5-b334-5f1b38e58e92
title: Ajout de nœuds de sortie avec TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e975e332a464218f8629363f34a2d3fbef0e5a49
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481975"
---
# <a name="adding-output-nodes-with-topoedit"></a>Ajout de nœuds de sortie avec TopoEdit

Dans une topologie, un nœud de sortie représente un récepteur multimédia qui reçoit des données multimédia à partir d’un nœud de transformation et le présente pour la lecture. Le type de nœud de sortie dépend du type de média du nœud source.

Le tableau suivant présente la commande de menu/barre d’outils permettant d’ajouter un nœud de sortie à la topologie.




| Type de média source | Menu/commande de barre d’outils | Description | 
|-------------------|----------------------|-------------|
| Flux audio | Dans le menu <strong>Topology (topologie</strong> ), cliquez sur <strong>Add SAR</strong>. | Crée un nœud de sortie pour le convertisseur audio en continu qui lit un flux audio via un périphérique audio tel qu’une carte son. | 
| Flux vidéo | Dans le menu <strong>Topology (topologie</strong> ), cliquez sur <strong>Add EVR</strong>. | Crée un nœud de sortie pour le convertisseur vidéo amélioré (EVR) qui affiche des frames pour un flux vidéo. | 
| Récepteur multimédia personnalisé | <ol><li>Dans le menu <strong>Topology (topologie</strong> ), cliquez sur <strong>Add Custom Sink</strong>.<br /> La boîte de dialogue <strong>GUID personnalisé d’entrée</strong> s’ouvre.<br /></li><li><p>Dans le champ <strong>GUID :</strong> , entrez le GUID de votre récepteur personnalisé que vous souhaitez ajouter à la topologie.<br /></p><blockquote>[!Note]<br />TopoEdit attend le GUID au format "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}". Dans le cas contraire, il ne parvient pas à ajouter le nœud et affiche un message d’erreur « GUID non valide ».</blockquote><p><br /></p></li><li>Cliquez sur <strong>OK</strong>.<br /></li></ol> | Crée un nœud de sortie pour le récepteur de flux pour une source de média personnalisée.<br /> Le récepteur personnalisé doit prendre en charge <strong>CoCreateInstance</strong> afin que le récepteur puisse être spécifié avec un CLSID.<br /> | 




 

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

 

 




