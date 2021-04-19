---
description: Cette rubrique explique comment utiliser la source de Sequencer.
ms.assetid: 7ce8dc67-02b1-4fd4-9e4d-6614fdb40620
title: Utilisation de la source de Sequencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba99202838fbdc8be86f2f1d8931e5aa99ae9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517736"
---
# <a name="using-the-sequencer-source"></a>Utilisation de la source de Sequencer

Cette rubrique explique comment utiliser la [source de Sequencer](sequencer-source.md). Il contient les sections suivantes :

-   [Vue d’ensemble](#overview)
-   [Ajout de topologies](#adding-topologies)
-   [Suppression de topologies](#deleting-topologies)
-   [Omission à un segment](#skipping-to-a-segment)
-   [Rubriques connexes](#related-topics)

Pour obtenir une vue d’ensemble générale de la source de Sequencer, consultez [à propos de la source de Sequencer](about-the-sequencer-source.md).

## <a name="overview"></a>Vue d’ensemble

La source Sequencer expose les interfaces suivantes.



| Interface                                                                        | Description                                                                        |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                         | Expose les fonctionnalités de source multimédia génériques.                                        |
| [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)                                 | Permet à l’application d’ajouter ou de supprimer des topologies.                               |
| [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)         | Récupère la topologie suivante à partir de la file d’attente de la session multimédia.                         |
| [**IMFMediaSourcePresentationProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider) | Utilisé par la session multimédia pour terminer les segments. Les applications n’utilisent pas cette interface. |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                           | Interroge la source de Sequencer pour les [interfaces de service](service-interfaces.md).     |



 

Pour lire une séquence de sources multimédias, procédez comme suit :

1.  Pour créer la source de Sequencer, appelez la fonction [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) .
2.  Pour chaque segment, créez une topologie de lecture, comme décrit dans [création de topologies de lecture](creating-playback-topologies.md). Pour ajouter la topologie à la présentation, appelez [**IMFSequencerSource :: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).
3.  Avant de commencer la lecture, appelez [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) sur la source de Sequencer. Cette méthode retourne un pointeur vers un descripteur de présentation pour le premier segment. Pour obtenir la topologie associée à ce segment, appelez **QueryInterface** sur la source de Sequencer pour l’interface [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) . Transmettez le descripteur de présentation à la méthode [**IMFMediaSourceTopologyProvider :: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) . Cette méthode retourne un pointeur vers la topologie.
4.  Transmettez la topologie du premier segment à la session multimédia, en appelant la méthode [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) de la session de média.
5.  Démarrez la lecture en appelant [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).
6.  Lorsque la source de Sequencer est prête à préparer le segment suivant, elle envoie un événement [MENewPresentation](menewpresentation.md) dont les données d’événement sont un pointeur d’interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) . Là encore, récupérez la topologie du segment en appelant [**GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) sur la source de Sequencer et définissez la topologie sur la session de média en appelant [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology). Il n’est pas nécessaire de redémarrer la source du média. elle est automatiquement lue jusqu’au segment suivant.
7.  Avant de quitter l’application, arrêtez la source de Sequencer en appelant [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).

Le code suivant montre comment récupérer la topologie et la définir sur la session multimédia :


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



Pour obtenir un exemple de code complet, consultez Code de l’exemple de code [source Sequencer](sequencer-source-example-code.md).

## <a name="adding-topologies"></a>Ajout de topologies

La source de Sequencer gère deux listes de topologies : la *liste d’entrée* et la *liste de préroll*.

La liste d’entrée est une collection de topologies correspondant aux segments de sélection, dans l’ordre dans lequel ils ont été ajoutés par l’application en appelant [**IMFSequencerSource :: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology). Cette méthode affecte à chaque topologie un identificateur de *segment* unique du type **MFSequencerElementId**. L’identificateur de segment est défini en tant qu’attribut pour tous les nœuds de topologie source. Une application peut obtenir l’identificateur de segment à partir d’un nœud source à l’aide de l’attribut d' [ \_ \_ \_ ELEMENTID de séquence TOPONODE MF](mf-toponode-sequence-elementid-attribute.md) . La liste d’entrée peut avoir des topologies en double si l’application a appelé **AppendTopology** sur la même topologie plusieurs fois. Toutefois, ils sont identifiés par leurs identificateurs de segment uniques.

La liste de préroll est une collection de topologies de liste d’entrée qui ont été initialisées en vue de la lecture. Cela permet à la session de média de passer à la topologie suivante en toute transparence lorsque la topologie Active se termine. L’application ne peut pas ajouter ou supprimer directement des topologies de la liste de préroll ; elle est générée par la source de Sequencer lorsqu’une topologie de la liste d’entrée est sélectionnée pour la lecture. Ainsi, la source de Sequencer ajoute la topologie suivante à partir de la liste d’entrée à la liste des prérolls. Après cela, la source Sequencer déclenche de manière asynchrone l’événement [MENewPresentation](menewpresentation.md) et passe le descripteur de présentation pour la topologie de prérestauration en tant que données d’événement. L’application doit écouter cet événement à l’aide de l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) de la session de média et effectuer la file d’attente de la topologie de prérestauration sur la session multimédia en appelant [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology). Cette opération doit être effectuée avant que la session multimédia ne termine la lecture de la topologie Active. **SetTopology** informe la session multimédia à propos de la topologie suivante qu’elle doit lire après la fin de la lecture de la topologie Active. Pour garantir un treansition transparent, l’application doit appeler **SetTopology** avant la fin de la session de média en lisant la topologie précédente. Dans le cas contraire, il y aura un intervalle entre les segments.

L’événement [MENewPresentation](menewpresentation.md) est déclenché tant qu’il existe une topologie qui suit la topologie Active. Par conséquent, si la liste d’entrée contient une seule topologie, ou si la topologie Active est la dernière de la liste d’entrée, cet événement n’est pas déclenché.

La liste des prérolls est synchronisée avec la liste d’entrée et est actualisée chaque fois qu’une topologie est ajoutée ou supprimée dans la liste d’entrée.

## <a name="deleting-topologies"></a>Suppression de topologies

Pour supprimer une topologie de la source de Sequencer, une application doit appeler la méthode [**IMFSequencerSource ::D eletetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) et spécifier l’identificateur de segment.

Avant d’appeler [**DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology), l’application doit s’assurer que la session multimédia n’utilise pas la topologie que l’application souhaite supprimer. Pour ce faire, les deux conditions suivantes doivent se produire avant que l’application appelle **DeleteTopology**:

-   L’événement [MESessionTopologyStatus](mesessiontopologystatus.md) avec MF \_ TOPOSTATUS \_ terminé est reçu pour la topologie pour s’assurer que la lecture de la session multimédia est terminée.

-   [MESessionTopologyStatus](mesessiontopologystatus.md) avec MF \_ TOPOSTATUS \_ Started \_ source est reçu pour la topologie suivante afin de s’assurer que la session multimédia a démarré la prochaine topologie, [MESessionEnded](mesessionended.md) événement est reçu pour s’assurer que la session multimédia est terminée avec la dernière topologie de la source de Sequencer.

Si le segment en cours de suppression est la topologie Active, la lecture est arrêtée et la source Sequencer déclenche l’événement [MEEndOfPresentationSegment](meendofpresentationsegment.md) . Si la topologie Active est également la dernière topologie, l’événement [MEEndOfPresentation](meendofpresentation.md) est déclenché.

## <a name="skipping-to-a-segment"></a>Omission à un segment

Une application peut passer à un segment particulier de la séquence en démarrant la [session multimédia](media-session.md) avec un décalage de segment, comme suit :

1.  Appelez la fonction [**MFCreateSequencerSegmentOffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) pour créer le décalage du segment. Spécifiez l’identificateur du segment dans le paramètre *dwId* . (L’identificateur a été retourné par la méthode [**IMFSequencerSource :: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) lorsque vous avez ajouté la topologie à la source du séquenceur pour la première fois.) Le paramètre *hnsOffset* spécifie un décalage horaire par rapport au début du segment. La lecture démarrera à ce moment-là. Pour le paramètre *pvarSegmentOffset* , transmettez l’adresse d’un **PROPVARIANT** vide. Quand la fonction retourne, ce **PROPVARIANT** contient le décalage de segment.

2.  Appelez la méthode [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) sur la session multimédia. Pour le paramètre *pguidTimeFormat* , utilisez la valeur GUID de \_ décalage de segment de format de temps MF \_ \_ \_ . Cette valeur indique la recherche par décalage de segment. Pour le paramètre *pvarStartPosition* , transmettez l’adresse du **PROPVARIANT** créé à l’étape précédente.

L’exemple de code suivant montre comment passer au début d’un segment spécifié dans une séquence.


```C++
// Skips to the specified segment in the sequencer source

HRESULT CPlaylist::SkipTo(DWORD index)
{
    if (index >= m_count)
    {
        return E_INVALIDARG;
    }

    MFSequencerElementId ID = m_segments[index].SegmentID;

    PROPVARIANT var;

    HRESULT hr = MFCreateSequencerSegmentOffset(ID, NULL, &var);
    
    if (SUCCEEDED(hr))
    {
        hr = m_pSession->Start(&MF_TIME_FORMAT_SEGMENT_OFFSET, &var);
        PropVariantClear(&var);
    }
    return hr;
}
```



Lorsque l’application recherche sur des segments, elle reçoit plusieurs événements, car la source de Sequencer termine le segment actuel et prépare la lecture du nouveau segment. Comme ces événements sont reçus de manière asynchrone, il est difficile de prédire la séquence exacte d’événements. Ces événements sont les suivants :

-   La source Sequencer envoie un événement [MENewPresentation](menewpresentation.md) pour le nouveau segment vers lequel la session multimédia est ignorée.

-   Lorsque la source de Sequencer termine le segment actif, elle envoie l’événement [MEEndOfPresentationSegment](meendofpresentationsegment.md) .
-   La source de Sequencer annule ensuite la topologie de prérestauration. Cela génère les événements suivants pour la topologie annulée :

    -   Événement [MESessionTopologyStatus](mesessiontopologystatus.md) avec l' \_ \_ indicateur prêt TOPOSTATUS Ready.
    -   Événement [MESessionTopologyStatus](mesessiontopologystatus.md) avec l' \_ \_ indicateur source démarré MF TOPOSTATUS \_ .
    -   Événement [MEEndOfPresentationSegment](meendofpresentationsegment.md) avec l’attribut de l’annulation de la topologie de la source de l' [ \_ événement \_ \_ \_ MF](mf-event-source-topology-canceled-attribute.md) pour indiquer que la topologie a été annulée par la source de Sequencer.

-   Ensuite, la source Sequencer envoie des événements pour le nouveau segment, y compris divers événements [MESessionTopologyStatus](mesessiontopologystatus.md) .
-   Si le nouveau segment n’est pas le dernier dans la liste, la source de Sequencer actualise la liste des préroll et déclenche un autre [MENewPresentation](menewpresentation.md) pour la nouvelle topologie de préroll. Pour plus d’informations sur les topologies dans la liste des préroll, consultez [à propos de la source de Sequencer](about-the-sequencer-source.md).

Vous trouverez plus de détails sur les événements envoyés par la source de Sequencer dans la rubrique [événements](sequencer-source-events.md)de la source de Sequencer.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment créer une sélection](how-to-create-a-playlist.md)
</dt> <dt>

[Source de Sequencer](sequencer-source.md)
</dt> </dl>

 

 



