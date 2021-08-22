---
description: Génération d’exemples de flux à partir d’un objet de données ASF existant
ms.assetid: eb27f122-d958-495d-98ea-8befd105a9a8
title: Génération d’exemples de flux à partir d’un objet de données ASF existant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97fb99440c3fc4721851f183b3bfc7aefafd3f652d0436b29e9cea1209ba59b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974448"
---
# <a name="generating-stream-samples-from-an-existing-asf-data-object"></a>Génération d’exemples de flux à partir d’un objet de données ASF existant

L’objet *séparateur* ASF est un composant de couche WMContainer qui analyse l’objet de données ASF d’un fichier ASF (Advanced Systems Format).

Avant de passer des paquets de données au séparateur, l’application doit initialiser, configurer et sélectionner des flux sur le séparateur afin de le préparer pour le processus d’analyse. Pour plus d’informations, consultez [création de l’objet Splitter ASF](creating-the-asf-splitter-object.md) et [configuration de l’objet Splitter ASF](configuring-the-asf-splitter-object.md).

Les méthodes requises pour l’analyse de l’objet de données ASF sont les suivantes :

-   [**IMFASFSplitter ::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) qui démarre le processus d’analyse en poussant le tampon contenant les paquets de données vers le séparateur.
-   [**IMFASFSplitter :: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) qui collecte les exemples de flux générés à partir de la mémoire tampon transmise au séparateur.

## <a name="finding-the-data-offset"></a>Recherche du décalage des données

Avant de commencer le processus d’analyse, l’application doit localiser l’objet de données dans le fichier ASF. Il existe deux façons d’afficher le décalage de l’objet de données à partir du début du fichier :

-   Avant d’initialiser l’objet ContentInfo, vous pouvez appeler la méthode [**IMFASFContentInfo :: GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) . Cette méthode requiert une mémoire tampon qui contient les 30 premiers octets de l’en-tête ASF. Elle retourne la taille de l’en-tête entier qui indique le décalage par rapport au premier paquet de données. Cette valeur comprend également la taille de l’en-tête de l’objet de données de 50 octets.
-   Une fois que vous avez initialisé l’objet ContentInfo, vous pouvez obtenir le descripteur de présentation en appelant [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor), puis en interrogeant le descripteur de présentation pour l’attribut de [**\_ décalage de \_ \_ \_ début \_ de données ASF pour MF PD**](mf-pd-asf-data-start-offset-attribute.md) . La valeur de cet attribut correspond à la taille de l’en-tête.
    > [!Note]  
    > L’attribut de [**\_ \_ \_ \_ longueur de données ASF PD ASF**](mf-pd-asf-data-length-attribute.md) sur le descripteur de présentation spécifie la longueur de l’objet de données ASF.

     

Dans les deux cas, la valeur retournée est la taille de l’objet d’en-tête plus la taille de la section d’en-tête de l’objet de données. Par conséquent, la valeur résultante est le décalage au début des paquets de données dans l’objet de données ASF. Lorsque vous commencez à envoyer des données au séparateur, les données doivent commencer à ce décalage à partir du début du fichier ASF.

La valeur de décalage est passée en tant que paramètre à **ParseData** qui démarre le processus d’analyse.

L’objet de données est divisé en paquets de données. Chaque paquet de données contient un en-tête de paquet de données qui fournit des informations d’analyse de paquets et les données de charge utile, les données de support numérique réelles. Dans un scénario de recherche, l’application peut souhaiter que le séparateur commence l’analyse au niveau d’un paquet de données particulier. Pour ce faire, vous pouvez utiliser l’indexeur ASF pour récupérer le décalage. L’indexeur retourne une valeur de décalage qui commence à la limite du paquet. Si vous n’utilisez pas l’indexeur, assurez-vous que l’offset commence au début de l’en-tête de paquet de données. Si un décalage non valide est passé au séparateur, par exemple si la valeur ne pointe pas vers la limite du paquet, les appels **ParseHeader** et **GetNextSample** réussissent mais **GetNextSample** ne récupère aucun échantillon et la **valeur null** est reçue dans le paramètre *pSample* .

Si le séparateur est configuré pour analyser dans le sens inverse, le séparateur commence toujours l’analyse à la fin de la mémoire tampon du média qui est transmise à **ParseData**. Par conséquent, pour l’analyse inverse dans l’appel à **ParseData**, transmettez l’offset dans le paramètre *cbLength* , qui spécifie la longueur des données et définissez *cbBufferOffset* sur zéro.

## <a name="generating-samples-for-asf-data-packets"></a>Génération d’exemples pour les paquets de données ASF

Une application démarre le processus d’analyse en passant les paquets de données au séparateur. L’entrée du séparateur est une série de mémoires tampons de média qui contiennent l’intégralité ou les fragments de l’objet de données. La sortie du séparateur est une série d’exemples de médias qui contiennent les données du paquet.

Pour transmettre des données d’entrée au séparateur, créez une mémoire tampon de média et remplissez-la avec les données de la section de l’objet de données du fichier ASF. (Pour plus d’informations sur les mémoires tampons de média, consultez [mémoires tampons de média](media-buffers.md).) Ensuite, transmettez la mémoire tampon du média à la méthode [**IMFASFSplitter ::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) . Vous pouvez également spécifier :

-   Offset dans la mémoire tampon où le séparateur doit commencer l’analyse. Si le décalage est égal à zéro, l’analyse commence au début de la mémoire tampon. Pour plus d’informations sur la définition du décalage des données, consultez la section « recherche de l’offset des données » dans cette rubrique.
-   Quantité de données à analyser. Si cette valeur est égale à zéro, le séparateur est analysé jusqu’à ce qu’il atteigne la fin de la mémoire tampon, comme spécifié par la méthode [**IMFMediaBuffer :: GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) .

Le séparateur génère des exemples de médias en référençant les données dans les mémoires tampons du média. Le client peut récupérer les exemples de sortie en appelant [**IMFASFSplitter :: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) dans une boucle jusqu’à ce qu’il n’y ait plus de données à analyser. Si **GetNextSample** retourne l' \_ indicateur ASF STATUSFLAGS \_ incomplet dans le paramètre *pdwStatusFlags* , cela signifie qu’il y a plus d’échantillons à récupérer, et que l’application peut appeler de nouveau **GetNextSample** . Sinon, appelez **ParseData** pour transmettre plus de données au séparateur. Pour les exemples générés, le séparateur définit les informations suivantes :

-   Le séparateur définit un horodatage sur tous les exemples qu’il génère. L’heure de l’exemple représente l’heure de présentation et n’inclut pas le temps de préroll. L’application peut appeler [**IMFSample :: GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) pour connaître l’heure de présentation, en unités de 100 nanosecondes.
-   Si une interruption se produit pendant la génération de l’échantillon, le séparateur définit l’attribut de [**\_ discontinuité MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) sur le premier échantillon après la discontinuation. Les discontinuités sont généralement dues à des paquets ignorés sur une connexion réseau, à des données de fichier endommagées ou à un déplacement de fractionnement d’un flux source à un autre.
-   Pour la vidéo, le séparateur vérifie si l’échantillon contient une image clé. Si c’est le cas, le séparateur définit l’attribut [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) sur l’exemple.

Si le séparateur analyse les paquets de données reçus d’un serveur multimédia, il est possible que la longueur du paquet soit variable. Dans ce cas, le client doit appeler **ParseData** pour chaque paquet et définir l’attribut de [**\_ \_ limite de paquet MFASFSPLITTER**](mfasfsplitter-packet-boundary-attribute.md) sur chaque mémoire tampon qui est envoyée au séparateur. Cet attribut indique au séparateur si la mémoire tampon du média contient le début d’un paquet ASF. Affectez la **valeur true** à l’attribut si la mémoire tampon contient le début d’un nouveau paquet. Si la mémoire tampon contient une continuation du paquet précédent, affectez la valeur **false** à l’attribut. Les mémoires tampons ne peuvent pas couvrir plusieurs paquets.

Avant de passer de nouvelles mémoires tampons de média au séparateur, l’application doit appeler [**IMFASFSplitter :: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush). Cette méthode réinitialise le séparateur et efface tout Frame partiel en attente d’achèvement. Cela est utile dans un scénario de recherche où le décalage se trouve à un emplacement différent.

### <a name="example"></a>Exemple

L’exemple de code suivant montre comment analyser des paquets de données. Cet exemple analyse à partir du début de l’objet de données jusqu’à la fin du flux et affiche des informations sur les exemples qui contiennent des images clés. Pour obtenir un exemple complet qui utilise ce code, consultez [Didacticiel : lecture d’un fichier ASF](tutorial--reading-an-asf-file.md).


```C++
// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Séparateur ASF](asf-splitter.md)
</dt> </dl>

 

 



