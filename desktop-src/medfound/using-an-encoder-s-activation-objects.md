---
description: pour convertir des fichiers multimédias au format ASF, vous pouvez utiliser des encodeurs Windows media. En savoir plus sur l’utilisation des objets d’activation d’un encodeur.
ms.assetid: 18c26619-6047-4f7f-bb65-ca418f02e5b1
title: Utilisation d’objets d’activation d’encodeurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24915020c1b888be6a1aeaca1e21af95d11cfc181a5c00a91c8359c3f780fa0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972738"
---
# <a name="using-an-encoders-activation-objects"></a>Utilisation des objets d’activation d’un encodeur

pour convertir des fichiers multimédias au format ASF, vous pouvez utiliser des encodeurs Windows media. Pour utiliser ces encodeurs, ceux-ci doivent être inscrits auprès du système.

Pour plus d’informations sur l’inscription de l’encodeur, consultez [instanciation d’un encodeur MFT](instantiating-the-encoder-mft.md).

-   [Utilisation des objets d’activation d’un encodeur](#using-an-encoders-activation-objects)
-   [énumération d’encodeurs dans Windows 7 et versions ultérieures](#encoder-enumeration-in-windows-7-and-later)
-   [Rubriques connexes](#related-topics)

## <a name="using-an-encoders-activation-objects"></a>Utilisation des objets d’activation d’un encodeur

En guise d’alternative à l’utilisation de l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) d’un encodeur (décrite dans [création d’un encodeur à l’aide de CoCreateInstance](using-an-encoder-s-imftransform--interface.md)), vous pouvez créer une instance de l’objet d’activation pour l’encodeur. Les objets d’activation facilitent la création de l’encodeur et Media Foundation fournissent les deux fonctions suivantes pour cette approche :

-   [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) pour l’instanciation de l’encodeur audio multimédia Windows.
-   [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) pour l’instanciation de l’encodeur vidéo multimédia Windows.

Ces deux fonctions nécessitent la création du type de média cible et la définition des propriétés d’encodage avant l’appel de ces fonctions. Si votre application utilise des [composants ASF de couche de pipeline](pipeline-layer-asf-components.md) pour encoder un fichier au format ASF et que vous avez déjà créé et configuré les [récepteurs de média ASF](asf-media-sinks.md), vous pouvez obtenir cet ensemble d’informations à partir du récepteur multimédia ASF.

[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) et [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) définissent le type de sortie de l’encodeur sur le type de média spécifié par l’application.

**Remarque**  Si vous utilisez [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) et [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) , vous pouvez activer l’encodeur en appelant [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) , mais vous ne pouvez pas modifier les types de média d’entrée et de sortie de l’encodeur, ni modifier les propriétés d’encodage.

Pour plus d’informations sur la création d’objets Media Foundation à l’aide d’objets d’activation, consultez [objets d’activation](activation-objects.md).

**Pour récupérer le type de média cible à partir du récepteur multimédia ASF**

1.  Obtenir un pointeur vers le pointeur [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) du récepteur de média ASF en appelant **IMFMediaSink :: QueryInterface** sur le récepteur de média ASF et en passant **IID \_ IMFASFContentInfo** comme identificateur d’interface.
2.  Obtient l’objet de profil ASF associé à l’objet ContentInfo.
3.  Énumérez les flux dans le profil pour récupérer le type de média du flux.

**Pour récupérer les propriétés d’encodage à partir du récepteur multimédia ASF**

1.  Si vous avez configuré les [propriétés d’encodage](configuring-the-encoder.md) dans le récepteur multimédia (décrit dans [définition des propriétés dans le récepteur de fichiers](setting-properties-in-the-file-sink.md)), vous pouvez référencer la Banque de propriétés du récepteur en appelant **IMFMediaSink :: QueryInterface** sur le récepteur de média ASF et en passant **IID \_ IPropertyStore** comme identificateur d’interface.
2.  Si vous avez un pointeur vers l’objet ContentInfo du récepteur, vous pouvez appeler [**IMFASFContentInfo :: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) pour obtenir une référence à la Banque de propriétés du récepteur multimédia.

    Assurez-vous que toutes les propriétés d’encodage définies sur le récepteur de média ASF sont reflétées dans la Banque de propriétés passée à [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) et [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate). L’encodeur est configuré automatiquement en fonction des paramètres spécifiés par l’application.

Lors de la création du nœud transformer dans la topologie d’encodage, vous pouvez définir le type d’objet en tant que pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) reçu dans ces deux appels. Lorsque la topologie est résolue, la session multimédia utilise l’objet d’activation pour créer une instance de la MFT de l’encodeur.

## <a name="encoder-enumeration-in-windows-7-and-later"></a>énumération d’encodeurs dans Windows 7 et versions ultérieures

pour les applications qui s’exécutent sur Windows 7, en plus de [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) , vous pouvez énumérer le MFTs d’encodeur en appelant [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex). Cette fonction retourne un pointeur vers l’objet d’activation de la table MFT de l’encodeur. La structure de la fonction est très similaire à **MFTEnum** décrite ci-dessus, à l’exception de **MFTEnumEx** retourne un tableau de pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pour le MFTS d’encodeur qui correspondent aux critères de recherche.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instanciation d’une table MFT d’encodeur](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Encodeurs multimédias](windows-media-encoders.md)
</dt> <dt>

[Objets d’activation](activation-objects.md)
</dt> </dl>

 

 



