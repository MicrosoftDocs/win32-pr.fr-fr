---
description: les codecs Windows Media Audio et vidéo sont un ensemble d’objets que vous pouvez utiliser pour compresser et décompresser des données multimédias numériques.
ms.assetid: 74de2e75-b1ee-436d-8d78-efe366ab7aa6
title: Codecs Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 863bb21e17200016317ce273ecb8e2493b9d6bea7d19f92f3f397fb61b88eba4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972528"
---
# <a name="windows-media-codecs"></a>Codecs Windows Media

les codecs Windows Media Audio et vidéo sont un ensemble d’objets que vous pouvez utiliser pour compresser et décompresser des données multimédias numériques. Chaque codec se compose de deux objets : un encodeur et un décodeur. cette partie de la documentation explique comment utiliser les fonctionnalités des codecs vidéo et Windows Media Audio pour produire et consommer des flux de données compressés.

> [!Note]  
> cette documentation concerne principalement les développeurs qui souhaitent utiliser Windows codecs multimédias dans leurs applications multimédias basées sur C++. pour obtenir une vue d’ensemble technique des fonctionnalités des codecs multimédias Windows, consultez [à propos des codecs multimédias Windows](about-the-windows-media-codecs.md).

 

Le terme *codec* est un amalgame des termes compresseur et décompresseur. Un codec est généralement implémenté comme une paire d’objets COM : l’un pour l’encodage du contenu et l’autre pour le décodage du contenu. Dans certains cas, les objets COM occupent la même bibliothèque de liens dynamiques (DLL).

Chaque objet codec implémente deux interfaces distinctes mais similaires :



| Interface                              | Description                                 |
|----------------------------------------|---------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | Compatible avec Microsoft Media Foundation. |
| [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | Compatible avec DirectShow.                 |



 

En outre, il existe différents codecs pour l’audio et la vidéo, mais également différents codecs pour différents types de contenu que vous pouvez placer dans un fichier audio ou vidéo. Les algorithmes utilisés pour compresser et décompresser les données des mots prononcés diffèrent des algorithmes utilisés pour compresser et décompresser les données de musique.

## <a name="codec-descriptions"></a>Descriptions des codecs

le tableau suivant décrit les utilisations prévues des codecs multimédias Windows.



| Codec                                                                     | Description                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows Media Audio](windowsmediaaudioencoder.md)                       | un codec audio qui prend en charge trois catégories de contenu encodé : Standard, Professional et sans perte.                                                                                                                                                                                      |
| [Windows Voix Media audio](windowsmediaaudiovoiceencoder.md)            | Codec audio optimisé pour l’encodage de la voix humaine à des taux de compression élevés. Il s’agit du codec préféré pour les flux composés principalement de mots prononcés. Pour le contenu mixte musical et vocal, ce codec peut modifier dynamiquement l’algorithme d’encodage utilisé, pour obtenir une qualité optimale. |
| [Windows Media Video 9](windowsmediavideo9encoder.md)                    | Codec vidéo qui prend en charge quatre catégories de contenu encodé : profil simple, profil principal, profil avancé et image.                                                                                                                                                                  |
| [Windows Écran Media Video 9](usingthewindowsmediavideo9screencodec.md) | Codec vidéo optimisé pour l’encodage des captures d’écran séquentielles à partir des moniteurs d’ordinateur. Ce codec est souvent utilisé pour la formation ou le support logiciel en enregistrant les images du moniteur pendant l’utilisation des applications de l’ordinateur.                                                                         |



 

les versions les plus récentes des objets codec permettent également d’accéder à certains codecs hérités, y compris les Windows Media Video 7 et 8, Windows l’écran de support 7, les codecs mpeg-4 anciens et les codecs microsoft ISO mpeg-4.

> [!Note]  
> Cette documentation ne couvre pas ces codecs hérités. Il couvre uniquement les versions actuelles des codecs.

 

Pour les codecs plus anciens, utilisez les mêmes procédures que lors de l’utilisation des codecs actuels. Toutefois, n’oubliez pas que toutes les fonctionnalités ne sont pas prises en charge dans tous les codecs.

## <a name="in-this-section"></a>Dans cette section

-   [à propos des codecs multimédias Windows](about-the-windows-media-codecs.md)
-   [Utilisation des objets codec et DSP](decidinghowtousethewindowsmediaaudioandvideocodecs.md)
-   [Méthodes d’encodage](encodingmethods.md)
-   [Implémentation du codec](codecimplementation.md)
-   [Modèle de mémoire tampon de compartiment avec fuite](the-leaky-bucket-buffer-model.md)
-   [Utilisation du codec DMOs](workingwithcodecdmos.md)
-   [Utilisation du codec MFTs](workingwithcodecmfts.md)
-   [Utilisation de l’audio](workingwithaudio.md)
-   [Utilisation de la vidéo](workingwithvideo.md)
-   [Stockage d’un média compressé dans des fichiers AVI](storingcompressedmediainavifiles.md)
-   [Utilisation de l’encodage VBR](usingvbrencoding.md)
-   [Utilisation de l’encodage Two-Pass](usingtwoencodingpasses.md)
-   [Obtention des statistiques d’encodage](gettingencodingstatistics.md)
-   [Utilisation des extensions d’unité de données](usingdataunitextensions.md)
-   [Constantes codec et DSP IPropertyBag](codecanddspproperties.md)
-   [Analyseur de table des matières](toc-parser.md)
-   [Windows FAQ sur les codecs multimédias](frequentlyaskedquestions.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation Media Foundation](media-foundation-programming-guide.md)
</dt> <dt>

[Technologies multimédias pour Windows](/previous-versions/bg125389(v=msdn.10))
</dt> </dl>

 

 
