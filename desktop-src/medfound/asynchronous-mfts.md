---
description: Cette rubrique décrit le traitement asynchrone des données pour les transformations de Media Foundation (MFTs).
ms.assetid: d438ffae-fc50-454f-8ce4-2d6676500fff
title: MFTs asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a16950cf431eff16f2befb382a77910c49ccb2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296359"
---
# <a name="asynchronous-mfts"></a>MFTs asynchrone

Cette rubrique décrit le traitement asynchrone des données pour les transformations de Media Foundation (MFTs).

> [!Note]  
> cette rubrique s’applique à Windows 7 ou version ultérieure.

 

-   [À propos des MFTs asynchrones](#about-asynchronous-mfts)
-   [Exigences générales](#general-requirements)
-   [Événements](#events)
-   [ProcessInput](#processinput)
-   [ProcessOutput](#processoutput)
-   [Drainage](#draining)
-   [Vidage](#flushing)
-   [Marqueurs](#markers)
-   [Modifications de format](#format-changes)
-   [Attributs](#attributes)
-   [Déverrouillage des MFTs asynchrones](#unlocking-asynchronous-mfts)
-   [Arrêt de la MFT](#shutting-down-the-mft)
-   [Inscription et énumération](#registration-and-enumeration)
-   [Rubriques connexes](#related-topics)

## <a name="about-asynchronous-mfts"></a>À propos des MFTs asynchrones

lorsque MFTs a été introduit dans Windows Vista, l’API a été conçue pour le traitement *synchrone* des données. Dans ce modèle, la MFT est toujours en attente d’obtenir une entrée ou en attente de production.

Prenons l’exemple d’un décodeur vidéo classique. Pour obtenir un frame décodé, le client appelle [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Si le décodeur a suffisamment de données pour décoder un frame, **ProcessOutput** se bloque pendant que la MFT décode le frame. Sinon, **ProcessOutput** retourne **MF_E_TRANSFORM_NEED_MORE_INPUT**, indiquant que le client doit appeler [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).

Ce modèle fonctionne bien si le décodeur effectue toutes les opérations de décodage sur un thread. Mais supposons que le décodeur utilise plusieurs threads pour décoder des frames en parallèle. Pour des performances optimales, le décodeur doit recevoir une nouvelle entrée chaque fois qu’un thread de décodage devient inactif. Mais la vitesse à laquelle les threads achèvent les opérations de décodage ne s’aligne pas exactement avec les appels du client à [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) et [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput), ce qui entraîne l’attente du travail par les threads.

Windows 7 présente le traitement *asynchrone* piloté par les événements pour MFTs. Dans ce modèle, chaque fois que la MFT a besoin d’une entrée ou d’une sortie, elle envoie un événement au client.

## <a name="general-requirements"></a>Exigences générales

Cette rubrique décrit la façon dont les MFTs asynchrones diffèrent de la MFT synchrone. Sauf indication contraire dans cette rubrique, les deux modèles de traitement sont les mêmes. (En particulier, la négociation de format est la même.)

Une table MFT asynchrone doit implémenter les interfaces suivantes :

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)

## <a name="events"></a>Événements

Une table MFT asynchrone utilise les événements suivants pour signaler son état de traitement de données :



| Événement                                                    | Description                                                       |
|----------------------------------------------------------|-------------------------------------------------------------------|
| [METransformNeedInput](metransformneedinput.md)         | Envoyé lorsque la MFT peut accepter davantage d’entrées.                          |
| [METransformHaveOutput](metransformhaveoutput.md)       | Envoyé lorsque la table MFT a une sortie.                                     |
| [METransformDrainComplete](metransformdraincomplete.md) | Envoyé lorsqu’une opération de drainage est terminée. Consultez [drainage](#draining). |
| [METransformMarker](metransformmarker.md)               | Envoyé lorsqu’un marqueur est un processus. Consultez [marqueurs](#markers).           |



 

Ces événements sont envoyés hors bande. Il est important de comprendre la différence entre les événements intrabande et hors bande dans le contexte d’une table MFT.

La conception MFT d’origine prend en charge les événements *intrabande* . Un événement intrabande contient des informations sur le flux de données, telles que des informations sur une modification de format. Le client envoie des événements intrabande à la MFT en appelant [**IMFTransform ::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent). La table MFT peut renvoyer des événements intrabande au client dans la méthode [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . (En particulier, les événements sont transmis dans le membre **pEvents** de la structure [**MFT_OUTPUT_DATA_BUFFER**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer) .)

Une table MFT envoie des événements hors bande par le biais de l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) , comme suit :

1.  La table MFT implémente l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) , comme décrit dans [Générateur d’événements multimédias](media-event-generators.md).
2.  Le client appelle **IUnknown :: QueryInterface** sur la MFT pour l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Une table MFT asynchrone doit exposer cette interface. Le MFTs synchrone ne doit pas exposer cette interface.
3.  Le client appelle [**IMFMediaEventGenerator :: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) et [**IMFMediaEventGenerator :: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) pour recevoir les événements hors bande de la MFT.

## <a name="processinput"></a>ProcessInput

La méthode [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) est modifiée comme suit :

1.  Lors du démarrage de la diffusion en continu, le client envoie le message [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) .
2.  Pendant la diffusion en continu, la MFT demande des données en envoyant un événement [METransformNeedInput](metransformneedinput.md) . Les données d’événement sont l’identificateur de flux.
3.  Pour chaque événement [METransformNeedInput](metransformneedinput.md) , le client appelle [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) pour le flux spécifié.
4.  À la fin de la diffusion en continu, le client peut appeler [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) avec le message [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) .

Remarques sur l’implémentation :

-   La table MFT ne doit pas envoyer d’événements [METransformNeedInput](metransformneedinput.md) tant qu’elle n’a pas reçu le message [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) .
-   Pendant la diffusion en continu, la table MFT peut envoyer des événements [METransformNeedInput](metransformneedinput.md) à tout moment.
-   La table MFT doit tenir à jour le nombre d’événements [METransformNeedInput](metransformneedinput.md) en attente. Tout appel à [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) qui ne correspond pas à un événement METransformNeedInput doit retourner **MF_E_NOTACCEPTING**.
-   Lorsque la table MFT reçoit le message [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) , elle réinitialise le nombre d’événements [METransformNeedInput](metransformneedinput.md) en attente à zéro.
-   La table MFT ne doit pas envoyer d’événements [METransformNeedInput](metransformneedinput.md) une fois qu’elle a reçu le message [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) .
-   Si [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) est appelé avant [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) ou après [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md), la méthode doit retourner **MF_E_NOTACCEPTING**.

## <a name="processoutput"></a>ProcessOutput

La méthode [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) est modifiée comme suit :

1.  Chaque fois que la table MFT a une sortie, elle envoie un événement [METransformHaveOutput](metransformhaveoutput.md) .
2.  Pour chaque événement [METransformHaveOutput](metransformhaveoutput.md) , le client appelle [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

Remarques sur l’implémentation :

-   Si le client appelle [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) à un autre moment, la méthode retourne **E_UNEXPECTED**.
-   Une table MFT asynchrone ne doit jamais retourner **MF_E_TRANSFORM_NEED_MORE_INPUT** à partir de la méthode [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . Si la table MFT requiert davantage d’entrées, elle envoie un événement [METransformNeedInput](metransformneedinput.md) .

## <a name="draining"></a>Drainage

Le vidage d’une table MFT fait que la table MFT produit autant de sortie que possible, quelles que soient les données d’entrée déjà envoyées. Le vidage d’une table MFT asynchrone fonctionne de la façon suivante :

1.  Le client envoie le message de [**MFT_MESSAGE_COMMAND_DRAIN**](mft-message-command-drain.md) .
2.  La table MFT continue à envoyer des événements [METransformHaveOutput](metransformhaveoutput.md) jusqu’à ce qu’elle n’ait plus aucune donnée à traiter. Elle n’envoie pas d’événements [METransformNeedInput](metransformneedinput.md) pendant cette période.
3.  Une fois que la table MFT envoie le dernier événement [METransformHaveOutput](metransformhaveoutput.md) , elle envoie un événement [METransformDrainComplete](metransformdraincomplete.md) .

Une fois la vidange terminée, la table MFT n’envoie pas d’autre événement [METransformNeedInput](metransformneedinput.md) tant qu’elle n’a pas reçu de message [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) du client.

## <a name="flushing"></a>Vidage

Le client peut vider la MFT en envoyant le message [**MFT_MESSAGE_COMMAND_FLUSH**](mft-message-command-flush.md) . La table MFT supprime tous les échantillons d’entrée et de sortie qu’elle contient.

La table MFT n’envoie pas d’autre événement [METransformNeedInput](metransformneedinput.md) tant qu’elle n’a pas reçu de message [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) du client.

## <a name="markers"></a>Marqueurs

Le client peut marquer un point dans le flux en envoyant le message [**MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) . La table MFT répond comme suit :

1.  La table MFT génère autant d’exemples de sortie que possible des données d’entrée existantes, en envoyant un événement [METransformHaveOutput](metransformhaveoutput.md) pour chaque exemple de sortie.
2.  Une fois que toutes les sorties sont générées, la table MFT envoie un événement [METransformMarker](metransformmarker.md) . Cet événement doit être envoyé après tous les événements [METransformHaveOutput](metransformhaveoutput.md) .

Supposons, par exemple, qu’un décodeur ait suffisamment de données d’entrée pour produire quatre échantillons de sortie. Si le client envoie le message [**MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) , la table MFT met en file d’attente quatre événements [METransformHaveOutput](metransformhaveoutput.md) (un par exemple de sortie), suivis d’un événement [METransformMarker](metransformmarker.md) .

Le message de marqueur est similaire au message de drainage. Toutefois, un drainage est considéré comme une rupture dans le flux, contrairement à un marqueur. Le drainage et les marqueurs présentent les différences suivantes.

Drainage

-   Lors de la vidange, la MFT n’envoie pas d’événements [METransformNeedInput](metransformneedinput.md) .
-   La table MFT ignore les données d’entrée qui ne peuvent pas être utilisées pour créer un exemple de sortie.
-   Certaines MFTs produisent une « queue » à la fin des données. Par exemple, les effets audio tels que la réverbération ou l’écho produisent des données supplémentaires une fois les données d’entrée arrêtées. Une table MFT qui génère une fin doit le faire à la fin d’une opération de drainage.
-   Une fois l’écoulement de la MFT terminé, l’exemple de sortie suivant est marqué avec l’attribut [**MFSampleExtension_Discontinuity**](mfsampleextension-discontinuity-attribute.md) , pour indiquer une discontinuité dans le flux.

Repère

-   La table MFT continue à envoyer des événements [METransformNeedInput](metransformneedinput.md) avant l’envoi de l’événement marqueur.
-   La table MFT n’ignore aucune donnée d’entrée. S’il existe des données partielles, elles doivent être traitées après le point de marqueur.
-   La table MFT ne produit pas de fin au niveau du point de marqueur.
-   La table MFT ne définit pas l’indicateur de discontinuité après le point de marqueur.

## <a name="format-changes"></a>Modifications de format

Une table MFT asynchrone doit prendre en charge les modifications de format dynamiques, comme décrit dans [gestion des modifications de flux](handling-stream-changes.md).

## <a name="attributes"></a>Attributs

Une table MFT asynchrone doit implémenter la méthode [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) pour retourner un magasin d’attributs valide. Les attributs suivants s’appliquent à un MFTs asynchrone :



| Attribut                                                                                    | Description                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [MF_TRANSFORM_ASYNC](mf-transform-async.md)                                               | La table MFT doit affecter à cet attribut la **valeur true** (1). Le client peut interroger cet attribut pour déterminer si la table MFT est asynchrone. |
| [MF_TRANSFORM_ASYNC_UNLOCK](mf-transform-async-unlock.md)                                |                                                                                                                                   |
| [**MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE**](mft-support-dynamic-format-change-attribute.md) | La table MFT doit affecter à cet attribut la **valeur true** (1). Le client peut supposer que cet attribut est défini.                                |



 

## <a name="unlocking-asynchronous-mfts"></a>Déverrouillage des MFTs asynchrones

Les MFTs asynchrones ne sont pas compatibles avec le modèle de traitement de données MFT d’origine. Pour empêcher les MFTs asynchrones de rompre les applications existantes, le mécanisme suivant est défini :

<dl> Le client appelle <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes">IMFTransform :: GetAttributes</a> sur la table MFT.  
Le client interroge pour cet attribut <a href="mf-transform-async.md">MF_TRANSFORM_ASYNC</a> . Pour une table MFT asynchrone, la valeur de cet attribut est **true**.  
Pour déverrouiller la MFT, le client doit affecter la **valeur true** à l’attribut <a href="mf-transform-async-unlock.md">MF_TRANSFORM_ASYNC_UNLOCK</a> .  
</dl>

Tant que le client n’a pas déverrouillé la MFT, toutes les méthodes [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) doivent retourner **MF_E_TRANSFORM_ASYNC_LOCKED**, avec les exceptions suivantes :

-   [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) (tous les MFTS asynchrones)
-   [**IMFTransform :: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) (tous les MFTS asynchrones)
-   [**IMFTransform :: GetOutputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype) (encodeurs uniquement)
-   [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) (encodeurs uniquement)
-   [**IMFTransform :: GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) (tous les MFTS asynchrones)
-   [**IMFTransform :: GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) (tous les MFTS asynchrones)

Le code suivant montre comment déverrouiller une table MFT asynchrone :


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
}
```



## <a name="shutting-down-the-mft"></a>Arrêt de la MFT

Un MFTs asynchrone doit implémenter l’interface [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown) .

-   [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown): la MFT doit arrêter sa file d’attente d’événements. Si vous utilisez la file d’attente d’événements standard, appelez [**IMFMediaEventQueue :: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown). Éventuellement, la MFT peut libérer d’autres ressources. Le client ne doit pas utiliser la MFT après l' **arrêt** de l’appel.
-   [**GetShutdownStatus**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-getshutdownstatus): après l’appel de [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown) , la table MFT doit retourner la valeur **MFSHUTDOWN_COMPLETED** dans le paramètre *pStatus* . Elle ne doit pas retourner la valeur **MFSHUTDOWN_INITIATED**.

## <a name="registration-and-enumeration"></a>Inscription et énumération

Pour inscrire une table MFT asynchrone, appelez la fonction [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) et définissez l’indicateur **MFT_ENUM_FLAG_ASYNCMFT** dans le paramètre *Flags* . (Précédemment, cet indicateur était réservé.)

Pour énumérer les MFTs asynchrones, appelez la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) et définissez l’indicateur **MFT_ENUM_FLAG_ASYNCMFT** dans le paramètre *Flags* . Pour la compatibilité descendante, la fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) n’énumère pas les MFTS asynchrones. Dans le cas contraire, l’installation d’une table MFT asynchrone sur l’ordinateur de l’utilisateur risque de perturber les applications existantes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transformations de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 



