---
description: Vous pouvez modifier les graphiques audio à tout moment pour ajouter ou supprimer des voix ou des sous-graphiques entiers.
ms.assetid: b2f9ec6a-4b5b-e618-759b-d7dbc0d97ac4
title: 'Procédure : Ajouter ou supprimer dynamiquement des voix d’un graphique audio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb26150b5614ec53e4cc4de5af74e9a14ee2a94
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225516"
---
# <a name="how-to-dynamically-add-or-remove-voices-from-an-audio-graph"></a>Procédure : Ajouter ou supprimer dynamiquement des voix d’un graphique audio

Vous pouvez modifier les graphiques audio à tout moment pour ajouter ou supprimer des voix ou des sous-graphiques entiers. Cette rubrique vous montre comment ajouter ou supprimer des voix de mixage secondaire d’un graphique qui a été créé en suivant les étapes décrites dans [Comment : générer un traitement audio de base Graph](how-to--build-a-basic-audio-processing-graph.md). Une seule voix peut envoyer sa sortie à plusieurs voix ou à une longue chaîne de voix. La suppression ou l’ajout d’une seule voix peut avoir un impact important sur un graphique audio.

## <a name="to-dynamically-change-an-audio-graph"></a>Pour modifier dynamiquement un graphique audio

L’ajout et la suppression de voix d’un graphique audio sont très similaires à l’ajout ou à la suppression de nœuds d’une liste ou d’un graphique à liaison unique.

-   Pour ajouter une voix ou un sous-graphe à un graphique audio

    Définissez la sortie d’une voix dans le graphique, la voix parente, sur la voix à ajouter à l’aide de la fonction [**SetOutputVoices**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) . Définissez la sortie de la nouvelle voix sur l’enfant d’origine de la voix parente.

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pNewVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    send.pOutputVoice = pChildVoice;
    pNewVoice->SetOutputVoices(&sendlist);
    ```

    

-   Pour supprimer une voix ou un sous-graphique d’un graphique audio

    Définissez la voix de sortie du parent de la voix en cours de suppression sur l’enfant de la voix en cours de suppression. Si la voix en cours de suppression se trouve à la fin du graphique, la voix parente doit être modifiée pour pointer vers la voix principale.

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pChildVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    ```

    

Notez que, par souci de clarté, chaque parent n’a qu’un seul enfant dans ces exemples. Si un nœud parent a plusieurs enfants, son sendlist contient un tableau de voix au lieu d’un pointeur vers une seule voix.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Graphiques audio](audio-graphs.md)
</dt> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> <dt>

[Procédure : créer un graphique de traitement audio de base](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Procédure : utiliser des voix prémixées](how-to--use-submix-voices.md)
</dt> <dt>

[Procédure : Créer une chaîne d’effets](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 
