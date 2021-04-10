---
title: Redirection
description: Redirection
ms.assetid: c8e3b43f-c11a-4ca7-b85c-038f0bfc3eb3
keywords:
- Sélections de métafichiers Windows Media, redirection
- listes de sélection, redirection
- sélections de métafichiers, redirection
- Lecteur Windows Media, redirection
- redirection
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf1bb4d690c8aa6808e009a45a7bff1d6efada72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309326"
---
# <a name="redirection"></a>Redirection

La sélection permet de rediriger le navigateur vers le lecteur Windows Media pour lire le fichier multimédia ou le flux de média désigné. La sélection de métafichier la plus basique contient uniquement l’Uniform Resource Locator (URL) d’un fichier multimédia.

Pour créer une sélection de métafichier de base, ouvrez votre éditeur de texte favori, tel que le bloc-notes Microsoft, puis tapez l’exemple de code suivant.


```XML
<ASX version="3.0">
   <ENTRY>
      <REF HREF="PathToYourFile"/>
   </ENTRY>
</ASX>

```



Remplacez un chemin d’accès valide à votre fichier Windows Media à l’aide de la syntaxe du tableau suivant.



| Source de contenu                                                                                 | Syntaxe                                    |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| Le contenu est un fichier sur un serveur Windows Media                                                       | mms://ServerName/Path/FileName.wma        |
| Le contenu est une multidiffusion de diffusion accessible à partir d’une station Windows Media.                    | https://WebServerName/Stations/kxyz.nsc    |
| Le contenu est une monodiffusion de diffusion accessible à partir d’un point de publication sur un serveur Windows Media. | mms://ServerName/PublishingPointAlias     |
| Le contenu est un fichier sur un serveur Web                                                                 | https://WebServerName/Path/Filename.wma    |
| Le contenu est un fichier sur un disque dur local                                                            | file://c : \\ chemin \\ nom_de_fichier. WMA             |
| Le contenu est un fichier sur un partage réseau                                                              | file:// \\ \\ nom_serveur \\ chemin \\ nom_de_fichier. WMA |
| Le contenu est un fichier sur un serveur Windows Media                                                       | mms://ServerName/Path/FileName.wmv        |



 

Enregistrez le fichier que vous avez créé avec un nom de fichier et une extension, comme décrit dans [extensions de noms de fichiers](file-name-extensions.md). Double-cliquez dessus dans l’Explorateur Windows. Le lecteur Windows Media doit ouvrir et démarrer la diffusion en continu du contenu. Vous pouvez enregistrer le fichier sur votre serveur Web, avec vos pages Web, et le lier à un élément **href** , ou l’incorporer dans une page Web à l’aide de la balise d' **objet** du lecteur Windows Media.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Sélections de métafichiers**](metafile-playlists.md)
</dt> <dt>

[**Utilisation des sélections de métafichiers**](using-metafile-playlists.md)
</dt> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guide des métafichiers Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




