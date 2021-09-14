---
title: fonctionnement des Packages de téléchargement Windows Media (déconseillé)
description: fonctionnement des Packages de téléchargement Windows Media (déconseillé)
ms.assetid: 8bab1764-93da-4abc-a8b7-17bc44b381ce
keywords:
- Windows fichiers multimédias, Windows les packages de téléchargement de média
- Lecteur Windows Media, Windows les packages de téléchargement de médias
- sous-fichiers, packages de téléchargement de médias Windows
- Windows médias, Windows les packages de téléchargement de média
- Windows Packages de téléchargement de médias, à propos de
- Windows Packages de téléchargement de médias, fonctionnement des packages
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1db477791bb93cd599dcef38a90b230c6cd7ddde
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416229"
---
# <a name="how-windows-media-download-packages-work-deprecated"></a>fonctionnement des Packages de téléchargement Windows Media (déconseillé)

cette page documente une fonctionnalité qui peut ne pas être disponible dans les futures versions de Lecteur Windows Media et le kit de développement logiciel (SDK) Lecteur Windows Media.

un package de téléchargement Windows Media est lancé à partir d’un site web lorsqu’un utilisateur clique sur un lien dans un navigateur Web, tel que Microsoft Internet Explorer. cette action ouvre Lecteur Windows Media puis télécharge et décompresse le package de téléchargement du support Windows sur le disque dur de l’utilisateur dans un dossier par défaut.

une fois que les fichiers ont été extraits du package Windows media Download, Lecteur Windows Media localise une sélection de métafichier multimédia Windows avec une extension de nom de fichier. asx parmi les fichiers empaquetés. S’il en trouve un, le lecteur crée une sélection basée sur le métafichier inclus. Les fichiers qui contiennent du contenu multimédia sont ensuite ajoutés à la bibliothèque.

Lecteur Windows Media recherche également un élément d' **apparence** dans le métafichier. Si l’élément d' **apparence** contient une référence à un fichier de bordure avec l’extension de nom de fichier. WMZ, le joueur charge la bordure dans le volet de **lecture en cours** . Le lecteur commence ensuite à lire le contenu fourni dans le package.

le diagramme suivant montre comment le contenu est empaqueté dans un fichier de téléchargement de média Windows, publié sur un site web, téléchargé et lu sur un ordinateur client à l’aide de Lecteur Windows Media.

![obtention et lecture d’un fichier de téléchargement Windows Media.](images/wmd-image.png) Windows Téléchargement de médias

le tableau suivant décrit les trois éléments qui composent un package Windows Media Download.



| Élément package    | Fonction                                                                                                                                                                                                                                        | Extensions de nom de fichier                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Bordure             | interface utilisateur personnalisée et fixe créée par le propriétaire du contenu pour l’affichage, la liaison et la diffusion de tous les médias empaquetés dans le package de téléchargement Windows media. Les techniques utilisées pour créer des bordures sont similaires à celles utilisées pour créer des apparences. | .wmz                                     |
| Sélection de métafichiers  | métafichier Windows Media qui contient des éléments d' **entrée** , des informations de sélection et une identité d’élément d' **apparence** pour les fichiers de contenu.                                                                                                             | .asx                                     |
| Contenu multimédia | fichier contenant tout format audio ou vidéo pris en charge par Lecteur Windows Media.                                                                                                                                                          | . WMA,. wmv,. ASF,. wav, .avi, .mpg .mp3 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Windows Packages de téléchargement de médias (déconseillés)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




