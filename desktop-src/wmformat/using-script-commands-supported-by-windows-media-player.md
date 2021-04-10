---
title: Utilisation de commandes de script prises en charge par le lecteur Windows Media
description: Utilisation de commandes de script prises en charge par le lecteur Windows Media
ms.assetid: 7054ce49-c000-4978-891e-825a83bfda5c
keywords:
- Windows Media Format SDK, commandes de script
- Windows Media Format SDK, Windows Media Player
- ASF (Advanced Systems Format), commandes de script
- ASF (format des systèmes avancés), commandes de script
- ASF (Advanced Systems Format), Windows Media Player
- ASF (format avancé des systèmes), Windows Media Player
- scripts, commandes
- scripts, Windows Media Player
- Lecteur Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25302b5f5b6789be0d9e18b0a93e1e781a9dc06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029294"
---
# <a name="using-script-commands-supported-by-windows-media-player"></a>Utilisation de commandes de script prises en charge par le lecteur Windows Media

Le kit de développement logiciel (SDK) Windows Media format ne fournit pas de prise en charge native pour l’analyse et la réponse aux commandes de script. Vous devez inclure toute logique relative aux commandes de script dans votre application. Les types de script que vous utilisez doivent également être définis dans votre application.

Vous pouvez inclure du code pour gérer les mêmes commandes de script que celles prises en charge par le lecteur Windows Media. La gestion de la compatibilité avec le lecteur Windows Media rend vos fichiers plus universels que si vous incorporez des commandes de script personnalisées.

Le tableau suivant répertorie les types de scripts pris en charge par le lecteur Windows Media.



| Type de script | Description                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| URL         | Le lecteur envoie l’URL spécifiée au navigateur pour qu’il s’affiche à l’utilisateur. Si un contrôle de lecteur incorporé est utilisé, vous pouvez ajouter une référence de frame spécifique à l’URL à l’aide de la syntaxe &&*frameName* .                                                                             |
| EXTENSION    | URL vers un autre fichier multimédia à lire.                                                                                                                                                                                                                                                |
| CAPTION     | Chaîne de texte qui est affichée dans la zone légendes du lecteur Windows Media. Ce type prend en charge la mise en forme HTML standard. le texte peut donc être mis en forme comme vous le souhaitez. Le sous-titrage est un exemple d’utilisation.                                                                             |
| ÉVÉNEMENT       | Nom d’un événement qui doit se produire. Le type d’événement prend en charge la personnalisation pour vos propres utilisations. Le code de l’événement spécifié doit être défini dans le métafichier Windows Media pour le flux afin que le lecteur puisse exécuter l’événement spécifié. Un exemple d’utilisation est l’insertion d’une publicité. |
| OPENEVENT   | Ce script précède l’événement réel. Le OPENEVENT permet au joueur de mettre en mémoire tampon le contenu afin que lorsque l’événement se produise, le basculement entre les flux semble être transparent.                                                                                                       |
| TEXT        | Chaîne de texte qui est affichée dans la zone légendes du lecteur Windows Media. Peut être du texte brut, du texte SAMI ou du texte mis en forme HTML.                                                                                                                                                           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des commandes de script**](using-script-commands.md)
</dt> </dl>

 

 




