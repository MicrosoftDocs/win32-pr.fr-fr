---
title: Utilisation de safiles pour basculer en continu
description: Utilisation de safiles pour basculer en continu
ms.assetid: e632f670-54c4-4b5b-8396-1d5368f90e6d
keywords:
- Windows Sélections de métafichiers multimédia, basculement de flux d’événements en direct
- sélections, basculement de flux d’événements en direct
- sélections de métafichiers, basculement de flux d’événements en direct
- Windows Sélections de métafichiers multimédia, basculement de flux d’événements
- sélections, basculement de flux d’événements
- sélections de métafichiers, basculement de flux d’événements
- Windows Sélections de métafichiers multimédia, insertion de publicités
- sélections, insertion de publicités
- sélections de métafichiers, insertion de publicités
- Lecteur Windows Media, basculement en temps réel des flux d’événements
- Lecteur Windows Media, basculement de flux d’événements
- Lecteur Windows Media, insertion de publicités
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311090"
---
# <a name="using-metafiles-for-seamless-stream-switching"></a>Utilisation de safiles pour basculer en continu

Vous pouvez faciliter le basculement continu de flux à l’aide de sélections de métafichiers. En général, lorsqu’une partie du contenu se termine, la mise en mémoire tampon se produit pour le clip ou le flux suivant avant son ouverture (s’il s’agit d’un contenu reçu à partir d’un serveur multimédia de diffusion en continu). Microsoft Services Windows Media vous permet d’éliminer ou de réduire au minimum ce temps de mise en mémoire tampon et de faire en sorte qu’une autre partie du contenu diffusé en continu commence à s’exécuter presque immédiatement. le mode de fonctionnement normal de Lecteur Windows Media consiste à ouvrir le flux multimédia suivant référencé par la sélection 20 secondes avant la fin du flux actuellement affiché. Cela fournit généralement une transition transparente entre les flux multimédias, en fonction d’autres facteurs tels que les temps d’accès au Web.

Utilisez l’élément **Event** dans une sélection conjointement avec les commandes OPENEVENT de l’encodeur pour faciliter le basculement transparent entre les flux ou les fichiers. L’envoi d’une commande OPENEVENT 20 secondes ou plus avant la commande EVENT peut réduire les retards dans le basculement de flux. Lecteur Windows Media est ensuite en mesure de précharger une partie du contenu de diffusion en continu à venir dans une mémoire tampon.

utilisez Windows Media encoder pour envoyer une commande de script dans le flux en utilisant le format suivant :


```XML
OPENEVENT eventname 

```



Le nom de l’événement doit être celui défini dans l’élément **événement** de la sélection. lorsque Lecteur Windows Media reçoit une commande de script OPENEVENT à partir de l’encodeur, il recherche l’élément d' **événement** dans la playlist et commence la mise en mémoire tampon du clip ou du flux défini dans l’élément **event** . Lecteur Windows Media contient ensuite ces informations jusqu’à l’événement réel du même nom. lorsque l’événement nommé est reçu, Lecteur Windows Media bascule vers ce contenu précédemment mis en mémoire tampon.

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

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guide du métafichier multimédia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




