---
description: Génération de nouveaux paquets de données ASF
ms.assetid: 7afa9694-c965-40e2-8549-e32ff48def2a
title: Génération de nouveaux paquets de données ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f3432ecf34c58247a1533adb202b75f59d770c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484072"
---
# <a name="generating-new-asf-data-packets"></a>Génération de nouveaux paquets de données ASF

Le *multiplexeur* ASF est un composant de couche WMContainer qui fonctionne avec l' [objet de données ASF](asf-file-structure.md) et donne à une application la possibilité de générer des paquets de données ASF pour un flux qui correspond aux exigences définies dans l’objet ContentInfo.

Le multiplexeur a une entrée et une sortie. Elle reçoit un exemple de flux qui contient des données multimédias numériques et produit un ou plusieurs paquets de données qui peuvent être écrits dans un conteneur ASF.

La liste suivante résume le processus de génération de paquets de données ASF :

1.  Transmettez les données d’entrée au multiplexeur dans [**IMFASFMultiplexer ::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample).
2.  Collectez les paquets de données en appelant [**IMFASFMultiplexer :: GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) dans une boucle jusqu’à ce que tous les paquets complets aient été récupérés.
3.  Une fois les données d’entrée converties en paquets complets, il peut y avoir des données en attente dans le multiplexeur, qui n’a pas été récupéré par [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket). Appelez [**IMFASFMultiplexer :: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) pour paqueter les exemples en attente et les collecter à partir du multiplexeur en appelant à nouveau **GetNextPacket** .
4.  Mettez à jour les objets d’en-tête ASF associés en appelant [**IMFASFMultiplexer :: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) pour refléter les modifications apportées par le multiplexeur pendant la génération des paquets de données.

Le diagramme suivant illustre la génération de paquets de données pour un fichier ASF par le biais du multiplexeur.

![Diagramme montrant la génération de paquets de données pour un fichier ASF](images/packet.gif)

## <a name="asf-data-packet-creation"></a>Création de paquets de données ASF

Après avoir créé et initialisé le multiplexeur comme décrit dans [création de l’objet multiplexeur](creating-the-multiplexer-object.md), appelez [**IMFASFMultiplexer ::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) pour transmettre des données d’entrée au multiplexeur en vue de leur traitement dans des paquets de données. L’entrée spécifiée doit se trouver dans un échantillon de média (interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) ) qui peut avoir un ou plusieurs tampons de média (interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) ) contenant les données d’un flux. Dans le cas d’un transcodage ASF-à-ASF, l’exemple de média d’entrée peut être généré à partir du séparateur qui crée des exemples de flux paquets. Pour plus d’informations, consultez [séparateur ASF](asf-splitter.md).

Avant d’appeler [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), assurez-vous que l’horodatage de l’exemple de média d’entrée est une heure de présentation valide. sinon **ProcessSample** échoue et retourne l' \_ exemple de code d’horodatage MF E \_ no \_ \_ .

Le multiplexeur peut accepter les entrées en tant qu’exemples de supports compressés ou non compressés via [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample). Le multiplexeur attribue des heures d’envoi à ces exemples en fonction de l’utilisation de la bande passante du flux. Pendant ce processus, le multiplexeur vérifie les paramètres de compartiment avec fuite (taux de bits et utilisation de la fenêtre de mémoire tampon) et peut rejeter des exemples qui n’adhèrent pas à ces valeurs. L’exemple de média d’entrée peut faire échouer la vérification de la bande passante pour l’une des raisons suivantes :

-   Si l’exemple de média d’entrée est arrivé à expiration parce que l’heure d’envoi du dernier assignée est supérieure à l’horodatage de cet exemple de support. [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) échoue et retourne l’exemple de code d’erreur **MF \_ E \_ Late \_** .
-   Si l’horodatage sur l’échantillon de média d’entrée est antérieur à l’heure d’envoi affectée (cela indique un dépassement de mémoire tampon). Le multiplexeur peut ignorer cette situation s’il est configuré pour ajuster la vitesse de transmission en définissant l’indicateur de vitesse de **\_ \_ \_ transmission** du multiplexeur MFASF au cours de l’initialisation du multiplexeur. Pour plus d’informations, consultez « initialisation du multiplexeur et paramètres des compartiments de fuites » dans [création de l’objet multiplexeur](creating-the-multiplexer-object.md). Si cet indicateur n’est pas défini et que le multiplexeur rencontre une saturation de la bande passante, [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) échoue et retourne le code d’erreur de **\_ \_ \_ dépassement de bande passante MF E** .

Une fois que le multiplexeur a affecté l’heure d’envoi, l’exemple de média d’entrée est ajouté à la *fenêtre d’envoi*, c’est-à-dire une liste d’exemples de médias d’entrée classés par heure d’envoi et prêts à être traités dans des paquets de données. Pendant la construction des paquets de données, l’exemple de média d’entrée est analysé et les données pertinentes sont écrites dans un paquet de données comme charge utile. Un paquet de données complet peut contenir des données provenant d’un ou de plusieurs exemples de supports d’entrée.

Quand de nouveaux exemples de médias d’entrée arrivent dans la fenêtre d’envoi, ils sont ajoutés à une file d’attente jusqu’à ce qu’il y ait suffisamment d’échantillons de supports pour former un paquet complet. Les données dans les mémoires tampons de média contenues par l’exemple de média d’entrée ne sont pas copiées dans le paquet de données généré. Le paquet de données conserve les références aux tampons du média d’entrée jusqu’à ce que l’exemple de média d’entrée ait été entièrement packeted et que le paquet complet ait été collecté du multiplexeur.

Lorsqu’un paquet de données complet est disponible, il peut être récupéré en appelant [**IMFASFMultiplexer :: GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket). Si vous appelez [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) alors que des paquets complets sont prêts pour la récupération, il échoue et retourne le code d’erreur **MF \_ E \_ NOTACCEPTING** . Cela indique que le multiplexeur ne peut pas accepter plus d’entrée et vous devez appeler **GetNextPacket** pour récupérer les paquets en attente. Dans l’idéal, chaque appel **ProcessSample** doit être suivi par un ou plusieurs appels **GetNextPacket** pour obtenir les paquets de données complets. Plusieurs exemples de média d’entrée peuvent être nécessaires pour créer un paquet de données complet. À l’inverse, les données d’un exemple de média d’entrée peuvent s’étendre sur plusieurs paquets. Par conséquent, tous les appels à **ProcessSample** produiront des exemples de supports de sortie.

Si l’exemple de média d’entrée contient une image clé indiquée par l’attribut [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) , le multiplexeur copie l’attribut dans le paquet.

## <a name="getting-asf-data-packets"></a>Obtention de paquets de données ASF

Pour collecter les exemples de supports de sortie pour un paquet de données complet généré par le multiplexeur, appelez [**IMFASFMultiplexer :: GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) dans une boucle jusqu’à ce qu’il n’y ait plus d’échantillons de média de sortie pour le paquet. La liste suivante répertorie les cas de réussite :

-   Si un paquet de données complet est disponible, [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) reçoit l’indicateur d' **\_ État ASF \_ \_ incomplet** dans le paramètre *pdwStatusFlags* ; le paramètre *ppIPacket* reçoit un pointeur vers le premier paquet de données. Vous devez appeler cette méthode aussi longtemps qu’elle reçoit cet indicateur. Avec chaque itération, *ppIPacket* pointe vers le paquet suivant dans la file d’attente.
-   S’il n’existe qu’un seul paquet de données, *ppIPacket* pointe vers celui-ci et l’indicateur **ASF \_ Status \_ Flags \_ incomplet** n’est pas reçu dans *pdwStatusFlags*.
-   [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) peut aboutir sans générer de paquets de données si le multiplexeur est toujours en train de transmettre et d’ajouter des paquets de données. Dans ce cas, *ppIPacket* pointe vers la **valeur null**. Pour continuer, vous devez fournir au multiplexeur plus d’exemples de supports d’entrée en appelant [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample).

L’exemple de code suivant illustre une fonction qui génère des paquets de données à l’aide du multiplexeur. Le contenu du paquet de données généré sera écrit dans le flux d’octets de données alloué par l’appelant.


```C++
//-------------------------------------------------------------------
// GenerateASFDataPackets
// 
// Gets data packets from the mux. This function is called after 
// calling IMFASFMultiplexer::ProcessSample. 
//-------------------------------------------------------------------

HRESULT GenerateASFDataPackets( 
    IMFASFMultiplexer *pMux, 
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;

    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacketBuffer = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pOutputSample)
        {
            //Convert to contiguous buffer
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacketBuffer);
            
            if (FAILED(hr))
            {
                break;
            }

            //Write buffer to byte stream
            hr = WriteBufferToByteStream(pDataStream, pDataPacketBuffer, NULL);

            if (FAILED(hr))
            {
                break;
            }
        }

        SafeRelease(&pDataPacketBuffer);
        SafeRelease(&pOutputSample);
    }

    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacketBuffer);
    return hr;
}
```



La `WriteBufferToByteStream` fonction est présentée dans la rubrique [**IMFByteStream :: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).

Pour voir une application complète qui utilise cet exemple de code, consultez [Didacticiel : copie de flux de fichiers ASF d’un fichier vers un autre](tutorial--copying-asf-streams-from-one-file-to-another.md).

## <a name="post-packet-generation-calls"></a>Appels de Packet-Generation de publication

Pour vous assurer qu’il n’y a pas de paquets de données complets en attente dans le multiplexeur, appelez [**IMFASFMultiplexer :: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush). Cela force le multiplexeur à empaqueter tous les exemples de supports en cours. L’application peut collecter ces paquets sous forme d’échantillons de médias via **GetNextPacket** dans une boucle jusqu’à ce qu’il n’y ait plus aucun paquet à récupérer.

Une fois tous les exemples de médias générés, appelez [**IMFASFMultiplexer :: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) pour mettre à jour l’objet d’en-tête ASF associé à ces paquets de données. L’objet d’en-tête est spécifié en passant l’objet ContentInfo qui a été utilisé pour initialiser le multiplexeur. Cet appel met à jour différents objets d’en-tête pour refléter les modifications apportées par le multiplexeur pendant la génération des paquets de données. Ces informations incluent le nombre de paquets, la durée d’envoi, la durée de lecture et les numéros de flux de tous les flux. La taille globale de l’en-tête est également mise à jour.

Vous devez vous assurer que [**end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) est appelé après que tous les paquets de données ont été récupérés. Si des paquets sont en attente dans le multiplexeur, **end** échoue et retourne le code d’erreur **MF \_ E \_ flush \_ requis** . Dans ce cas, récupérez le paquet en attente en appelant [**flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) et [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) dans une boucle.

> [!Note]  
> Pour l’encodage VBR, après avoir appelé **end**, vous devez définir les statistiques d’encodage dans les propriétés d’encodage de l’objet ContentInfo. Pour plus d’informations sur ce processus, consultez « Configuration de l’objet ContentInfo avec les paramètres de l’encodeur » dans [définition des propriétés dans l’objet ContentInfo](setting-properties-in-the-contentinfo-object.md). La liste suivante répertorie les propriétés spécifiques à définir :
>
> -   [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md) est la vitesse de transmission moyenne du contenu VBR.
> -   [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md) est la fenêtre de mémoire tampon pour la vitesse de transmission moyenne.
> -   [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md) est le taux binaire de pointe du contenu VBR.
> -   [**MFPKEY \_ BMAX**](mfpkey-bmaxproperty.md) est la fenêtre de mémoire tampon de pointe.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Multiplexeur ASF](asf-multiplexer.md)
</dt> <dt>

[Didacticiel : copie de flux de fichiers ASF d’un fichier à un autre](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[Didacticiel : écriture d’un fichier WMA à l’aide de l’encodage CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



