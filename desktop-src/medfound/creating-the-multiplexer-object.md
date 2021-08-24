---
description: Création de l’objet multiplexeur
ms.assetid: a5adc40c-abb4-4012-b6f2-eb871eaed7b9
title: Création de l’objet multiplexeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aedf314a63e9475342a7a2091e1d8531bc5bb2839f8c53ae71fa760cdd58b32e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942939"
---
# <a name="creating-the-multiplexer-object"></a>Création de l’objet multiplexeur

Le multiplexeur ASF est un objet de couche WMContainer qui fonctionne avec l' [objet de données ASF](asf-file-structure.md) et donne à une application la possibilité de générer des paquets de données ASF pour les flux de données multimédias.

L’objet multiplexeur expose l’interface [**IMFASFMultiplexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) . Pour créer le multiplexeur, appelez [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer). Cette fonction retourne un pointeur vers un objet vide. Si l’application écrit un nouveau fichier ASF, l’application doit initialiser le multiplexeur avec un objet ContentInfo. Pour ce faire, appelez [**IMFASFMultiplexer :: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize). L’objet ContentInfo spécifié représente l’objet d’en-tête ASF du nouveau fichier. Pour plus d’informations sur la création et l’initialisation de l’objet ContentInfo pour un nouveau fichier, consultez [initialisation de l’objet ContentInfo d’un nouveau fichier ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md).

La méthode [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) analyse l’objet ContentInfo pour collecter des informations de configuration de flux, telles que le nombre de flux, la taille de paquet, le préroll. Éventuellement, le multiplexeur peut également avoir besoin de paramètres de compartiment avec fuite et les unités d’extension de charge utile. Ces informations sont nécessaires pour générer des paquets de données qui correspondent aux spécifications définies dans l’objet d’en-tête ASF. La méthode **Initialize** configure le multiplexeur en fonction du type de média et des paramètres de configuration des flux. par exemple, si un flux est configuré pour avoir des extensions de charge utile (voir [création et configuration de Flux ASF](creating-and-configuring-asf-streams.md)), puis le multiplexeur est configuré pour ajouter ces valeurs aux paquets de données générés.

La méthode [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) obtient également un handle vers l’objet de données initial qui a été créé lors de la création de l’objet ContentInfo en écriture. Pendant la génération des paquets de données, le multiplexeur ajoute des paquets à l’objet de données et le met à jour de manière appropriée. Une fois que le multiplexeur a généré tous les paquets de données, il met à jour l’objet ContentInfo fourni afin que certaines valeurs, telles que le nombre de paquets de données, soient mises à jour.

L’exemple de code suivant montre comment créer un multiplexeur et l’initialiser avec un objet ContentInfo.


```C++
//-------------------------------------------------------------------
// CreateOutputGenerators
//
// Creates the ASF mux and the ASF Content Info object for the 
// output file.
//-------------------------------------------------------------------

HRESULT CreateOutputGenerators(
    IMFASFProfile *pProfile, 
    IMFASFContentInfo **ppContentInfo, 
    IMFASFMultiplexer **ppMux
    )
{
    IMFASFContentInfo *pContentInfo = NULL;
    IMFASFMultiplexer *pMux = NULL;

    // Use the ASF profile to create the ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);

    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->SetProfile(pProfile);
    }

    // Create the ASF Multiplexer object.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFMultiplexer(&pMux);
    }
    
    // Initialize it using the new ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Initialize(pContentInfo);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();

        *ppMux = pMux;
        (*ppMux)->AddRef();
    }

    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);

    return hr;
}
```



pour voir cette fonction utilisée dans une application complète, consultez [didacticiel : copie de Flux ASF d’un fichier vers un autre](tutorial--copying-asf-streams-from-one-file-to-another.md).

## <a name="multiplexer-initialization-and-leaky-bucket-settings"></a>initialisation du multiplexeur et compartiment de fuite Paramètres

La méthode [**IMFASFMultiplexer :: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) configure le multiplexeur pour déterminer le flot de données de compartiments avec fuite. Pour configurer ces paramètres, assurez-vous que les valeurs de propriété suivantes sont définies sur l’objet ContentInfo spécifié. Pour plus d’informations sur la définition de ces propriétés, consultez [définition des propriétés dans l’objet ContentInfo](setting-properties-in-the-contentinfo-object.md).

-   [**MFPKEY \_ ASFMEDIASINK propriété \_ \_ vitesse de transmission**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) automatique : indique si le multiplexeur doit ajuster automatiquement la vitesse de transmission, pour maintenir le workflow dans le compartiment avec fuite. Ce paramètre peut être modifié par l’application en appelant [**IMFASFMultiplexer :: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) et en passant l’indicateur de **\_ vitesse de \_ \_ transmission du multiplexeur MFASF** .

-   [**MFPKEY \_ ASFMEDIASINK \_ base \_ SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md) Property : l’heure d’envoi indique quand la charge utile dans le compartiment avec fuite est libérée. Les heures d’envoi doivent être supérieures ou égales à l’heure de la présentation, car la charge utile doit avoir le temps d’accéder à la destination avant l’heure de la présentation.

    Cette valeur de propriété est la première heure d’envoi. Le multiplexeur utilise cette valeur pour calculer les heures d’envoi suivantes afin de s’assurer que les données transitent régulièrement par le compartiment. Si l’indicateur de **\_ \_ \_ débit binaire MFASF du multiplexeur** est défini sur le multiplexeur, le multiplexeur ajuste la vitesse de transmission afin que la charge utile soit envoyée lorsque la fenêtre de la mémoire tampon est pleine. Si l’indicateur n’est pas défini, le multiplexeur ne parvient pas à générer des paquets de données en raison d’un dépassement de bande passante.

Le multiplexeur obtient des informations de configuration de flux à partir du profil ASF associé à l’objet ContentInfo spécifié dans la méthode [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) . Les informations de configuration de flux incluent des paramètres de compartiments perdus. Cette valeur est requise par le multiplexeur pour générer des paquets de données.

Pour spécifier les paramètres de compartiment à fuite, définissez les valeurs de l’attribut [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) sur l’objet de configuration de flux qui représente le flux dans le profil. Pour utiliser la valeur de la fenêtre de mémoire tampon, qui est utilisée par l’encodeur, appelez [**IWMCodecLeakyBucket :: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md). La valeur réelle de la fenêtre de la mémoire tampon est connue uniquement après la définition du type de média de sortie de l’encodeur. Pour plus d’informations sur la définition du type de média de sortie, consultez [négociation de type de média sur l’encodeur](media-type-negotiation-on-the-encoder.md).

> [!Note]  
> Les valeurs de compartiment fuites utilisées par l’encodeur peuvent être différentes dans l’objet ContentInfo fourni par le profil ASF utilisé pour créer le multiplexeur.

 

La méthode [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) met à jour l’objet ContentInfo afin que les valeurs correctes soient reflétées dans l’objet d’en-tête ASF final.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Multiplexeur ASF](asf-multiplexer.md)
</dt> <dt>

[Génération de nouveaux paquets de données ASF](generating-new-asf-data-packets.md)
</dt> </dl>

 

 
