---
title: Utilisation d’annonces
description: Utilisation d’annonces
ms.assetid: c372a4f8-2355-4c69-bba2-72b224879c4d
keywords:
- Sélections de métafichiers Windows Media, annonces
- sélections, annonces
- sélections de métafichiers, annonces
- Windows Media Player, annonces
- annonces
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c16fafee1984d08992b96c39d7c3893ea54f682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512242"
---
# <a name="using-announcements"></a>Utilisation d’annonces

Une annonce est un fichier qui contient des informations sur l’URL d’un flux multimédia, y compris l’adresse IP de multidiffusion, le port, le format de flux et d’autres paramètres de station. Les annonces sont créées par l’administrateur Windows Media lors de la création d’un flux de publication de monodiffusion ou de multidiffusion. Le client peut charger rapidement le fichier d’annonce, puis continuer à accéder au fichier multimédia de diffusion en continu.

Pour un point de publication monodiffusion, le flux de média du point de publication est ouvert. Pour un point de publication de multidiffusion, l’URL est extraite d’un fichier de station de diffusion avec une extension. NSC et le média de streaming est accessible. Contrairement à un flux de données en monodiffusion, aucune information d’en-tête n’est contenue dans un flux de multidiffusion. Ces informations proviennent du fichier de station de diffusion avec une extension. NSC. Le lecteur Windows Media ouvre généralement d’abord un fichier d’annonce, qui est une utilisation pour les sélections de métafichiers, qui pointe vers l’emplacement du fichier de station de diffusion.

Exemple de code


```XML
<ASX VERSION="3.0">
    <TITLE>title</TITLE>
    <ENTRY>
        <REF HREF="mms://proseware.com/pubpoint"/>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création de sélections de métafichiers**](creating-metafile-playlists.md)
</dt> <dt>

[**Utilisation des sélections de métafichiers**](using-metafile-playlists.md)
</dt> </dl>

 

 




