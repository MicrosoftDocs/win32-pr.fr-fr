---
description: Utilisation de sources multimédias avec la session multimédia
ms.assetid: b50d3d6e-728b-4ba5-9b79-413d2108ade1
title: Utilisation de sources multimédias avec la session multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ffec1b854829b5b8a0317d10adf121463e539dde471bc5b3063b1479037ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117688723"
---
# <a name="using-media-sources-with-the-media-session"></a>Utilisation de sources multimédias avec la session multimédia

Si vous utilisez la session multimédia pour contrôler la lecture, l’ensemble de méthodes que vous devez appeler sur une source de média est limité. Cette section décrit comment utiliser la source de média conjointement avec la session multimédia.

Voici les étapes de base que votre application doit effectuer :

1.  Créez la source du média. Pour créer une source de média, utilisez le programme de résolution source. Pour plus d’informations, consultez la page programme de [résolution source](source-resolver.md). Le programme de résolution source retourne un pointeur vers l’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) de la source. (Si vous avez écrit une source de média personnalisée, vous pouvez fournir une méthode de création personnalisée à la place.)

2.  Configurez la présentation. Pour configurer la présentation de la source, appelez [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). Vous pouvez modifier cette copie, mais les modifications ne sont pas actives tant que la lecture n’a pas commencé. Ne modifiez pas le descripteur de présentation pendant la lecture. Pour plus d’informations, consultez [descripteurs de présentation](presentation-descriptors.md).

3.  Créez une topologie qui contient la source du média. Pour plus d’informations, consultez [topologies](topologies.md).

4.  Utilisez la session multimédia pour contrôler la lecture. La session multimédia appelle des méthodes sur la source du média. Pour l’instant, l’application ne doit pas appeler de méthode sur la source du média.

5.  Avant de libérer la source du média, appelez [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) pour arrêter la source.

    > [!Note]  
    > Si vous utilisez la source de Sequencer, la source de Sequencer gère l’arrêt des sources de segment. Pour plus d’informations, consultez [Sequencer source](sequencer-source.md).

     

Si vous utilisez la session multimédia, les seules méthodes que vous devez appeler sur la source du média sont [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor), [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics)et [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown). En particulier :

-   N’appelez pas [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), [**Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause)ou [**Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop); ces méthodes doivent être appelées uniquement par la session multimédia.

-   N’appelez aucune méthode [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) .

-   Ne récupérez pas d’événements directement à partir de la source du média ou de l’un des flux. La session multimédia doit recevoir ces événements pour que le pipeline fonctionne correctement. La session multimédia transfère tous les événements qui sont requis par l’application.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Session multimédia](media-session.md)
</dt> </dl>

 

 



