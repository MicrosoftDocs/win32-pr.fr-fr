---
title: Utilisation de safiles pour basculer en continu
description: Utilisation de safiles pour basculer en continu
ms.assetid: e632f670-54c4-4b5b-8396-1d5368f90e6d
keywords:
- Sélections de métafichiers Windows Media, basculement de flux d’événements en direct
- sélections, basculement de flux d’événements en direct
- sélections de métafichiers, basculement de flux d’événements en direct
- Sélections de métafichiers Windows Media, basculement de flux d’événements
- sélections, basculement de flux d’événements
- sélections de métafichiers, basculement de flux d’événements
- Sélections de métafichiers Windows Media, insertion de publicités
- sélections, insertion de publicités
- sélections de métafichiers, insertion de publicités
- Windows Media Player, basculement de flux d’événements en direct
- Lecteur Windows Media, basculement de flux d’événements
- Windows Media Player, insertion de publicités
- basculement de flux d’événements en direct
- basculement de flux d’événements
- insertion de publicité
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29496c71c0c849480bae029f246bfd544667071e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512028"
---
# <a name="using-metafiles-for-seamless-stream-switching"></a>Utilisation de safiles pour basculer en continu

Vous pouvez faciliter le basculement continu de flux à l’aide de sélections de métafichiers. En général, lorsqu’une partie du contenu se termine, la mise en mémoire tampon se produit pour le clip ou le flux suivant avant son ouverture (s’il s’agit d’un contenu reçu à partir d’un serveur multimédia de diffusion en continu). Microsoft Windows Media Services vous permet d’éliminer ou de réduire au minimum le temps de mise en mémoire tampon et de faire en sorte qu’une autre partie du contenu diffusé en continu commence à s’exécuter presque immédiatement. Le mode de fonctionnement normal pour le lecteur Windows Media est d’ouvrir le flux multimédia suivant référencé par la sélection 20 secondes avant la fin du flux actuellement affiché. Cela fournit généralement une transition transparente entre les flux multimédias, en fonction d’autres facteurs tels que les temps d’accès au Web.

Utilisez l’élément **Event** dans une sélection conjointement avec les commandes OPENEVENT de l’encodeur pour faciliter le basculement transparent entre les flux ou les fichiers. L’envoi d’une commande OPENEVENT 20 secondes ou plus avant la commande EVENT peut réduire les retards dans le basculement de flux. Le lecteur Windows Media est ensuite en mesure de précharger une partie du contenu de diffusion en continu à venir dans une mémoire tampon.

Utilisez l’encodeur Windows Media pour envoyer une commande de script dans le flux en utilisant le format suivant :


```XML
OPENEVENT eventname 

```



Le nom de l’événement doit être celui défini dans l’élément **événement** de la sélection. Lorsque le lecteur Windows Media reçoit une commande de script OPENEVENT à partir de l’encodeur, il recherche l’élément d' **événement** dans la sélection et commence la mise en mémoire tampon du clip ou du flux défini dans l’élément **Event** . Le lecteur Windows Media contient ensuite ces informations jusqu’à l’événement réel du même nom. Lorsque l’événement nommé est reçu, le lecteur Windows Media bascule vers ce contenu précédemment mis en mémoire tampon.

> [!Note]  
> Vous ne pouvez pas utiliser de caractères Unicode pour la commande de script OPENEVENT dans le fichier multimédia ou l’élément d' **événement** dans la sélection.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création de sélections de métafichiers**](creating-metafile-playlists.md)
</dt> <dt>

[**Sélections de métafichiers**](metafile-playlists.md)
</dt> <dt>

[**Événement Player. commande**](player-player-scriptcommand.md)
</dt> <dt>

[**Utilisation des sélections de métafichiers**](using-metafile-playlists.md)
</dt> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guide des métafichiers Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




