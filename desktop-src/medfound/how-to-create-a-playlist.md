---
description: Cette rubrique explique comment utiliser la source de séquence pour lire une séquence de fichiers.
ms.assetid: 5a760492-bd52-40b8-a652-8a62646db6ae
title: Comment créer une sélection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d2a36735d29510e0622882a399fff199fd2289261453a51f281414b5076826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828169"
---
# <a name="how-to-create-a-playlist"></a>Comment créer une sélection

Cette rubrique explique comment utiliser la source de séquence pour lire une séquence de fichiers.

## <a name="overview"></a>Vue d’ensemble

Pour lire des fichiers multimédias dans une séquence, l’application doit ajouter des topologies dans une séquence afin de créer une sélection, puis les faire défiler sur la session multimédia pour la lecture.

La source de Sequencer garantit une lecture transparente en initialisant et en chargeant la topologie suivante avant que la session multimédia ne commence à lire la topologie actuelle. Cela permet à l’application de démarrer rapidement la topologie suivante chaque fois qu’elle est requise.

La session multimédia est responsable de l’alimentation des données aux récepteurs et de la diffusion des topologies dans la source de séquence. En outre, la session multimédia gère l’heure de présentation des segments.

Pour plus d’informations sur la façon dont la source Sequencer gère les topologies, consultez [à propos de la source de Sequencer](about-the-sequencer-source.md).

Cette procédure pas à pas contient les étapes suivantes :

1.  [Composants requis](#prerequisites)
2.  [Initialisation de Media Foundation](#initializing-media-foundation)
3.  [Création d’objets Media Foundation](#creating-media-foundation-objects)
4.  [Création de la source du média](#creating-the-media-source)
5.  [Création de topologies partielles](#creating-partial-topologies)
6.  [Ajout de topologies à la source de Sequencer](#adding-topologies-to-the-sequencer-source)
7.  [Définition de la première topologie sur la session multimédia](#setting-the-first-topology-on-the-media-session)
8.  [Mise en file d’attente de la topologie suivante sur la session multimédia](#queuing-the-next-topology-on-the-media-session)
9.  [Libération de la source de Sequencer](#releasing-the-sequencer-source)

Les exemples de code présentés dans cette rubrique sont des extraits de l' [exemple de code source Sequencer](sequencer-source-example-code.md), qui contient l’exemple de code complet.

## <a name="prerequisites"></a>Prérequis

Avant de commencer cette procédure pas à pas, familiarisez-vous avec les concepts de Media Foundation suivants :

-   [Session multimédia](media-session.md)
-   [Topologies](topologies.md)
-   [Générateurs d’événements de média](media-event-generators.md)
-   [Descripteurs de présentation](presentation-descriptors.md)

Lisez également [Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md), car l’exemple de code shwon ici s’étend sur le code de cette rubrique.

## <a name="initializing-media-foundation"></a>Initialisation de Media Foundation

Avant de pouvoir utiliser des interfaces ou des méthodes Media Foundation, initialisez Media Foundation en appelant la fonction [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) . Pour plus d’informations, consultez [initialisation des Media Foundation](initializing-media-foundation.md).


```C++
    hr = MFStartup(MF_VERSION);
```



## <a name="creating-media-foundation-objects"></a>Création d’objets Media Foundation

Créez ensuite les objets Media Foundation suivants :

-   Session multimédia. Cet objet expose l’interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) , qui fournit des méthodes pour lire, suspendre et arrêter la topologie actuelle.
-   Source de Sequencer. Cet objet expose l’interface [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) , qui fournit des méthodes pour ajouter, mettre à jour et supprimer des topologies dans une séquence.

1.  Appelez la fonction [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) pour créer la session multimédia.
2.  Appelez [**IMFMediaEventQueue :: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) pour demander le premier événement de la session multimédia.
3.  Appelez la fonction [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) pour créer la source de Sequencer.

Le code suivant crée la session multimédia et demande le premier événement :


```C++
//  Create a new instance of the media session.
HRESULT CPlayer::CreateSession()
{
    // Close the old session, if any.
    HRESULT hr = CloseSession();
    if (FAILED(hr))
    {
        goto done;
    }

    assert(m_state == Closed);

    // Create the media session.
    hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    // Start pulling events from the media session
    hr = m_pSession->BeginGetEvent((IMFAsyncCallback*)this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = Ready;

done:
    return hr;
}
```



## <a name="creating-the-media-source"></a>Création de la source du média

Ensuite, créez une source de média pour le premier segment de sélection. Utilisez le programme de [résolution source](source-resolver.md) pour créer une source de média à partir d’une URL. Pour ce faire, appelez la fonction [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) pour créer un programme de résolution source, puis appelez la méthode [**IMFSourceResolver :: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) pour créer la source du média.

Pour plus d’informations sur les sources multimédias, consultez [sources multimédias](media-sources.md).

## <a name="creating-partial-topologies"></a>Création de topologies partielles

Chaque segment de la source Sequencer a sa propre topologie partielle. Ensuite, créez des topologies partielles pour les sources multimédias. Pour une topologie partielle, les nœuds sources de la topologie sont connectés directement aux nœuds de sortie, sans spécifier de transformations intermédiaires. La session multimédia utilise l’objet de chargeur topologique pour résoudre la topologie. Une fois la topologie résolue, les décodeurs requis et les autres nœuds de transformation sont ajoutés. La source de Sequencer peut également contenir des topologies complètes.

Pour créer l’objet de topologie, utilisez la fonction [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) , puis utilisez l’interface [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) pour créer des nœuds de flux.

Pour obtenir des instructions complètes sur l’utilisation de ces éléments de programmation pour créer des topologies, consultez [création de topologies de lecture](creating-playback-topologies.md).

Une application peut lire une partie sélectionnée de la source Native en configurant le nœud source. Pour ce faire, définissez l’attribut [**MF \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md) et l’attribut [**\_ \_ MEDIASTOP MF TOPONODE**](mf-toponode-mediastop-attribute.md) sur les nœuds de topologie de **\_ \_ \_ nœud SOURCESTREAM** de topologie MF. Spécifiez l’heure de début du média et l’heure d’arrêt du support par rapport au début de la source Native en tant que types **UINT64** .

## <a name="adding-topologies-to-the-sequencer-source"></a>Ajout de topologies à la source de Sequencer

Ensuite, ajoutez à la source Sequencer les topologies partielles que vous avez créées. Chaque élément Sequence, appelé *segment*, est associé à un identificateur **MFSequencerElementId** . Pour plus d’informations sur la façon dont la source Sequencer gère les topologies, consultez [à propos de la source de Sequencer](about-the-sequencer-source.md).

Une fois que toutes les topologies ont été ajoutées à la source de Sequencer, l’application doit marquer le dernier segment dans la séquence pour terminer la lecture dans le pipeline. Sans cet indicateur, la source de Sequencer attend l’ajout de plus de topologies.

1.  Appelez la méthode [**IMFSequencerSource :: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) pour ajouter une topologie spécifique à la source de Sequencer.

    ```C++
        hr = m_pSequencerSource->AppendTopology(
            pTopology, 
            SequencerTopologyFlags_Last, 
            &SegmentId
            );
    ```

    

    [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) ajoute la topologie spécifiée à la séquence. Cette méthode retourne l’identificateur de segment dans le paramètre *pdwId* .

    Si la topologie est la dernière de la source Sequencer, transmettez SequencerTopologyFlags \_ Last dans le paramètre *dwFlags* . Cette valeur est définie dans l’énumération [**MFSequencerTopologyFlags**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) .

2.  Appelez [**IMFSequencerSource :: UpdateTopologyFlags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) pour mettre à jour les indicateurs de la topologie associée à l’identificateur de segment dans la liste d’entrée. Dans ce cas, l’appel indique que le segment spécifié est le dernier segment du séquenceur. (Cet appel est facultatif si la dernière topologie est spécifiée dans l’appel [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) .)

    ```C++
        BOOL bFirstSegment = (NumSegments() == 0);

        if (!bFirstSegment)
        {
            // Remove the "last segment" flag from the last segment.
            hr = m_pSequencerSource->UpdateTopologyFlags(LastSegment(), 0);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    ```

    

L’application peut remplacer la topologie d’un segment par une autre topologie en appelant [**IMFSequencerSource :: UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) et en passant la nouvelle topologie dans *pTopology*. S’il existe de nouvelles sources natives dans la nouvelle topologie, les sources sont ajoutées au cache source. La liste des prérolls est également actualisée.

## <a name="setting-the-first-topology-on-the-media-session"></a>Définition de la première topologie sur la session multimédia

Ensuite, met en file d’attente la première topologie dans la source de séquence sur la session multimédia. Pour récupérer la première topologie à partir de la source de Sequencer, l’application doit appeler la méthode [**IMFMediaSourceTopologyProvider :: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) . Cette méthode retourne la topologie partielle, qui est résolue par la session multimédia.

Pour plus d’informations sur les topologies partielles, consultez [à propos des topologies](about-topologies.md).

1.  Récupérez la source du média natif pour la première topologie de la source de séquence.
2.  Créez un descripteur de présentation pour la source du média en appelant la méthode [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) .
3.  Récupérez la topologie associée pour la présentation en appelant la méthode [**IMFMediaSourceTopologyProvider :: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .
4.  Définissez la première topologie sur la session multimédia en appelant [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

    Appelez [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) avec le paramètre *DwSetTopologyFlags* défini sur **null**. Cela indique à la session multimédia de démarrer la topologie spécifiée lorsque la topologie actuelle est terminée. Étant donné que dans ce cas, la topologie spécifiée est la première topologie et qu’il n’y a pas de présentation actuelle, la session multimédia démarre immédiatement la nouvelle présentation.

    La valeur **null** indique également que la session multimédia doit résoudre la topologie, car la topologie retournée par le fournisseur de topologie est toujours une topologie partielle.


```C++
// Queues the next topology on the session.

HRESULT CPlaylist::QueueNextSegment(IMFPresentationDescriptor *pPD)
{
    IMFMediaSourceTopologyProvider *pTopoProvider = NULL;
    IMFTopology *pTopology = NULL;

    //Get the topology for the presentation descriptor
    HRESULT hr = m_pSequencerSource->QueryInterface(IID_PPV_ARGS(&pTopoProvider));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pTopoProvider->GetMediaSourceTopology(pPD, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the topology on the media session
    m_pSession->SetTopology(NULL, pTopology);

done:
    SafeRelease(&pTopoProvider);
    SafeRelease(&pTopology);
    return hr;
}
```



## <a name="queuing-the-next-topology-on-the-media-session"></a>Mise en file d’attente de la topologie suivante sur la session multimédia

Ensuite, l’application doit gérer l’événement [MENewPresentation](menewpresentation.md) .

La source de Sequencer déclenche [MENewPresentation](menewpresentation.md) quand la session multimédia commence à exécuter un segment qui en suit un autre segment. Cet événement informe l’application de la topologie suivante dans la source de séquence en fournissant le descripteur de présentation du segment suivant dans la liste des préroll. L’application doit récupérer la topologie associée, en utilisant le fournisseur de topologie, et la faire défiler sur la session multimédia. La source de Sequencer préroll ensuite cette topologie, ce qui garantit une transition transparente entre les présentations.

Lorsque l’application recherche sur les segments, elle reçoit plusieurs événements [MENewPresentation](menewpresentation.md) , car la source de Sequencer actualise la liste des préroll et configure la topologie correcte. L’application doit gérer chaque événement et effectuer la mise en file d’attente de la topologie renvoyée dans les données d’événement, sur la session multimédia. Pour plus d’informations sur les segments ignorés, consultez [utilisation de la source de Sequencer](using-the-sequencer-source.md).

Pour plus d’informations sur l’obtention des notifications de la source de Sequencer, consultez [événements sources de Sequencer](sequencer-source-events.md).

1.  Dans le gestionnaire d’événements [MENewPresentation](menewpresentation.md) , récupérez le descripteur de présentation du segment suivant à partir des données d’événement.
2.  Obtenir la topologie associée pour la présentation en appelant la méthode [**IMFMediaSourceTopologyProvider :: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .
3.  Définissez la topologie sur la session de média en appelant la méthode [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) .

    La session multimédia démarre la nouvelle présentation lorsque la présentation en cours est terminée.


```C++
HRESULT CPlaylist::OnNewPresentation(IMFMediaEvent *pEvent)
{
    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = GetEventObject(pEvent, &pPD);

    if (SUCCEEDED(hr))
    {
        // Queue the next segment on the media session
        hr = QueueNextSegment(pPD);
    }

    SafeRelease(&pPD);
    return hr;
}
```



## <a name="releasing-the-sequencer-source"></a>Libération de la source de Sequencer

Enfin, arrêtez la source de Sequencer. Pour ce faire, appelez la méthode [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sur la source de Sequencer. Cet appel arrête toutes les sources de média natives sous-jacentes dans la source de Sequencer.

Après avoir libéré la source de Sequencer, l’application doit fermer et arrêter la session multimédia en appelant [**IMFMediaSession :: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) et [**IMFMediaSession :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown), dans cet ordre.

Pour éviter les fuites de mémoire, l’application doit libérer des pointeurs vers des interfaces Media Foundation lorsqu’elles ne sont plus nécessaires.

## <a name="next-steps"></a>Étapes suivantes

Cette procédure pas à pas montre comment créer une playlist de base à l’aide de la source de Sequencer. Après avoir créé la sélection, vous souhaiterez peut-être ajouter des fonctionnalités avancées telles que le saut de segment, la modification de l’état de lecture et la recherche dans un segment. La liste suivante fournit des liens vers les rubriques connexes :

-   [Comment contrôler les États de présentation](how-to-control-presentation-states.md): la source de Sequencer s’appuie sur la session multimédia pour fournir un contrôle de transport tel que, lecture, pause et arrêt.
-   [Comment effectuer un nettoyage](how-to-perform-scrubbing.md) de la vue décrit les étapes requises pour rechercher une position spécifique dans un flux.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Source de Sequencer](sequencer-source.md)
</dt> </dl>

 

 



