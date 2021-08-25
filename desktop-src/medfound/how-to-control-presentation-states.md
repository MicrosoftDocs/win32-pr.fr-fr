---
description: Comment contrôler les États de présentation
ms.assetid: 978373ef-b2a4-4035-b889-e28a037c0ab5
title: Comment contrôler les États de présentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2148410527ecf966b10e605bbe4d6beb0ac3d515acd6895e4fc03e73564a72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942419"
---
# <a name="how-to-control-presentation-states"></a>Comment contrôler les États de présentation

La session multimédia fournit un contrôle de transport, tel que la modification des États de présentation (lecture, pause et arrêt dans un scénario de lecture de style playlist). Cette rubrique décrit les méthodes de session multimédia qu’une application doit appeler pour modifier l’état de lecture.

Le tableau suivant répertorie les transitions d’état de présentation valides.



| Transition d'état | Description                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| Lecture > pause | L’horloge de la présentation se fige.                                                            |
| Lecture > arrêter  | L’horloge de la présentation est réinitialisée.                                                           |
| Pause-> de lecture | L’horloge de la présentation reprend à partir du moment où elle figée pendant la lecture pour suspendre la transition. |
| Interrompre-> arrêter | L’horloge de la présentation est réinitialisée.                                                           |
| Lecture >  | L’horloge de présentation commence au début de la présentation.                      |
| Arrêter > suspendre | Non autorisé.                                                                               |



 

## <a name="to-change-presentation-states"></a>Pour modifier les États de présentation

-   Appelez la méthode [**IMFMediaSession ::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) pour suspendre la lecture.

    ```C++
    hr = pMediaSession->Pause();
    ```

    

    Avant d’appeler cette méthode, l’application doit appeler la méthode [**IMFMediaSession :: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) pour déterminer si la source du média prend en charge l’État pause. Si c’est le cas, cette méthode retourne **MFSESSIONCAP \_ Pause** dans le paramètre *pdwCaps* .

    Suspendre arrête temporairement la session multimédia, l’horloge de présentation et le récepteur de flux pour la présentation actuelle. Une fois l’appel terminé, l’application reçoit un événement [MESessionPaused](mesessionpaused.md) .

-   Appelez la méthode [**IMFMediaSession :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) pour arrêter la lecture.

    ```C++
    hr = pMediaSession->Stop();
    ```

    

    Cette méthode arrête la session multimédia en arrêtant la source du média, les horloges correspondantes et les récepteurs de flux. Si la session multimédia contrôle la [source de Sequencer](sequencer-source.md), les sources natives sous-jacentes sont arrêtées par la source de Sequencer. Une fois la session multimédia arrêtée, l’application reçoit un événement [MESessionStopped](mesessionstopped.md) .

-   Appelez la méthode [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) pour démarrer la lecture ou rechercher une nouvelle position.

    ```C++
    hr = pMediaSession->Start(NULL, &var);
    ```

    

    Cette méthode démarre la session multimédia à partir des États pause et arrêt. La session multimédia est responsable de la configuration du workflow dans le pipeline. Cette méthode indique à la session multimédia de démarrer l’horloge de la présentation. Après cet appel, la session multimédia envoie un événement [MESessionStarted](mesessionstarted.md) à l’application.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Session multimédia](media-session.md)
</dt> </dl>

 

 



