---
description: création d’un Graph de Capture Audio avec aperçu
ms.assetid: 73c0b799-060b-4b20-b072-6a0c5c30de20
title: création d’un Graph de Capture Audio avec aperçu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241d5522f04e40704d635d7d4cc925fd81045579c01ae05dbdebd725611139fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108242"
---
# <a name="creating-an-audio-capture-graph-with-preview"></a>création d’un Graph de Capture Audio avec aperçu

le graphique de filtre décrit dans [création d’une capture Audio Graph](creating-an-audio-capture-graph.md) effectue la capture uniquement, sans aperçu. Pour obtenir un aperçu et une capture en même temps, le graphique de filtre doit utiliser le [filtre tee de code confidentiel infini](infinite-pin-tee-filter.md). Ce filtre a une broche d’entrée et crée autant de broches de sortie que nécessaire. (Il commence par une broche de sortie. Chaque fois que vous connectez une broche de sortie, elle en crée une autre.) Le filtre tee de pin infini remet chaque échantillon qu’il reçoit, sans modification, à travers toutes ses broches de sortie.

Connecter le filtre de Capture Audio sur le code confidentiel infini, et connectez l’infinite pin tee au multiplexeur et au [filtre de convertisseur DirectSound](directsound-renderer-filter.md). Connecter le multiplexeur au writer de fichier, comme précédemment. Le diagramme suivant illustre le graphique de filtre résultant pour un fichier AVI.

![graphique de capture audio avec aperçu](images/audio-capture-graph.png)

Étant donné que le convertisseur DirectSound est le convertisseur audio par défaut, il vous suffit d’appeler la méthode [**IGraphBuilder :: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) sur la broche de sortie d’un tee pin infini. le gestionnaire de Graph de filtre utilise des [Connecter intelligents](intelligent-connect.md) pour créer le convertisseur, l’ajouter au graphique de filtre et connecter les broches.

> [!Note]  
> Si vous capturez de l’audio à partir d’un microphone et que vous l’affichez à partir d’un haut-parleur sur le même ordinateur, vous pouvez créer des commentaires audio.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capture audio](audio-capture.md)
</dt> </dl>

 

 



