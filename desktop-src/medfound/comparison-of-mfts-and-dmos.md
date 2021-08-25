---
description: Les transformations de Media Foundation (MFTs) sont une évolution du modèle de transformation introduit pour la première fois avec DirectX Media Objects (DMOs).
ms.assetid: 4e8c3ec9-6ffa-4858-a4ea-8ef8ccaf9253
title: Comparaison entre MFT et DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e145effed095fb22f6bfeb07cbee23ab3d30836a404f36a2bad4b9fbeb1dd81a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958979"
---
# <a name="comparison-of-mfts-and-dmos"></a>Comparaison entre MFT et DMO

Les transformations de Media Foundation (MFTs) sont une évolution du modèle de transformation introduit pour la première fois avec DirectX Media Objects (DMOs). Cette rubrique résume les principales façons dont MFTs diffère de DMOs. lisez cette rubrique si vous êtes déjà familiarisé avec les interfaces DMO ou si vous souhaitez convertir un DMO existant en MFT.

Cette rubrique contient les sections suivantes :

-   [Nombre de Flux](#number-of-streams)
-   [Négociation de format](#format-negotiation)
-   [Streaming](#streaming)
    -   [Allocation des ressources](#allocating-resources)
    -   [Traitement des données](#processing-data)
    -   [Vidage](#flushing)
    -   [Discontinuités de flux](#stream-discontinuities)
-   [Différences diverses](#miscellaneous-differences)
-   [Indicateurs](#flags)
    -   [Indicateurs ProcessInput](#processinput-flags)
    -   [Indicateurs ProcessOutput](#processoutput-flags)
    -   [Indicateurs GetInputStatus](#getinputstatus-flags)
    -   [Indicateurs GetOutputStatus](#getoutputstatus-flags)
    -   [Indicateurs GetInputStreamInfo](#getinputstreaminfo-flags)
    -   [Indicateurs GetOutputStreamInfo](#getoutputstreaminfo-flags)
    -   [Indicateurs SetInputType/SetOutputType](#setinputtypesetoutputtype-flags)
-   [Codes d’erreur](#error-codes)
-   [création d’objets/MFT hybrides DMO](#creating-hybrid-dmomft-objects)
-   [Rubriques connexes](#related-topics)

## <a name="number-of-streams"></a>Nombre de Flux

un DMO a un nombre fixe de flux, alors qu’un MFT peut prendre en charge un nombre dynamique de flux. Le client peut ajouter des flux d’entrée, et la table MFT peut ajouter de nouveaux flux de sortie pendant le traitement. Toutefois, les MFTs ne sont pas nécessaires pour prendre en charge les flux dynamiques. Une table MFT peut avoir un nombre fixe de flux, comme un DMO.

Les méthodes suivantes sont utilisées pour prendre en charge les flux dynamiques sur une table MFT :

-   [**IMFTransform::AddInputStreams**](/windows/win32/api/mftransform/nf-mftransform-imftransform-addinputstreams)
-   [**IMFTransform ::D eleteInputStream**](/windows/win32/api/mftransform/nf-mftransform-imftransform-deleteinputstream)
-   [**IMFTransform::GetStreamIDs**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamids)
-   [**IMFTransform::GetStreamLimits**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamlimits)

En outre, la méthode [**IMFTransform ::P rocessoutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) définit le comportement d’ajout ou de suppression de flux de sortie.

étant donné que les DMOs ont des flux fixes, les flux sur un DMO sont identifiés à l’aide de valeurs d’index de base zéro. MFTs, en revanche, utilisez des identificateurs de flux qui ne correspondent pas nécessairement aux valeurs d’index. Cela est dû au fait que le nombre de flux sur une table MFT peut changer. Par exemple, le flux 0 peut être supprimé, ce qui laisse Stream 1 comme premier flux. Toutefois, une table MFT avec un nombre fixe de flux doit respecter la même convention que DMOs et utiliser des valeurs d’index pour les identificateurs de flux.

## <a name="format-negotiation"></a>Négociation de format

MFTs utilisez l’interface [**IMFMediaType**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediatype) pour décrire les types de médias. Dans le cas contraire, la négociation de format avec MFTs fonctionne sur les mêmes principes de base que avec DMOs. Le tableau suivant répertorie les méthodes de négociation de format pour DMOs et les méthodes correspondantes pour MFTs.



| méthode DMO                                                                        | MFT, méthode                                                                          |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**IMediaObject::GetInputCurrentType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputcurrenttype)   | [**IMFTransform::GetInputCurrentType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)       |
| [**IMediaObject::GetInputMaxLatency**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputmaxlatency)     | [**IMFTransform::GetInputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**IMediaObject::GetInputSizeInfo**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo)         | [**IMFTransform::GetInputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)                 | [**IMFTransform::GetInputAvailableType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)   |
| [**IMediaObject::GetOutputCurrentType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputcurrenttype) | [**IMFTransform::GetOutputCurrentType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)     |
| [**IMediaObject::GetOutputSizeInfo**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo)       | [**IMFTransform::GetOutputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)       |
| [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)               | [**IMFTransform::GetOutputAvailableType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) |



 

## <a name="streaming"></a>Diffusion en continu

Comme DMOs, MFTs traite les données par le biais d’appels à des méthodes [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) et [**ProcessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) . voici les principales différences entre les DMO et les processus MFT lors de la diffusion de données en continu.

### <a name="allocating-resources"></a>Allocation des ressources

MFTs n’ont pas les méthodes [**IMediaObject :: AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) et [**IMediaObject :: FreeStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-freestreamingresources) utilisées avec DMOs. Pour gérer efficacement l’allocation et la désallocation des ressources, une table MFT peut répondre aux messages suivants dans la méthode [**IMFTransform ::P rocessmessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) :

-   [**\_notification de \_ début \_ de \_ diffusion de message MFT**](mft-message-notify-begin-streaming.md)
-   [**\_ \_ début de la notification par message MFT \_ \_ du \_ flux**](mft-message-notify-start-of-stream.md)

En outre, le client peut signaler le début et la fin d’un flux en appelant [**ProcessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) avec les messages suivants :

-   [**\_ \_ \_ fin \_ de flux de notification de message MFT \_**](mft-message-notify-end-of-stream.md)
-   [**\_notification de \_ fin \_ de \_ diffusion de message MFT**](mft-message-notify-end-streaming.md)

ces deux messages n’ont pas d’équivalent DMO exact.

### <a name="processing-data"></a>Traitement des données

MFTs utilisez les exemples de supports pour stocker les données d’entrée et de sortie. Les exemples de média exposent l’interface [**IMFSample**](/windows/win32/api/mfobjects/nn-mfobjects-imfsample) et contiennent les données suivantes :

-   Horodatage et durée.
-   Attributs qui contiennent des informations par exemple. Pour obtenir la liste des attributs, consultez [exemples d’attributs](sample-attributes.md).
-   Zéro, un ou plusieurs tampons de média. Chaque mémoire tampon de média expose l’interface [**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) .

l’interface [**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) est similaire à l’interface **IMediaBuffer** DMO. Pour accéder à la mémoire tampon sous-jacente, appelez [**IMFMediaBuffer :: Lock**](/windows/win32/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Cette méthode est à peu près équivalente à [**IMediaBuffer :: GetBufferAndLength**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-getbufferandlength) pour DMOs.

Pour les données vidéo non compressées, une mémoire tampon de support peut également prendre en charge l’interface [**IMF2DBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imf2dbuffer) . Une table MFT qui traite la vidéo non compressée (en tant qu’entrée ou sortie) doit être préparée à utiliser l’interface **IMF2DBuffer** si la mémoire tampon l’expose. Pour plus d’informations, consultez [mémoires tampons vidéo non compressées](uncompressed-video-buffers.md).

Media Foundation fournit certaines implémentations standard de [**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer), il n’est généralement pas nécessaire d’écrire votre propre implémentation. pour créer une mémoire tampon de DMO à partir d’une mémoire tampon de Media Foundation, appelez [**MFCreateLegacyMediaBufferOnMFMediaBuffer**](/windows/win32/api/mfapi/nf-mfapi-mfcreatelegacymediabufferonmfmediabuffer).

### <a name="flushing"></a>Vidage

Les MFTs n’ont pas de méthode [**flush**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-flush) . Pour vider une table MFT, appelez [**IMFTransform ::P rocessmessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) avec le message de vidage de la [**\_ \_ commande \_ MFT message**](mft-message-command-flush.md) .

### <a name="stream-discontinuities"></a>Discontinuités de flux

Les MFTs n’ont pas de méthode de [**discontinuité**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-discontinuity) . Pour signaler une discontinuité dans un flux, définissez l’attribut de [**\_ discontinuité MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) sur l’exemple d’entrée.

## <a name="miscellaneous-differences"></a>Différences diverses

Voici quelques-unes des différences mineures entre MFTs et DMOs.

-   il n’existe aucun équivalent MFT pour les méthodes de DMO suivantes :
    -   [**IMediaObject :: Lock**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-lock)
    -   [**IMediaObject::SetInputMaxLatency**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputmaxlatency)
-   Les MFTs ne sont pas nécessaires pour prendre en charge l’agrégation.
-   MFTs prend en charge une opération appelée *drainage*. L’objectif de la vidange est de traiter toutes les données qui restent dans le MF, sans fournir de données d’entrée supplémentaires à la MFT (par exemple, à la fin du flux). Pour vider une table MFT, appelez [**IMFTransform ::P rocessmessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) avec le message de [**drainage de \_ \_ commande \_ de message MFT**](mft-message-command-drain.md) . Pour plus d’informations, consultez [modèle de traitement MFT de base](basic-mft-processing-model.md).
-   MFTs peut avoir des attributs, y compris des attributs par flux. Utilisez les méthodes suivantes pour récupérer les attributs d’une table MFT :

    -   [**IMFTransform :: GetAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getattributes)
    -   [**IMFTransform::GetInputStreamAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)
    -   [**IMFTransform::GetOutputStreamAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)

-   MFTs peut traiter les événements. Pour envoyer un événement à une table MFT, appelez [**IMFTransform ::P rocessevent**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processevent). Une table MFT peut envoyer un événement au client par le biais de la méthode [**ProcessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) . Pour plus d’informations, consultez [modèle de traitement MFT de base](basic-mft-processing-model.md).

## <a name="flags"></a>Indicateurs

les tableaux suivants répertorient les différents indicateurs de DMO et leurs équivalents MFT. chaque fois qu’un indicateur de DMO est mappé directement à un indicateur MFT, les deux indicateurs ont la même valeur numérique. toutefois, certains indicateurs de DMO n’ont pas d’équivalents de la table MFT exacte, et vice versa.

### <a name="processinput-flags"></a>Indicateurs ProcessInput

DMOs : DMO énumération [**\_ \_ d' \_ \_ \_ indicateurs de tampon de données d’entrée**](/previous-versions/windows/embedded/aa451599(v=msdn.10)) .

MFTs : aucune énumération équivalente.



| indicateur de DMO                                  | Indicateur MFT                                                                                                                                      |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **DMO \_ données d’entrée \_ \_ BUFFERF \_ SYNCPOINT**  | Aucun indicateur équivalent. Au lieu de cela, définissez l’attribut [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) sur l’exemple. |
| **DMO \_ \_BUFFERF des données d’entrée \_ \_**       | Aucun indicateur équivalent. Au lieu de cela, appelez [**IMFSample :: SetSampleTime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampletime) sur l’exemple.                                  |
| **DMO \_ données d’entrée \_ \_ BUFFERF \_ TIMELENGTH** | Aucun indicateur équivalent. Au lieu de cela, appelez [**IMFSample :: SetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) sur l’exemple.                          |



 

### <a name="processoutput-flags"></a>Indicateurs ProcessOutput

DMOs : DMO de traiter l’énumération des [**\_ \_ \_ \_ indicateurs de sortie**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_process_output_flags) .

MFTs : énumération des [**\_ \_ indicateurs de \_ sortie \_ du processus MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_process_output_flags) .



| indicateur de DMO                                            | Indicateur MFT                                            |
|-----------------------------------------------------|-----------------------------------------------------|
| **DMO \_ TRAITER la \_ sortie \_ ignorée \_ quand \_ aucune \_ mémoire tampon** | **\_sortie du processus MFT \_ \_ ignorée \_ en l’absence de \_ \_ mémoire tampon** |



 

DMOs : DMO l’énumération des [**\_ \_ indicateurs de tampon de \_ données \_ \_ de sortie**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_output_data_buffer_flags) .


MFTs : énumération d' [**\_ \_ indicateurs de tampon de données de sortie \_ \_ \_ MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_data_buffer_flags) .



| indicateur de DMO                                   | Indicateur MFT                                                                                                                                            |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| **DMO \_ données de sortie \_ \_ BUFFERF \_ SYNCPOINT**  | Aucun indicateur équivalent. Au lieu de cela, recherchez l’attribut [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) sur l’exemple. |
| **DMO \_ \_temps de \_ BUFFERF des données de sortie \_**       | Aucun indicateur équivalent. Au lieu de cela, appelez [**IMFSample :: GetSampleTime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampletime) sur l’exemple.                                        |
| **DMO \_ données de sortie \_ \_ BUFFERF \_ TIMELENGTH** | Aucun indicateur équivalent. Au lieu de cela, appelez [**IMFSample :: GetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampleduration) sur l’exemple.                                |
| **DMO \_ données de sortie \_ \_ BUFFERF \_ incomplètes** | **\_mémoire tampon de données de sortie MFT \_ \_ \_ incomplète**                                                                                                           |
| Aucun indicateur équivalent.                        | **\_modification du \_ \_ format de mémoire tampon des données de \_ sortie MFT \_**                                                                                                       |
| Aucun indicateur équivalent.                        | **\_fin du \_ \_ flux de mémoire tampon des données de \_ sortie MFT \_**                                                                                                          |
| Aucun indicateur équivalent.                        | **\_exemple de \_ \_ mémoire tampon \_ de données de sortie MFT \_**                                                                                                           |



 

### <a name="getinputstatus-flags"></a>Indicateurs GetInputStatus

DMOs : DMO énumération **\_ \_ d' \_ \_ indicateurs d’état d’entrée** .

MFTs : énumération [**\_ \_ d' \_ \_ indicateurs d’état d’entrée MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_status_flags) .



| indicateur de DMO                              | Indicateur MFT                             |
|---------------------------------------|--------------------------------------|
| **DMO \_ ENTRÉE \_ STATUSF \_ accepter les \_ données** | **l' \_ État d’entrée MFT \_ \_ accepte les \_ données** |



 

### <a name="getoutputstatus-flags"></a>Indicateurs GetOutputStatus

DMOs : aucune énumération équivalente.

MFTs : énumération des [**\_ \_ indicateurs d' \_ état \_ de sortie MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_status_flags) .



| indicateur de DMO            | Indicateur MFT                               |
|---------------------|----------------------------------------|
| Aucun indicateur équivalent. | **\_exemple d’état de sortie MFT \_ \_ \_ prêt** |



 

### <a name="getinputstreaminfo-flags"></a>Indicateurs GetInputStreamInfo

DMOs : DMO de l’énumération des [**\_ \_ \_ informations de flux \_ \_ d’entrée**](/previous-versions/windows/embedded/aa451600(v=msdn.10)) .

MFTs : [**\_ \_ informations de flux d’entrée MFT \_ \_ \_**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_stream_info_flags) énumération des indicateurs.



| indicateur de DMO                                             | Indicateur MFT                                            |
|------------------------------------------------------|-----------------------------------------------------|
| **DMO \_ exemples d’entrée \_ STREAMF \_ entière \_**              | **\_ \_ exemples complets de flux d’entrée \_ MFT \_**              |
| **DMO \_ exemple d’entrée \_ STREAMF \_ unique \_ \_ par \_ mémoire tampon** | **\_exemple unique de flux d’entrée MFT \_ \_ \_ \_ par \_ mémoire tampon** |
| **DMO \_ \_taille d' \_ \_ échantillon fixe \_ d’entrée STREAMF**         | **\_taille d' \_ \_ échantillon fixe \_ de flux d’entrée MFT \_**         |
| **DMO \_ le \_ STREAMF d’entrée \_ contient des \_ tampons**              | **le \_ flux d’entrée MFT \_ \_ contient des \_ tampons**              |
| Aucun indicateur équivalent.                                  | **le \_ flux d’entrée MFT \_ \_ ne fait \_ pas de \_ ADDREF**           |
| Aucun indicateur équivalent.                                  | **\_flux d’entrée MFT \_ \_ amovible**                   |
| Aucun indicateur équivalent.                                  | **\_flux d’entrée MFT \_ \_ facultatif**                    |



 

### <a name="getoutputstreaminfo-flags"></a>Indicateurs GetOutputStreamInfo

DMOs : DMO de l’énumération d' [**\_ \_ informations de \_ flux \_ \_ de sortie**](/previous-versions/ms806053(v=msdn.10)) .

MFTs : l’énumération des [**\_ \_ informations de flux de sortie \_ \_ \_ MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags) est l’énumération.



| indicateur de DMO                                              | Indicateur MFT                                             |
|-------------------------------------------------------|------------------------------------------------------|
| **DMO \_ \_échantillons de STREAMF \_ entier \_ de sortie**              | **\_exemples de flux de sortie MFT \_ \_ complets \_**              |
| **DMO \_ exemple de sortie \_ STREAMF \_ unique \_ \_ par \_ mémoire tampon** | **\_exemple de flux de sortie MFT \_ \_ unique \_ \_ par \_ mémoire tampon** |
| **DMO \_ \_taille d' \_ \_ échantillon fixe STREAMF de \_ sortie**         | **\_taille d' \_ \_ échantillon fixe \_ du flux de sortie MFT \_**         |
| **DMO \_ SORTIE \_ STREAMF \_ Ignorable**                 | **\_flux de sortie MFT \_ \_ ignoré**                 |
| **DMO \_ STREAMF de sortie \_ \_ facultatif**                    | **\_flux de sortie MFT \_ \_ facultatif**                    |
| Aucun indicateur équivalent.                                   | **le \_ flux de sortie MFT \_ fournit des \_ \_ exemples**           |
| Aucun indicateur équivalent.                                   | **le \_ flux de sortie MFT \_ \_ peut \_ fournir des \_ exemples**       |
| Aucun indicateur équivalent.                                   | **\_ \_ \_ lecture différée du flux de sortie MFT \_**                  |
| Aucun indicateur équivalent.                                   | **\_flux de sortie MFT \_ \_ amovible**                   |



 

### <a name="setinputtypesetoutputtype-flags"></a>Indicateurs SetInputType/SetOutputType

DMOs : DMO de définir l’énumération des [**\_ \_ \_ \_ indicateurs de TYPE**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_set_type_flags) .

MFTs : énumération des indicateurs de type de l' [**\_ \_ ensemble \_ \_ MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_set_type_flags) .



| indicateur de DMO                        | Indicateur MFT                                                                             |
|---------------------------------|--------------------------------------------------------------------------------------|
| **DMO \_ DÉFINIR \_ le \_ test TYPEF \_ uniquement** | **\_test de type d’ensemble MFT \_ \_ \_ uniquement**                                                       |
| **DMO \_ DÉFINIR \_ TYPEF \_ Clear**      | Aucun indicateur équivalent. Au lieu de cela, définissez le type de média sur **null** pour effacer le type de média. |



 

## <a name="error-codes"></a>Codes d’erreur

le tableau suivant montre comment mapper DMO codes d’erreur aux codes d’erreur MFT. un objet MFT/DMO hybride doit retourner les codes d’erreur DMO à partir des méthodes [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) et les codes d’erreur MFT des méthodes [**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) . les codes d’erreur DMO sont définis dans le fichier d’en-tête MediaErr. h. Les codes d’erreur MFT sont définis dans le fichier d’en-tête mferror. h.



| code d’erreur DMO                  | Code d’erreur MFT                       |
|---------------------------------|--------------------------------------|
| **DMO \_ \_INVALIDTYPE E**         | **\_INVALIDTYPE MF E \_**               |
| **DMO \_ \_INVALIDSTREAMINDEX E**  | **\_INVALIDSTREAMNUMBER MF E \_**       |
| **DMO \_ \_NOTACCEPTING E**        | **\_NOTACCEPTING MF E \_**              |
| **DMO \_ E \_ aucun \_ autre \_ élément**     | **MF \_ E \_ \_ plus de \_ types**           |
| **DMO \_ \_type E \_ non \_ accepté** | **\_INVALIDMEDIATYPE MF E \_**          |
| **DMO \_ \_type E \_ non \_ défini**      | **\_type de transformation MF E \_ \_ \_ non \_ défini** |



 

## <a name="creating-hybrid-dmomft-objects"></a>création d’objets/MFT hybrides DMO

L’interface [**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) est vaguement basée sur [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject), qui est l’interface principale de DirectX Media Objects (DMOs). Il est possible de créer des objets qui exposent les deux interfaces. Toutefois, cela peut entraîner des conflits de noms, car les interfaces ont des méthodes qui partagent le même nom. Vous pouvez résoudre ce problème de deux manières :

Solution 1 : incluez la ligne suivante en haut de tout fichier. cpp qui contient des fonctions MFT :

``` syntax
#define MFT_UNIQUE_METHOD_NAMES
```

Cela modifie la déclaration de l’interface [**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) de sorte que la plupart des noms de méthode aient pour préfixe « MFT ». Ainsi, [**IMFTransform ::P rocessinput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) devient **IMFTransform :: MFTProcessInput**, tandis que [**IMediaObject ::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) conserve son nom d’origine. cette technique est particulièrement utile si vous convertissez un DMO existant en DMO hybride/MFT. vous pouvez ajouter les nouvelles méthodes MFT sans modifier les méthodes de DMO.

Solution 2 : utilisez la syntaxe C++ pour lever l’ambiguïté des noms hérités de plusieurs interfaces. Par exemple, déclarez la version MFT de [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) comme suit :

``` syntax
CMyHybridObject::IMFTransform::ProcessInput(...)
```

déclarez la version DMO de [**ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) comme suit :

``` syntax
CMyHybridObject::IMediaObject::ProcessInput(...)
```

Si vous effectuez un appel interne à une méthode dans l’objet, vous pouvez utiliser cette syntaxe, mais cela remplace l’État virtuel de la méthode. Un meilleur moyen d’effectuer des appels à partir de l’objet est le suivant :

``` syntax
hr = ((IMediaObject*)this)->ProcessInput(...)
```

Ainsi, si vous dérivez une autre classe de **CMyHybridObject** et que vous remplacez la méthode CMyHybridObject :: IMediaObject ::P rocessinput, la méthode virtuelle appropriée est appelée. les interfaces DMO sont documentées dans la documentation du kit de développement logiciel (SDK) DirectShow.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transformations de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 
