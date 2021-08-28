---
title: utilisation des commandes de Script prises en charge par Lecteur Windows Media
description: utilisation des commandes de Script prises en charge par Lecteur Windows Media
ms.assetid: 7054ce49-c000-4978-891e-825a83bfda5c
keywords:
- Windows Media Format SDK, commandes de script
- Windows Media Format SDK, Lecteur Windows Media
- ASF (Advanced Systems Format), commandes de script
- ASF (format des systèmes avancés), commandes de script
- ASF (Advanced Systems Format), Lecteur Windows Media
- ASF (Format avancé des systèmes), Lecteur Windows Media
- scripts, commandes
- scripts, Lecteur Windows Media
- Lecteur Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58709af99cb4ebcb4eaba64fa6bb167b0ca80acb3fcb21b34efe4a55e2bacf12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110069"
---
# <a name="using-script-commands-supported-by-windows-media-player"></a>utilisation des commandes de Script prises en charge par Lecteur Windows Media

le kit de développement logiciel (SDK) Windows Media Format ne fournit pas de prise en charge native pour l’analyse et la réponse aux commandes de script. Vous devez inclure toute logique relative aux commandes de script dans votre application. Les types de script que vous utilisez doivent également être définis dans votre application.

vous pouvez inclure du code pour gérer les mêmes commandes de script que celles prises en charge par Lecteur Windows Media. la gestion de la compatibilité avec Lecteur Windows Media rend vos fichiers plus universels que si vous incorporez des commandes de script personnalisées.

le tableau suivant répertorie les types de scripts pris en charge par Lecteur Windows Media.



| Type de script | Description                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| URL         | Le lecteur envoie l’URL spécifiée au navigateur pour qu’il s’affiche à l’utilisateur. Si un contrôle de lecteur incorporé est utilisé, vous pouvez ajouter une référence de frame spécifique à l’URL à l’aide de la syntaxe &&*frameName* .                                                                             |
| EXTENSION    | URL vers un autre fichier multimédia à lire.                                                                                                                                                                                                                                                |
| CAPTION     | chaîne de texte qui est affichée dans la zone de légendes de Lecteur Windows Media. Ce type prend en charge la mise en forme HTML standard. le texte peut donc être mis en forme comme vous le souhaitez. Le sous-titrage est un exemple d’utilisation.                                                                             |
| ÉVÉNEMENT       | Nom d’un événement qui doit se produire. Le type d’événement prend en charge la personnalisation pour vos propres utilisations. le code de l’événement spécifié doit être défini dans le Windows métafichier multimédia du flux afin que le lecteur puisse exécuter l’événement spécifié. Un exemple d’utilisation est l’insertion d’une publicité. |
| OPENEVENT   | Ce script précède l’événement réel. Le OPENEVENT permet au joueur de mettre en mémoire tampon le contenu afin que lorsque l’événement se produise, le basculement entre les flux semble être transparent.                                                                                                       |
| TEXT        | chaîne de texte qui est affichée dans la zone de légendes de Lecteur Windows Media. Peut être du texte brut, du texte SAMI ou du texte mis en forme HTML.                                                                                                                                                           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des commandes de script**](using-script-commands.md)
</dt> </dl>

 

 




