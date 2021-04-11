---
title: Utilisation des commandes de script
description: Utilisation des commandes de script
ms.assetid: be8a2d22-35cb-4b8d-ad00-e8a45bb85b39
keywords:
- Windows Media Format SDK, commandes de script
- ASF (Advanced Systems Format), commandes de script
- ASF (format des systèmes avancés), commandes de script
- scripts, commandes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2e840a677e58a1be528e84e4ed1b4be7fe3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029293"
---
# <a name="using-script-commands"></a>Utilisation des commandes de script

Le kit de développement logiciel (SDK) Windows Media format prend en charge l’utilisation de commandes de script pour communiquer des actions d’application dans des fichiers ASF. Chaque commande de script est composée de deux chaînes, la première est le type de commande, la seconde est celle des données de commande. Par exemple, vous pouvez utiliser le type de script « URL » et transmettre une URL Internet valide en tant que données de commande. Lorsqu’une application de lecture qui prend en charge les commandes de script de type « URL » reçoit cette commande, elle ouvre l’adresse spécifiée dans une fenêtre de navigateur.

Le kit de développement logiciel (SDK) du format Windows Media offre deux options de diffusion de script dans des fichiers ASF. Vous pouvez créer un flux de script ou inclure des commandes de script dans l’en-tête du fichier. Les flux de script sont utiles car les commandes de script sont fournies dans l’ordre chronologique des présentations. Si vous utilisez des commandes de script dans l’en-tête de fichier, votre application doit récupérer toutes les commandes de script avant de commencer la lecture. Vous devez suivre les durées de présentation des commandes de script et y répondre au bon moment.

Les sections suivantes décrivent comment inclure des commandes de script dans un fichier ASF.



| Section                                                                                                                | Description                                                  |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Pour utiliser un flux de script](to-use-a-script-stream.md)                                                                   | Décrit comment inclure des commandes de script dans un flux de script. |
| [Pour ajouter des données de script à l’en-tête](to-add-script-data-to-the-header.md)                                               | Décrit comment inclure des commandes de script dans l’en-tête de fichier. |
| [Utilisation de commandes de script prises en charge par le lecteur Windows Media](using-script-commands-supported-by-windows-media-player.md) | Décrit les commandes de script utilisées par le lecteur Windows Media.  |



 

> [!Note]  
> Dans les versions précédentes du kit de développement logiciel (SDK) de format Windows Media, les flux de script étaient utilisés pour ouvrir des adresses Web correspondant au contenu d’un fichier ASF. Vous pouvez désormais utiliser des flux Web pour travailler avec des pages Web synchronisées. Pour plus d’informations, consultez consultez [flux Web](web-streams.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Commandes de script**](script-commands.md)
</dt> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 




