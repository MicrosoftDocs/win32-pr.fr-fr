---
description: Dans le modèle de pipeline Media Foundations, une source de média est connectée à une transformation qui est encore connectée à un récepteur multimédia.
ms.assetid: 55ab3a53-d9fd-438c-998c-8888f99958ce
title: Composants ASF de couche de pipeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3b6eb2d00404d193e50cebf174210a1c25655e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531097"
---
# <a name="pipeline-layer-asf-components"></a>Composants ASF de couche de pipeline

Dans le modèle de pipeline d’Media Foundation, une source de média est connectée à une transformation qui est encore connectée à un récepteur multimédia. Les données contenues dans la source circulent dans la transformation et génèrent des échantillons de média de sortie dans le récepteur à des fins de lecture ou d’encodage. Selon que l’application souhaite lire du contenu ASF ou Encoder dans un fichier ASF, l’application doit générer le pipeline différemment.

Les rubriques suivantes contiennent des informations sur les composants de la couche de pipeline.

-   [Source de média ASF](asf-media-source.md)
-   [Windows Encodeurs multimédias](windows-media-encoders.md)
-   [Récepteurs de média ASF](asf-media-sinks.md)

Les trois principaux composants d’un pipeline ASF pour la lecture sont les suivants :

-   La source du média ASF est fournie par Media Foundation qui représente un fichier ASF.
-   Rééchantillonneurs audio, redimensionnements d’images vidéo, etc., (transformation)
-   Convertisseur audio et vidéo (récepteurs)

Pour plus d’informations sur la création d’un pipeline de lecture, consultez [création de topologies de lecture](creating-playback-topologies.md).

Les trois principaux composants d’un pipeline ASF pour l’encodage sont les suivants :

-   Source de média représentant les données dans un format qui doit être converti. Ce composant peut être l’une des sources de média par défaut fournies par Media Foundation ou une source personnalisée qui expose l’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .
-   Windows Encodeurs multimédia (transformation) qui effectuent la conversion de format.
-   Récepteurs de média ASF fournis par Media Foundation qui écrivent des objets ASF et des exemples de média dans un fichier de sortie spécifié par l’application.

Le pipeline est représenté dans une topologie et chaque objet dans le pipeline est représenté par un nœud de topologie. Pour la lecture et l’encodage, toutes les opérations de pipeline sont gérées par la session multimédia. L’une des responsabilités de la session multimédia est de s’assurer que le pipeline dispose de tous les composants requis pour générer la sortie. Par exemple, dans un pipeline d’encodage, si le format de la source audio est différent du format cible, la session multimédia insère des composants de transformation supplémentaires, tels que le rééchantillonneur qui effectue des conversions de taux d’échantillonnage appropriées. Le contrôle de workflow via le pipeline est également géré par la session multimédia. Dans un scénario de lecture, démarrant la session multimédia, la session multimédia envoie des exemples à SAR et EVR, qui les affiche sur le périphérique de sortie. Pour l’encodage, le démarrage de la session multimédia commence le processus d’encodage. La session avertit de façon asynchrone l’application lorsque l’encodage est terminé.

La rubrique suivante contient des instructions pas à pas sur l’utilisation des composants de couche de pipeline pour créer une topologie d’encodage. composants pour la lecture et l’écriture de fichiers ASF.

-   [didacticiel : encodage de média de Windows Pass](tutorial--1-pass-windows-media-encoding.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge ASF dans Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



