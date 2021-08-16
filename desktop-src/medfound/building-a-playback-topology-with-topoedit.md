---
description: Génération d’une topologie de lecture avec TopoEdit
ms.assetid: 4d4c4ff9-dad1-4c79-a44a-2ad20f1bbca0
title: Génération d’une topologie de lecture avec TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a71ae353c11108fe7c844d8ddd6441e652e007646b91f44c6fe2b480a22a8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035427"
---
# <a name="building-a-playback-topology-with-topoedit"></a>Génération d’une topologie de lecture avec TopoEdit

TopoEdit peut créer une topologie de lecture pour un fichier de média local en ajoutant et en connectant automatiquement les nœuds source, de transformation et de sortie. TopoEdit ne résout pas automatiquement la topologie. Pour lire la topologie, résolvez-la, puis utilisez les contrôles de transport.

## <a name="to-build-and-play-a-topology-for-a-media-file"></a>Pour générer et lire une topologie pour un fichier multimédia

1.  Dans le menu **fichier** , cliquez sur **fichier de rendu**.

    La boîte de dialogue **Sélectionner la source du média** s’ouvre.

2.  Accédez au dossier où se trouve le fichier multimédia.
3.  Dans le champ **nom du fichier :** , entrez le nom du fichier.
4.  Cliquez sur **Ouvrir**.

    Le **volet topologie** affiche la topologie connectée. En interne, TopoEdit effectue les tâches suivantes :

    -   Énumère les flux dans le fichier multimédia et crée les nœuds sources.
    -   En fonction du type de média des nœuds sources, ajoute des nœuds de transformation, tels que des décodeurs.
    -   Ajoute le récepteur de diffusion audio en continu (SAR) pour le flux audio et le récepteur Video Enhancer (EVR) pour le flux vidéo.
    -   Connecte les entrées de nœud et les sorties de nœud.

5.  Dans le menu **Topology (topologie** ), cliquez sur **Resolve Topology**.
6.  Cliquez sur le bouton **lecture** dans la barre d’outils pour lire la topologie. L’illustration suivante montre le  bouton lecture :::image type="icon" source="images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg"::: .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôles de lecture dans TopoEdit](playback-controls-in-topoedit.md)
</dt> <dt>

[Résolution d’une topologie avec TopoEdit](resolving-a-topology-with-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



