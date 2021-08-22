---
description: Ajout de nœuds de transformation avec TopoEdit
ms.assetid: e1725c37-3f04-4208-9c09-56ce9a854138
title: Ajout de nœuds de transformation avec TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b9357b08230b706dc9215cebdbc60d226cadaf0a3f1d7b29f533324ae2e3b1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664929"
---
# <a name="adding-transform-nodes-with-topoedit"></a>Ajout de nœuds de transformation avec TopoEdit

Un nœud de transformation représente une transformation de Media Foundation (MFT) qui traite les données multimédias qu’il reçoit d’un nœud source. Quand il est prêt, le pipeline le transmet au nœud de sortie pour le rendu. Dans Media Foundation, les encodeurs, les décodeurs, les multiplexeurs, les démultiplexeurs et les effets de vidéo audio sont implémentés en tant que MFTs. TopoEdit prend en charge l’ajout de nœuds de transformation qui représentent les MFTs inscrits et personnalisés.

Pour plus d’informations sur l’ajout par programme de nœuds de transformation à l’aide d’API Media Foundation, consultez [création de nœuds de transformation](creating-transform-nodes.md).

## <a name="to-add-a-registered-mft-to-the-topology"></a>Pour ajouter une table MFT inscrite à la topologie

1.  Dans le menu **topologie** , cliquez sur **Ajouter une transformation**.

    La boîte de dialogue **Sélectionner une transformation** s’ouvre. Elle affiche une liste par catégorie des MFTs enregistrés générées en énumérant les entrées inscrites dans le registre en appelant la fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) .

2.  Développez la catégorie et sélectionnez la MFT que vous souhaitez ajouter à la topologie.

3.  Cliquez sur **OK** pour fermer la boîte de dialogue et revenir au **volet topologie**.

TopoEdit crée le nœud de transformation spécifié. Le **volet topologie** affiche le nœud transformation sous la forme d’une zone verte qui affiche le nom de la table MFT.

## <a name="to-add-a-custom-mft-to-the-topology"></a>Pour ajouter une table MFT personnalisée à la topologie

1.  Dans le menu **Topology (topologie** ), cliquez sur **Add Custom MFT**.

    La boîte de dialogue **GUID personnalisé d’entrée** s’ouvre.

2.  Dans le champ **GUID :** , entrez le GUID de la MFT que vous souhaitez ajouter à la topologie.

    > [!Note]  
    > TopoEdit attend le GUID au format "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}". Dans le cas contraire, il ne parvient pas à ajouter le nœud et affiche un message d’erreur « GUID non valide ».

     

3.  Cliquez sur **OK** pour fermer la boîte de dialogue et revenir au **volet topologie**.

TopoEdit crée le nœud de transformation spécifié. Le **volet topologie** affiche le nœud transformation sous la forme d’une zone verte qui affiche le nom de la table MFT.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de topologies à l’aide de TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[Transformations de Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



