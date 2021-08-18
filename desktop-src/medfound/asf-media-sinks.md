---
description: Le récepteur multimédia ASF est le composant final dans le pipeline d’encodage qui permet à une application d’écrire un fichier ASF.
ms.assetid: 65bb8822-5eb0-46a3-ab9e-c55ae466e982
title: Récepteurs de média ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50af8530b1c2b8d9131243cafa67e841289cbbe0691cfcb499b57df68b60b141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118744210"
---
# <a name="asf-media-sinks"></a>Récepteurs de média ASF

Le récepteur multimédia ASF est le composant final dans le pipeline d’encodage qui permet à une application d’écrire un fichier ASF.

Media Foundation fournit deux types de récepteurs de média ASF :

-   Le *récepteur de fichiers ASF* est utilisé pour archiver des données de support ASF dans un fichier.
-   Le *récepteur de streaming ASF* est utilisé pour écrire du contenu ASF dans un flux d’octets pouvant être diffusé en continu sur le réseau.

Les récepteurs de média ASF contiennent un ou plusieurs récepteurs de flux, qui représentent les données à écrire pour chaque flux dans le fichier ASF de sortie. pour l’encodage des applications qui s’exécutent sur Windows Vista, vous devez configurer manuellement la topologie d’encodage en créant et en configurant le récepteur multimédia ASF, puis en l’ajoutant à la topologie. dans Windows 7, si vous utilisez les objets de transcodage rapide pour créer la topologie, vous n’avez pas à créer directement le récepteur multimédia et l’application n’appelle aucune méthode sur le récepteur multimédia ou sur l’un des récepteurs de flux. Les objets de transcodage rapide instancient les récepteurs multimédia requis et l’ajoutent à la topologie avant de retourner une référence à l’application appelant. Toutefois, pour les objets de transcodage rapides, certaines restrictions s’appliquent selon le type d’encodage.

-   [Modèle objet du récepteur multimédia ASF](#asf-media-sink-object-model)
-   [Récepteur de fichiers ASF](#asf-file-sink)
-   [Rubriques connexes](#related-topics)

## <a name="asf-media-sink-object-model"></a>Modèle objet du récepteur multimédia ASF

Les récepteurs de média ASF implémentent l’interface [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) et exposent les interfaces suivantes. Une application peut obtenir une référence à ces interfaces en appelant [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le récepteur multimédia ASF qu’elle utilise pour générer des exemples de sortie.



| Interface                                                  | Description                                                                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                       | Requis pour tous les récepteurs multimédias.                                                                                                                                                                          |
| [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) | Implémenté par le récepteur de fichiers ASF qui écrit le contenu multimédia généré dans un fichier. Vous pouvez utiliser les méthodes sur cette interface pour vider les données et mettre à jour l’objet d’en-tête ASF du fichier de sortie final. |
| [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)             | Reçoit des notifications de modification d’État à partir de l’horloge de présentation.                                                                                                                                       |
| [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)             | L’objet ASF ContentInfo est un objet de niveau WMContainer qui stocke principalement les informations d’objet d’en-tête ASF. Cette valeur est utilisée pour créer des récepteurs de média ASF.                                                     |
| [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                         | Utilisé pour décrire les métadonnées du fichier ASF.                                                                                                                                                        |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)         | Récupère une collection de métadonnées, soit pour une présentation complète, soit pour un flux de la présentation.                                                                                          |



 

## <a name="asf-file-sink"></a>Récepteur de fichiers ASF

Le récepteur de fichiers ASF est une implémentation de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fournie par Media Foundation qu’une application peut utiliser pour archiver des données de média ASF dans un fichier.

Vous devez créer, configurer et appeler des méthodes sur le récepteur de fichiers ou l’un de ses récepteurs de flux si vous utilisez les objets de couche de pipeline pour écrire un nouveau fichier ASF. Après avoir configuré le récepteur de fichiers, vous pouvez l’ajouter au pipeline d’encodage.

Voici les étapes générales à suivre pour utiliser le récepteur de fichiers ASF :

1.  Créez le récepteur de fichiers in-process ou out-of-process.
2.  Configurez le récepteur de fichiers avec tous les flux, les propriétés d’encodage et les informations de métadonnées.
3.  Associez le récepteur de fichiers au nœud de topologie de sortie en énumérant les récepteurs de flux ou en effectuant le suivi des numéros de flux avec dans le récepteur.

Les rubriques suivantes contiennent des informations détaillées sur l’utilisation du récepteur de fichiers ASF :

-   [Création du récepteur de fichiers ASF](creating-the-asf-file-sink.md)
-   [Ajout d’informations de flux au récepteur de fichiers ASF](adding-stream-information-to-the-asf-file-sink.md)
-   [Définition des propriétés dans le récepteur de fichiers](setting-properties-in-the-file-sink.md)
-   [Ajout de métadonnées au récepteur de fichiers](adding-metadata-to-the-file-sink.md)
-   [Modèle de mémoire tampon de compartiment avec fuite](the-leaky-bucket-buffer-model.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Composants ASF de couche de pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Prise en charge ASF dans Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
