---
description: Le récepteur de fichiers ASF est une implémentation de IMFMediaSink fournie par Media Foundation qu’une application peut utiliser pour archiver des données de média ASF dans un fichier. Pour plus d’informations sur le modèle objet des récepteurs de média ASF et l’utilisation générale, consultez récepteurs de média ASF.
ms.assetid: 21cbde27-a2ca-4298-9197-43bcaf05588d
title: Ajout d’informations de flux au récepteur de fichiers ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e08c6997d9c77836f379d4ca7b75720ddea245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513402"
---
# <a name="adding-stream-information-to-the-asf-file-sink"></a>Ajout d’informations de flux au récepteur de fichiers ASF

Le récepteur de fichiers ASF est une implémentation de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fournie par Media Foundation qu’une application peut utiliser pour archiver des données de média ASF dans un fichier. Pour plus d’informations sur le modèle objet et l’utilisation générale des récepteurs de média ASF, consultez [récepteurs de média ASF](asf-media-sinks.md).

Après avoir instancié le récepteur de fichiers, vous devez le configurer avant de générer la topologie. Le récepteur de fichiers doit connaître les flux de données dans le fichier de sortie, les informations sur le mode d’encodage et les métadonnées. Cette rubrique décrit le processus d’ajout de flux dans le récepteur de fichiers.

-   [Ajout de flux dans le récepteur de fichiers ASF](#adding-streams-in-the-asf-file-sink)
-   [Énumération des récepteurs de flux](#enumerating-stream-sinks)
-   [Rubriques connexes](#related-topics)

## <a name="adding-streams-in-the-asf-file-sink"></a>Ajout de flux dans le récepteur de fichiers ASF

Le récepteur de fichiers doit connaître les flux de sortie et leurs propriétés afin de pouvoir générer des exemples de sortie en conséquence et les ajouter au fichier ASF de sortie. Ces paramètres sont écrits dans l’objet d’en-tête ASF final.

Pour définir des informations de flux, vous devez avoir une référence à l’objet ASF ContentInfo du récepteur de fichiers. Pour plus d’informations, consultez [création du récepteur de fichiers ASF](creating-the-asf-file-sink.md).

La procédure suivante résume les étapes générales de la configuration de Stream à l’aide de l’objet de profil ASF.

**Pour configurer les informations de flux dans le récepteur de fichiers ASF**

1.  Créez un objet de profil ASF en appelant [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).
2.  Pour chaque flux du fichier de sortie, créez un type de média pour le flux cible à ajouter dans le récepteur de fichiers. Le type de média doit être compatible avec les types de sortie pris en charge par les encodeurs Windows Media.

    Pour plus d’informations sur l’ajout de flux audio au profil, consultez Création de flux audio pour l’encodage ASF.

    Pour plus d’informations sur l’ajout de flux vidéo au profil, consultez Création de flux vidéo pour l’encodage ASF.

3.  Créez des flux basés sur les types de médias créés à l’étape 2 en appelant [**IMFASFProfile :: CreateStream,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).
4.  Assignez un numéro de flux pour le flux nouvellement créé en appelant le pointeur d’interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) reçu à l’étape 3.
5.  Éventuellement, configurez le flux avec les informations suivantes :
    -   Paramètres de compartiment avec fuite en définissant les attributs : [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) ou [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
    -   Extension de charge utile, exclusion mutuelle en appelant des méthodes [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .
6.  Vous pouvez également définir la taille des paquets de données pour le profil en définissant les attributs [**MF \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) et [**MF \_ ASFPROFILE \_ MaxPacketSize**](mf-asfprofile-maxpacketsize-attribute.md) . Le profil ASF expose l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , à laquelle une application peut se procurer une référence en appelant **IMFASFProfile :: QueryInterface**.
7.  Définissez les informations d’encodage du flux dans le récepteur de fichiers. Décrit dans [définition des propriétés dans le récepteur de fichiers](setting-properties-in-the-file-sink.md).
8.  Ajoutez le flux au profil en appelant [**IMFASFProfile :: SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).
9.  Associez le profil à l’objet ContentInfo en appelant [**IMFASFContentInfo :: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).

Pour modifier un flux existant, l’application peut obtenir une référence à l’interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) du flux et la reconfigurer conformément aux exigences. Pour ajouter ou supprimer des flux, l’application doit appeler [**IMFASFProfile :: RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream). Pour appliquer ces modifications, modifier ou supprimer le flux, vous devez redéfinir le profil dans l’objet ContentInfo. Cela remplace le profil existant qui est déjà associé à l’objet ContentInfo.


```C++
//-------------------------------------------------------------------
//  CreateVideoStream
//  Create an video stream and add it to the profile.
//
//  pProfile: A pointer to the ASF profile.
//  wStreamNumber: Stream number to assign for the new stream.
//    pType: A pointer to the source's video media type.
//-------------------------------------------------------------------

HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
{
    if (!pProfile)
    {
        return E_INVALIDARG;
    }
    if (wStreamNumber < 1 || wStreamNumber > 127 )
    {
        return MF_E_INVALIDSTREAMNUMBER;
    }

    HRESULT hr = S_OK;

    
    IMFMediaType* pVideoType = NULL;
    IMFASFStreamConfig* pVideoStream = NULL;

    UINT32 dwBitRate = 0;
        
    //Create a new video type from the source type
    hr = CreateCompressedVideoType(pType, &pVideoType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create a new stream with the video type
    hr = pProfile->CreateStream(pVideoType, &pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }
    

    //Set a valid stream number
    hr = pVideoStream->SetStreamNumber(wStreamNumber);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile
    hr = pProfile->SetStream(pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }

    wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

done:

    SafeRelease(&pVideoStream);
    SafeRelease(&pVideoType);

    return hr;
}
```



## <a name="enumerating-stream-sinks"></a>Énumération des récepteurs de flux

Pour chaque flux du profil dont l’objet ContentInfo est conscient, le récepteur de fichiers ASF crée et ajoute un récepteur de flux qui contient toutes les propriétés du flux encodé. Le récepteur de fichiers ASF est conçu pour contenir des flux fixes. Cela signifie que vous ne pouvez pas ajouter ou supprimer des flux en appelant [**IMFMediaSink :: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) ou [**IMFMediaSink :: RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink). Ces appels sur le récepteur de fichiers échouent avec \_ le \_ code d’erreur fixe MF E STREAMSINKS \_ . L’ajout ou la suppression de flux dans le profil n’ajoute pas ou ne supprime pas automatiquement les récepteurs de flux dans le récepteur de fichiers. Vous devez ignorer l’instance existante du fichier et la recréer avec les nouvelles informations de flux si vos flux du profil ont été modifiés.

La procédure suivante résume les étapes générales pour l’énumération des récepteurs de flux dans le récepteur de fichiers ASF.

**Pour énumérer des récepteurs de flux**

1.  Appelez [**IMFMediaSink :: GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) pour connaître le nombre total de récepteurs de flux dans le récepteur de fichiers ASF.
2.  Parcourez les récepteurs de flux ang pour obtenir une référence à l’interface [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) du récepteur de flux.

    -ou-

    Appelez [**IMFMediaSink :: GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) pour récupérer le récepteur de flux en spécifiant le numéro de flux. Chaque récepteur de flux est identifié par le numéro de flux que vous définissez lors de la création du flux dans le profil.

Si vous générez une topologie partielle pour l’encodage d’un fichier multimédia, vous devez ajouter le récepteur de fichiers à la topologie en tant que nœud de topologie de sortie. Vous pouvez le faire en spécifiant chaque récepteur de vapeur dans le récepteur de fichiers ou en définissant l’objet d’activation du récepteur de fichiers et les identificateurs du récepteur de flux. Pour plus d’informations et pour obtenir un exemple de code, consultez [création de nœuds de sortie](creating-output-nodes.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Récepteurs de média ASF](asf-media-sinks.md)
</dt> <dt>

[Prise en charge ASF dans Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



