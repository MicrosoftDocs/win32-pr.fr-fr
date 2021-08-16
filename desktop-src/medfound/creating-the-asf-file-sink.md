---
description: En savoir plus sur la création du récepteur de fichiers ASF, qu’une application peut utiliser pour archiver des données de média ASF dans un fichier.
ms.assetid: 991f3345-a6b4-45c2-a89d-3c13c70b6bbc
title: Création du récepteur de fichiers ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510ed3aeb3082277fa3a8bb4c814c1a82f92dd3da8815ffdbd70e4ef87d0d4f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743257"
---
# <a name="creating-the-asf-file-sink"></a>Création du récepteur de fichiers ASF

Le récepteur de fichiers ASF est une implémentation de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fournie par Media Foundation qu’une application peut utiliser pour archiver des données de média ASF dans un fichier. Pour plus d’informations sur le modèle objet et l’utilisation générale des récepteurs de média ASF, consultez [récepteurs de média ASF](asf-media-sinks.md).

Il existe deux façons de créer une instance du récepteur de fichiers ASF. Vous pouvez appeler [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) ou [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate).

Si vous appelez [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink), vous devez spécifier un flux d’octets, pour le fichier de sortie, dans lequel le récepteur écrira le contenu ASF pendant une session d’encodage. Le flux d’octets spécifié doit avoir des fonctionnalités pouvant être recherchées et accessibles en écriture, sinon l’appel **MFCreateASFMediaSink** échoue avec le \_ code d’erreur E Fail. Cet appel crée un objet récepteur de fichiers in-process et retourne un pointeur vers l’interface [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) du récepteur de fichiers.

Si vous appelez [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate), vous devez spécifier l’URL du fichier de sortie dans lequel le récepteur de fichiers écrira les données multimédias. Dans ce cas, le récepteur de fichiers crée en interne le flux d’octets. La fonction retourne un pointeur vers l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) du récepteur de fichiers. À

Pensez à [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) au lieu de [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink), lorsque votre topologie d’encodage est conçue comme suit :

-   La topologie d’encodage est pour le chemin d’accès du média protégé (PMP) et le récepteur de fichiers est utilisé hors processus.
-   Le nœud de sortie de la topologie est créé à l’aide du pointeur retourné vers l’objet Activate du récepteur de fichiers et votre application effectue le suivi des flux dans le récepteur de fichiers par numéros de flux.
    > [!Note]  
    > Vous pouvez activer le récepteur de fichiers en appelant [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). Toutefois, vous n’avez pas besoin d’activer l’objet de façon explicitement. La session multimédia effectue le suivi de l’objet d’activation et active le récepteur de fichiers automatiquement pendant la session d’encodage.

     

-   Les informations de flux de données sont configurées dans l’objet ContentInfo. Disucssed dans la sous-section suivante.

Une fois le récepteur de fichiers ASF créé, il doit être configuré avant de générer la topologie. Le récepteur de fichiers doit connaître les informations suivantes afin de générer le fichier de sortie.

-   Informations de base sur le flux
-   Informations sur le mode d’encodage
-   Métadonnées

Le récepteur de fichiers implémente l' [objet ASF ContentInfo](asf-contentinfo-object.md) et expose l’interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) afin qu’une application puisse l’utiliser pour définir les informations relatives aux flux et à l’encodage. Selon la fonction que vous avez appelée pour créer le récepteur de fichiers, il existe deux façons d’obtenir une référence à l’interface **IMFASFContentInfo** .

-   Si vous appelez la fonction [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) , l’application doit interroger l’interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) en appelant **IMFMediaSink :: QueryInterface** sur le récepteur de fichiers retourné.
-   Si vous choisissez d’appeler [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate), cette fonction s’attend à ce que vous disposiez d’un objet ContentInfo entièrement configuré avant l’appel. Pour ce faire, vous devez créer un objet ContentInfo vide en appelant [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , puis le configurer avec toutes les informations requises. Transmettez l’objet ContentInfo configuré à **MFCreateASFMediaSinkActivate** pour recevoir un pointeur vers l’objet récepteur Activate. Vous ne pouvez pas activer le récepteur de fichiers en utilisant l’objet d’activation retourné, puis modifier les informations de flux ou d’encodage.

Pour plus d’informations sur la configuration des flux de récepteurs et des propriétés spécifiques, consultez les rubriques suivantes :

-   [Ajout d’informations de flux au récepteur de fichiers ASF](adding-stream-information-to-the-asf-file-sink.md)
-   [Définition des propriétés dans le récepteur de fichiers](setting-properties-in-the-file-sink.md)
-   [Ajout de métadonnées au récepteur de fichiers](adding-metadata-to-the-file-sink.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Récepteurs de média ASF](asf-media-sinks.md)
</dt> <dt>

[Composants ASF de couche de pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Prise en charge ASF dans Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



