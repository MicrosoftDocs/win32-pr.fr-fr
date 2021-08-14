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
ms.openlocfilehash: 88b77de3e892d4f7b479822442a2637849df3d4bcd56273deb952246fba14f28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118195785"
---
# <a name="using-script-commands"></a>Utilisation des commandes de script

le kit de développement logiciel (SDK) Windows Media Format prend en charge l’utilisation de commandes de script pour communiquer des actions d’application dans des fichiers ASF. Chaque commande de script est composée de deux chaînes, la première est le type de commande, la seconde est celle des données de commande. Par exemple, vous pouvez utiliser le type de script « URL » et transmettre une URL Internet valide en tant que données de commande. Lorsqu’une application de lecture qui prend en charge les commandes de script de type « URL » reçoit cette commande, elle ouvre l’adresse spécifiée dans une fenêtre de navigateur.

le kit de développement logiciel (SDK) Windows Media Format fournit deux options pour fournir un script dans des fichiers ASF. Vous pouvez créer un flux de script ou inclure des commandes de script dans l’en-tête du fichier. Les flux de script sont utiles car les commandes de script sont fournies dans l’ordre chronologique des présentations. Si vous utilisez des commandes de script dans l’en-tête de fichier, votre application doit récupérer toutes les commandes de script avant de commencer la lecture. Vous devez suivre les durées de présentation des commandes de script et y répondre au bon moment.

Les sections suivantes décrivent comment inclure des commandes de script dans un fichier ASF.



| Section                                                                                                                | Description                                                  |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Pour utiliser un flux de script](to-use-a-script-stream.md)                                                                   | Décrit comment inclure des commandes de script dans un flux de script. |
| [Pour ajouter des données de script à l’en-tête](to-add-script-data-to-the-header.md)                                               | Décrit comment inclure des commandes de script dans l’en-tête de fichier. |
| [utilisation des commandes de Script prises en charge par Lecteur Windows Media](using-script-commands-supported-by-windows-media-player.md) | décrit les commandes de script utilisées par Lecteur Windows Media.  |



 

> [!Note]  
> dans les versions précédentes du kit de développement logiciel (SDK) de Format de média Windows, les flux de script étaient utilisés pour ouvrir des adresses Web correspondant au contenu d’un fichier ASF. Vous pouvez désormais utiliser des flux Web pour travailler avec des pages Web synchronisées. Pour plus d’informations, consultez consultez [flux Web](web-streams.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Commandes de script**](script-commands.md)
</dt> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 




