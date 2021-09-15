---
description: Cette rubrique est une vue d’ensemble des API d’encodage de fichier fournies dans Microsoft Media Foundation.
ms.assetid: 69dbef63-e272-4ad2-8d04-ae9366f79b33
title: Vue d’ensemble de l’encodage dans Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81882bd6da43f4040614347b662d988844c7b7a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414052"
---
# <a name="overview-of-encoding-in-media-foundation"></a>Vue d’ensemble de l’encodage dans Media Foundation

Cette rubrique est une vue d’ensemble des API d’encodage de fichier fournies dans Microsoft Media Foundation.

## <a name="terminology"></a>Terminologie

L' *encodage* est un terme général qui couvre plusieurs processus distincts :

1.  Encodage d’un flux audio ou vidéo dans un format compressé. Par exemple, l’encodage d’un flux vidéo en vidéo H. 264.
2.  Multiplexage (« muxing ») un ou plusieurs flux en un seul flux d’octets. En règle générale, les flux entrants sont encodés en premier. Cette étape peut impliquer la transmission de paquets de flux encodés.
3.  Écriture d’un flux d’octets multiplexés dans un fichier, tel qu’un fichier MP4 ou ASF (Advanced Systems Format). Le flux Multiplexed peut également être envoyé sur le réseau.

Le diagramme suivant illustre ces trois processus :

![Diagramme montrant les processus d’encodage et de multiplexage](images/encoding03.png)

Les variantes de ce processus incluent le transcodage et la remuxing :

-   Le *transcodage* consiste à décoder un fichier existant, à ré-encoder les flux et à Remultiplexer les flux encodés. Le transcodage peut être effectué pour convertir un fichier d’un type d’encodage à un autre. par exemple, pour convertir la vidéo H. 264 en Windows Media Video (WMV). Elle peut également être effectuée pour modifier la vitesse de transmission encodée. taille de l’image vidéo ; la fréquence d’images ; ou d’autres paramètres de format.
-   Le *Remultiplexage* ou *remuxing* désigne le démultiplexage d’un fichier et le Remultiplexage des flux, sans étape de décodage/codage. Cela peut être fait pour modifier la façon dont les paquets audio/vidéo sont multiplexés, pour supprimer un flux ou pour combiner des flux de deux fichiers sources différents.
-   La conversion est un cas particulier de transcodage, où le débit *binaire est modifié* sans modifier le type de compression. Par exemple, vous pouvez convertir un fichier à taux binaire élevé en un débit inférieur. Un scénario classique dans lequel la transclassification peut être utilisée consiste à synchroniser le contenu multimédia d’un PC à un appareil mobile. Si le périphérique portable ne prend pas en charge une vitesse de transmission élevée, il est possible que le fichier soit au prorata avant d’être copié sur le périphérique portable.

Le diagramme de blocs suivant illustre le processus de transcodage.

![Diagramme montrant le processus de transcodage](images/encoding05.png)

Le diagramme de blocs suivant illustre le processus remuxing.

![Diagramme montrant le processus remuxing](images/encoding06.png)

Cette documentation utilise parfois le terme *encodage* pour inclure le transcodage et les remuxing. Lorsqu’il est important de faire la distinction entre ces deux éléments, la documentation indique la différence.

Voir aussi : [Media Foundation : concepts essentiels](media-foundation-programming--essential-concepts.md).

## <a name="media-foundation-encoding-architecture"></a>Architecture d’encodage Media Foundation

Au niveau de la couche la plus basse de l’architecture Media Foundation, les types de composant suivants sont utilisés pour l’encodage :

-   Pour le transcodage, les [sources de média](media-sources.md) sont utilisées pour démultiplexer le fichier source.
-   Pour le processus d’encodage, les [transformations Media Foundation](media-foundation-transforms.md) sont utilisées pour décoder et encoder les flux.
-   Pour le processus de multiplexage, les [récepteurs de médias](media-sinks.md) sont utilisés pour multiplexer les flux et écrire le flux multiplexé dans un fichier ou un réseau.

Le diagramme suivant montre le déroulement des données entre ces composants dans un scénario de transcodage :

![Diagramme montrant les composants utilisés dans le transcodage](images/encoding04.png)

La plupart des applications n’utilisent pas directement ces composants. Au lieu de cela, une application utilise des API de niveau supérieur qui gèrent ces composants de niveau inférieur. Media Foundation fournit deux API de niveau supérieur pour l’encodage :

<dl> <dt>

<span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Session multimédia](media-session.md)
</dt> <dd>

La session multimédia fournit un pipeline de bout en bout qui déplace les données de la source du média, via les codecs, et enfin vers le récepteur multimédia. L’application contrôle la session multimédia et reçoit des événements d’état de la session multimédia.

</dd> <dt>

<span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Lecteur source](source-reader.md) et [enregistreur récepteur](sink-writer.md)
</dt> <dd>

Le lecteur source encapsule la source du média et éventuellement les décodeurs. Il fournit à l’application des exemples encodés ou décodés. Le writer du récepteur encapsule le récepteur multimédia et éventuellement les encodeurs. L’application transmet des exemples au writer du récepteur.

</dd> </dl>

Le diagramme suivant illustre la session de média :

![Diagramme montrant comment la session multimédia effectue le transcodage](images/encoding01.png)

l' [api de transcodage](transcode-api.md) (zone ombrée bleue) est un ensemble d’api introduites dans Windows 7, ce qui facilite la configuration de la Session multimédia pour l’encodage.

Le diagramme suivant montre le lecteur source et le writer du récepteur :

![Diagramme montrant le transcodage avec le lecteur source et le writer du récepteur](images/encoding02.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Codage et création de fichier](encoding-and-file-authoring.md)
</dt> <dt>

[Programmation Media Foundation : concepts essentiels](media-foundation-programming--essential-concepts.md)
</dt> </dl>

 

 



