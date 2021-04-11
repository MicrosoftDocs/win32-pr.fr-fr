---
title: Redimensionnement vidéo
description: Redimensionnement vidéo
ms.assetid: 38ecb729-68eb-4452-8389-cabe987fb8b6
keywords:
- Windows Media Format SDK, redimensionnement vidéo
- Windows Media Format SDK, redimensionnement de la vidéo
- Format de systèmes avancés (ASF), redimensionnement vidéo
- ASF (format des systèmes avancés), redimensionnement vidéo
- Format de systèmes avancés (ASF), redimensionnement vidéo
- ASF (format des systèmes avancés), redimensionnement de la vidéo
- redimensionnement vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200496b1dead3abacfbfad7674519e0cf7ce4f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196552"
---
# <a name="video-resizing"></a>Redimensionnement vidéo

Lorsque vous définissez les paramètres d’un flux vidéo, vous devez spécifier une largeur et une hauteur pour les images vidéo. Cette taille vidéo détermine la taille des images vidéo encodées dans la section de données du fichier. Toutefois, la taille de la vidéo dans un profil ne détermine pas, ou limite, la taille du média d’entrée que vous fournissez au rédacteur, ou la taille du média de sortie que vous recevez du lecteur. L’enregistreur peut redimensionner les images vidéo en fonction des besoins de votre application.

La taille de l’image vidéo peut être considérée comme allant jusqu’à trois étapes : la taille de la vidéo d’entrée, la taille de la vidéo du flux et la taille de la vidéo de sortie.

La taille de la vidéo d’entrée correspond à la taille des frames que vous transmettez comme exemples à l’objet enregistreur. Vous définissez cette taille comme l’une des propriétés d’entrée vidéo requises. Pour plus d’informations sur les propriétés d’entrée, consultez [pour énumérer les formats d’entrée](to-enumerate-input-formats.md).

La taille vidéo de la diffusion en continu correspond à la taille des frames dans la section des données du fichier ASF. Vous définissez cette taille en tant qu’un des paramètres de configuration de flux requis dans le profil. Si vous écrivez un fichier et que la taille de la vidéo d’entrée est différente de la taille de la vidéo du flux, l’enregistreur redimensionne les frames pendant l’encodage. Pour plus d’informations sur les propriétés du flux vidéo, consultez [Configuration des flux vidéo](configuring-video-streams.md).

La taille de la vidéo de sortie est la taille des trames fournies par le lecteur ou le lecteur synchrone. Vous définissez cette taille comme l’une des propriétés de sortie vidéo requises. Si vous lisez un fichier et que la taille de la vidéo de sortie est différente de celle de la vidéo de diffusion en continu, le lecteur redimensionne les frames lors du décodage.

Vous ne pouvez pas définir une taille vidéo de flux sur un nombre impair de pixels de largeur. Si vous définissez la largeur d’un flux vidéo sur une valeur impaire, soit le profil n’est pas accepté par le writer, soit la vidéo obtenue est encodée avec une ligne noire d’un côté pour commettre la différence.

Vous devez veiller à redimensionner la vidéo. Les images ont tendance à être plus adaptées à leur résolution d’origine. Le redimensionnement des images peut souvent provoquer une distorsion et rendre le texte illisible. Si vous compressez la vidéo à une vitesse de transmission faible, vous constaterez également que les distorsions de redimensionnement peuvent entraîner des artefacts de compression graves.

Le codec d’écran Windows Media Video 9 ne prend pas en charge le redimensionnement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités d’écriture de fichier**](file-writing-features.md)
</dt> <dt>

[**Utilisation des entrées**](working-with-inputs.md)
</dt> <dt>

[**Utilisation des sorties**](working-with-outputs.md)
</dt> </dl>

 

 




