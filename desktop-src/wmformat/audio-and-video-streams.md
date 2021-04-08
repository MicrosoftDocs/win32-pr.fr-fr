---
title: Flux audio et vidéo
description: Flux audio et vidéo
ms.assetid: 809e5bb6-2bc4-4022-9117-a2be5418d7d1
keywords:
- Windows Media Format SDK, flux audio
- ASF (Advanced Systems Format), flux audio
- ASF (format des systèmes avancés), flux audio
- Kit de développement logiciel (SDK) Windows Media format, flux vidéo
- ASF (Advanced Systems Format), flux vidéo
- ASF (format de systèmes avancés), flux vidéo
- Windows Media Format SDK, flux
- ASF (Advanced Systems Format), flux
- ASF (format de systèmes avancés), flux
- flux audio, à propos de
- flux vidéo, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d72eb46a6fb19129da2b9a841eab1710da47013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029141"
---
# <a name="audio-and-video-streams"></a>Flux audio et vidéo

Les types de flux les plus courants utilisés dans les fichiers créés à l’aide du kit de développement logiciel (SDK) Windows Media format sont des flux audio et vidéo. Les représentations numériques des données audio et vidéo sont complexes et occupent de grandes quantités de mémoire. Dans la plupart des cas, l’audio et la vidéo sont compressés avant d’être ajoutés à un fichier ASF. La compression s’effectue à l’aide d’un compresseur/décompresseur (codec).

Plusieurs codecs Windows Media sont inclus dans ce kit de développement logiciel (SDK) et offrent une excellente compression de qualité pour les médias numériques. Pour plus d’informations sur les codecs Windows Media, consultez [fonctionnalités du codec](codec-features.md). De nombreux autres codecs sont disponibles à partir de différentes sources. Vous pouvez utiliser les codecs de votre choix lors de la création de fichiers ASF, mais seuls les codecs Windows Media sont directement pris en charge par les objets de ce kit de développement logiciel (SDK). Pour utiliser d’autres codecs, vous devez compresser les exemples et les transmettre à l’objet writer en tant que données arbitraires.

La distinction la plus importante entre les flux audio et vidéo et les flux arbitraires est que les flux contenant des données audio ou vidéo Windows Media sont validés par les objets du kit de développement logiciel (SDK) du format Windows Media. Les flux de données arbitraires ne sont pas validés automatiquement et doivent être vérifiés pour vérifier l’intégrité de votre application.

Les propriétés d’un flux audio ou vidéo sont décrites dans le profil utilisé pour créer le fichier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Flux arbitraires**](arbitrary-streams.md)
</dt> <dt>

[**Fonctionnalités des fichiers ASF**](asf-file-features.md)
</dt> <dt>

[**Utilisation des profils**](working-with-profiles.md)
</dt> </dl>

 

 




