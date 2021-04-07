---
title: Utilisation d’une sélection de métafichiers
description: Utilisation d’une sélection de métafichiers
ms.assetid: e6cbdb76-4405-409e-93c3-38a3baa7c231
keywords:
- Sélections de métafichiers Windows Media, utilisation
- sélections de métafichiers, utilisation
- sélections, utilisation
- Sélections de métafichiers Windows Media, à propos de
- sélections de métafichiers, à propos de
- sélections, à propos de
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a5f1832c0c739874fbbd4db219f2c622fc2debfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672766"
---
# <a name="using-a-metafile-playlist"></a>Utilisation d’une sélection de métafichiers

Étant donné que vous ne pouvez pas lier directement d’une page Web à un serveur multimédia de diffusion en continu, vous utilisez des sélections de métafichiers. Les sélections de métafichiers contiennent les informations requises par le lecteur Windows Media et sont stockées sur un serveur Web. Vous pouvez ensuite créer un lien à partir du document Web vers une sélection de métafichiers. Lorsqu’une sélection de métafichier est ouverte, le contrôle est transféré vers le lecteur Windows Media, qui traite le fichier, se connecte au serveur de diffusion multimédia en continu et lit le contenu spécifié.

Le navigateur télécharge d’abord la sélection de métafichiers dans le répertoire de cache de l’utilisateur. Étant donné que la sélection de métafichiers est petite, il s’agit d’une étape très rapide. L’ordinateur de l’utilisateur trouve ensuite dans son tableau associations de fichiers l’Association de la sélection de métafichiers avec le lecteur Windows Media. Le lecteur Windows Media ouvre et interprète les scripts dans la sélection de métafichiers, qui contient, entre autres choses, l’URL du contenu de diffusion en continu. Le lecteur Windows Media utilise l’URL pour localiser le contenu et initier le flux. Le script de sélection de métafichiers contrôle ensuite l’expérience de diffusion en continu.

Étant donné que les playlists de métafichiers fonctionnent par le biais d’une application auxiliaire associée au type ASXMIME (application/Mplayer2 ou Video/x-ms-asf), elles sont compatibles avec n’importe quel navigateur prenant en charge les applications auxiliaires. Les exemples présentés dans ce document fonctionnent avec Microsoft Internet Explorer 4,0 et versions ultérieures, et avec Netscape Navigator 4,0 et versions ultérieures sur les plateformes Microsoft Win32® et Apple Macintosh. Dans tous les exemples, vous devez vous assurer que tous les fichiers multimédias numériques référencés ont des chemins d’accès et des noms de fichiers valides pour votre environnement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide des métafichiers Windows Media**](windows-media-metafile-guide.md)
</dt> <dt>

[**Informations de référence sur les métafichiers Windows Media**](windows-media-metafile-reference.md)
</dt> <dt>

[**Présentation des fichiers Windows Media**](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




