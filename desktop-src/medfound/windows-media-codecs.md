---
description: Les codecs Windows Media Audio et vidéo sont un ensemble d’objets que vous pouvez utiliser pour compresser et décompresser des données multimédias numériques.
ms.assetid: 74de2e75-b1ee-436d-8d78-efe366ab7aa6
title: Codecs Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec98f98fbd0561b291dfc4cc18e4270bf363baf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106525805"
---
# <a name="windows-media-codecs"></a>Codecs Windows Media

Les codecs Windows Media Audio et vidéo sont un ensemble d’objets que vous pouvez utiliser pour compresser et décompresser des données multimédias numériques. Chaque codec se compose de deux objets : un encodeur et un décodeur. Cette partie de la documentation explique comment utiliser les fonctionnalités des codecs vidéo et Windows Media Audio pour produire et consommer des flux de données compressés.

> [!Note]  
> Cette documentation concerne principalement les développeurs qui souhaitent utiliser des codecs Windows Media dans leurs applications multimédias basées sur C++. Pour obtenir une vue d’ensemble technique des fonctionnalités des codecs Windows Media, consultez [à propos des codecs Windows Media](about-the-windows-media-codecs.md).

 

Le terme *codec* est un amalgame des termes compresseur et décompresseur. Un codec est généralement implémenté comme une paire d’objets COM : l’un pour l’encodage du contenu et l’autre pour le décodage du contenu. Dans certains cas, les objets COM occupent la même bibliothèque de liens dynamiques (DLL).

Chaque objet codec implémente deux interfaces distinctes mais similaires :



| Interface                              | Description                                 |
|----------------------------------------|---------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | Compatible avec Microsoft Media Foundation. |
| [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | Compatible avec DirectShow.                 |



 

En outre, il existe différents codecs pour l’audio et la vidéo, mais également différents codecs pour différents types de contenu que vous pouvez placer dans un fichier audio ou vidéo. Les algorithmes utilisés pour compresser et décompresser les données des mots prononcés diffèrent des algorithmes utilisés pour compresser et décompresser les données de musique.

## <a name="codec-descriptions"></a>Descriptions des codecs

Le tableau suivant décrit les utilisations prévues des codecs Windows Media.



| Codec                                                                     | Description                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows Media Audio](windowsmediaaudioencoder.md)                       | Un codec audio qui prend en charge trois catégories de contenu encodé : standard, Professional et Lossless.                                                                                                                                                                                      |
| [Windows Media Audio Voice](windowsmediaaudiovoiceencoder.md)            | Codec audio optimisé pour l’encodage de la voix humaine à des taux de compression élevés. Il s’agit du codec préféré pour les flux composés principalement de mots prononcés. Pour le contenu mixte musical et vocal, ce codec peut modifier dynamiquement l’algorithme d’encodage utilisé, pour obtenir une qualité optimale. |
| [Windows Media Video 9](windowsmediavideo9encoder.md)                    | Codec vidéo qui prend en charge quatre catégories de contenu encodé : profil simple, profil principal, profil avancé et image.                                                                                                                                                                  |
| [Écran Windows Media Video 9](usingthewindowsmediavideo9screencodec.md) | Codec vidéo optimisé pour l’encodage des captures d’écran séquentielles à partir des moniteurs d’ordinateur. Ce codec est souvent utilisé pour la formation ou le support logiciel en enregistrant les images du moniteur pendant l’utilisation des applications de l’ordinateur.                                                                         |



 

Les versions les plus récentes des objets codec permettent également d’accéder à certains codecs hérités, notamment les Windows Media Video 7 et 8, Windows Media Screen 7, les codecs Microsoft MPEG-4 plus anciens et les codecs Microsoft ISO MPEG-4.

> [!Note]  
> Cette documentation ne couvre pas ces codecs hérités. Il couvre uniquement les versions actuelles des codecs.

 

Pour les codecs plus anciens, utilisez les mêmes procédures que lors de l’utilisation des codecs actuels. Toutefois, n’oubliez pas que toutes les fonctionnalités ne sont pas prises en charge dans tous les codecs.

## <a name="in-this-section"></a>Dans cette section

-   [À propos des codecs Windows Media](about-the-windows-media-codecs.md)
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
-   [FAQ sur les codecs Windows Media](frequentlyaskedquestions.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation Media Foundation](media-foundation-programming-guide.md)
</dt> <dt>

[Technologies multimédias pour Windows](/previous-versions/bg125389(v=msdn.10))
</dt> </dl>

 

 
