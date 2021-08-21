---
description: décrit comment ajouter des extensions d’unité de données lors de l’utilisation de Windows encodeurs multimédia.
ms.assetid: fdadcb85-c564-4d05-a4d7-af53a0107455
title: Utilisation des extensions d’unités de données (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4680626f06c93e63f293699360d98ac995eedc3b3351fe617c182dbc176165ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972718"
---
# <a name="using-data-unit-extensions-microsoft-media-foundation"></a>Utilisation des extensions d’unités de données (Microsoft Media Foundation)

les codecs vidéo et Windows Media Audio sont conçus pour fonctionner correctement avec le conteneur ASF (Advanced Systems Format). ASF est le format structuré utilisé pour les fichiers Windows Media Audio (WMA) et les fichiers Windows Media Video (WMV). Il s’agit d’un format extensible conçu pour la diffusion de données en continu. L’une des caractéristiques inhabituelles de la structure ASF est la possibilité d’associer des métadonnées à des exemples individuels et d’incorporer ces données avec les exemples dans le flux de bits. Un élément de métadonnées stocké de cette façon est appelé *extension d’unité* de données, ou *exemple d’extension*.

Une extension d’unité de données peut contenir des informations requises par l’encodeur, le décodeur ou l’application de lecteur. la plupart des types d’extension de données qui sont implémentés dans la série de codecs Windows Media 9 contiennent des données destinées à l’application qui décode et restitue le média. Par exemple, vous pouvez gérer les codes temporels SMPTE à partir des données sources en les ajoutant en tant qu’extensions d’unité de données. Toutefois, les fonctionnalités de codec suivantes requièrent des extensions d’unité de données :

-   [Insertion d’une image clé forcée](forcedkeyframeinsertion.md)
-   [Encodage vidéo entrelacé](interlacedvideoencoding.md)
-   La difficulté à utiliser les extensions d’unité de données lors de l’accès direct au codec est le mécanisme par lequel l’objet reçoit les données d’extension. pour ce faire, les objets du kit de développement logiciel (SDK) Windows Media Format utilisent des objets de mémoire tampon conçus pour prendre en charge cette fonctionnalité. il est recommandé d’utiliser le kit de développement logiciel (SDK) de Format multimédia Windows pour activer les fonctionnalités de codec qui requièrent des extensions d’unité de données, mais vous pouvez rendre ces fonctionnalités compatibles avec les objets de codec autonomes.

## <a name="passing-extended-samples-to-the-codec-objects"></a>Passage d’exemples étendus aux objets codec

le kit de développement logiciel (SDK) Windows Media Format utilise des objets buffer qui exposent des interfaces [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) . La dernière interface est [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4). Pour passer des exemples à un objet codec avec des extensions d’unité de données, vous devez utiliser un objet buffer qui implémente l’interface [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) ou [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) et l’interface **INSSBuffer** . vous pouvez utiliser des objets de mémoire tampon créés par le kit de développement logiciel (SDK) de Format multimédia Windows ou Microsoft Media Foundation pour ce faire, ou vous pouvez créer votre propre classe de mémoire tampon qui répond aux exigences. Pour créer votre propre classe de mémoire tampon, vous devez vous conformer aux prototypes de méthode pour les interfaces **INSSBuffer** . ces définitions d’interface se trouvent dans le fichier d’en-tête wmsbuffer. h qui est installé avec le kit de développement logiciel (SDK) de Format multimédia Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Codecs Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 
