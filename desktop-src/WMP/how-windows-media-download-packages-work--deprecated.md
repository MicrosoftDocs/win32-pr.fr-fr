---
title: Fonctionnement des packages de téléchargement Windows Media (déconseillé)
description: Fonctionnement des packages de téléchargement Windows Media (déconseillé)
ms.assetid: 8bab1764-93da-4abc-a8b7-17bc44b381ce
keywords:
- Fichiers Windows Media, packages de téléchargement Windows Media
- Windows Media Player, packages de téléchargement Windows Media
- sous-fichiers, packages de téléchargement Windows Media
- Windows Media, packages de téléchargement Windows Media
- Packages de téléchargement Windows Media, à propos de
- Packages de téléchargement Windows Media, mode de fonctionnement des packages
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1db477791bb93cd599dcef38a90b230c6cd7ddde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100680"
---
# <a name="how-windows-media-download-packages-work-deprecated"></a>Fonctionnement des packages de téléchargement Windows Media (déconseillé)

Cette page décrit une fonctionnalité qui peut ne pas être disponible dans les versions ultérieures du lecteur Windows Media et du kit de développement logiciel (SDK) du lecteur Windows Media.

Un package de téléchargement Windows Media est lancé à partir d’un site Web lorsqu’un utilisateur clique sur un lien dans un navigateur Web, tel que Microsoft Internet Explorer. Cette action ouvre le lecteur Windows Media, puis télécharge et décompresse le package de téléchargement Windows Media sur le disque dur de l’utilisateur dans un dossier par défaut.

Une fois que les fichiers ont été extraits du package de téléchargement Windows Media, le lecteur Windows Media localise une sélection de métafichiers Windows Media avec une extension de nom de fichier. asx parmi les fichiers empaquetés. S’il en trouve un, le lecteur crée une sélection basée sur le métafichier inclus. Les fichiers qui contiennent du contenu multimédia sont ensuite ajoutés à la bibliothèque.

Le lecteur Windows Media recherche également un élément d' **apparence** dans le métafichier. Si l’élément d' **apparence** contient une référence à un fichier de bordure avec l’extension de nom de fichier. WMZ, le joueur charge la bordure dans le volet de **lecture en cours** . Le lecteur commence ensuite à lire le contenu fourni dans le package.

Le diagramme suivant montre comment le contenu est empaqueté dans un fichier de téléchargement Windows Media, publié sur un site Web, téléchargé et lu sur un ordinateur client à l’aide du lecteur Windows Media.

![obtention et lecture d’un fichier de téléchargement Windows Media.](images/wmd-image.png) Téléchargement Windows Media

Le tableau suivant décrit les trois éléments qui composent un package de téléchargement Windows Media.



| Élément package    | Fonction                                                                                                                                                                                                                                        | Extensions de nom de fichier                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Bordure             | Interface utilisateur personnalisée et fixe créée par le propriétaire du contenu pour l’affichage, la liaison et la diffusion de tous les supports empaquetés dans le package de téléchargement Windows Media. Les techniques utilisées pour créer des bordures sont similaires à celles utilisées pour créer des apparences. | .wmz                                     |
| Sélection de métafichiers  | Métafichier Windows Media qui contient des éléments d' **entrée** , des informations de sélection et une identité d’élément d' **apparence** pour les fichiers de contenu.                                                                                                             | .asx                                     |
| Contenu multimédia | Fichier contenant un format audio ou vidéo pris en charge par le lecteur Windows Media.                                                                                                                                                          | . WMA,. wmv,. ASF,. wav,. avi,. mpg,. mp3 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Packages de téléchargement Windows Media (déconseillés)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




