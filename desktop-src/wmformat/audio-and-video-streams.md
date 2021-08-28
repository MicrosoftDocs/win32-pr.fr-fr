---
title: Flux audio et vidéo
description: Flux audio et vidéo
ms.assetid: 809e5bb6-2bc4-4022-9117-a2be5418d7d1
keywords:
- Windows Media Format SDK, flux audio
- ASF (Advanced Systems Format), flux audio
- ASF (format des systèmes avancés), flux audio
- Windows Media Format SDK, flux vidéo
- ASF (Advanced Systems Format), flux vidéo
- ASF (format de systèmes avancés), flux vidéo
- Windows Media Format SDK, Streams
- ASF (Advanced Systems Format), flux
- ASF (format de systèmes avancés), flux
- flux audio, à propos de
- flux vidéo, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6bb1836540a8de3b0834d271c1aeb97ba2869fa5acfcd221d03071b32ec94e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705223"
---
# <a name="audio-and-video-streams"></a>Flux audio et vidéo

les types de flux les plus courants utilisés dans les fichiers créés à l’aide du kit de développement logiciel (SDK) Windows Media Format sont des flux audio et vidéo. Les représentations numériques des données audio et vidéo sont complexes et occupent de grandes quantités de mémoire. Dans la plupart des cas, l’audio et la vidéo sont compressés avant d’être ajoutés à un fichier ASF. La compression s’effectue à l’aide d’un compresseur/décompresseur (codec).

plusieurs codecs de média Windows sont inclus dans ce kit de développement logiciel (SDK) et offrent une excellente compression de qualité pour les médias numériques. pour plus d’informations sur les codecs multimédias Windows, consultez [fonctionnalités du codec](codec-features.md). De nombreux autres codecs sont disponibles à partir de différentes sources. vous pouvez utiliser les codecs de votre choix lors de la création de fichiers ASF, mais seuls les codecs multimédias Windows sont directement pris en charge par les objets de ce kit de développement logiciel (SDK). Pour utiliser d’autres codecs, vous devez compresser les exemples et les transmettre à l’objet writer en tant que données arbitraires.

la distinction la plus importante entre les flux audio et vidéo et les flux arbitraires est que les flux contenant Windows données audio ou vidéo de média sont validés par les objets du kit de développement logiciel (SDK) Windows media Format. Les flux de données arbitraires ne sont pas validés automatiquement et doivent être vérifiés pour vérifier l’intégrité de votre application.

Les propriétés d’un flux audio ou vidéo sont décrites dans le profil utilisé pour créer le fichier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Flux arbitraire**](arbitrary-streams.md)
</dt> <dt>

[**Fonctionnalités des fichiers ASF**](asf-file-features.md)
</dt> <dt>

[**Utilisation des profils**](working-with-profiles.md)
</dt> </dl>

 

 




