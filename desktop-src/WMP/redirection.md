---
title: Redirection
description: Redirection
ms.assetid: c8e3b43f-c11a-4ca7-b85c-038f0bfc3eb3
keywords:
- Windows Sélections de métafichiers de média, redirection
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013221"
---
# <a name="redirection"></a>Redirection

la sélection permet de rediriger le navigateur vers Lecteur Windows Media pour lire le fichier multimédia ou le flux de média désigné. La sélection de métafichier la plus basique contient uniquement l’Uniform Resource Locator (URL) d’un fichier multimédia.

pour créer une sélection de métafichier de base, ouvrez votre éditeur de texte favori, tel que Microsoft Bloc-notes, puis tapez l’exemple de code suivant.


```XML
<ASX version="3.0">
   <ENTRY>
      <REF HREF="PathToYourFile"/>
   </ENTRY>
</ASX>

```



substituez un chemin d’accès valide à votre fichier multimédia Windows à l’aide de la syntaxe du tableau suivant.



| Source de contenu                                                                                 | Syntaxe                                    |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| le contenu est un fichier sur un serveur multimédia Windows                                                       | mms://ServerName/Path/FileName.wma        |
| le contenu est une multidiffusion de diffusion accessible à partir d’une station de média Windows                    | https://WebServerName/Stations/kxyz.nsc    |
| le contenu est une monodiffusion de diffusion accessible à partir d’un point de publication sur un serveur multimédia Windows | mms://ServerName/PublishingPointAlias     |
| Le contenu est un fichier sur un serveur Web                                                                 | https://WebServerName/Path/Filename.wma    |
| Le contenu est un fichier sur un disque dur local                                                            | file://c : \\ chemin \\ nom_de_fichier. WMA             |
| Le contenu est un fichier sur un partage réseau                                                              | file:// \\ \\ nom_serveur \\ chemin \\ nom_de_fichier. WMA |
| le contenu est un fichier sur un serveur multimédia Windows                                                       | mms://ServerName/Path/FileName.wmv        |



 

Enregistrez le fichier que vous avez créé avec un nom de fichier et une extension, comme décrit dans [extensions de noms de fichiers](file-name-extensions.md). Double-cliquez dessus dans l’explorateur de Windows. Lecteur Windows Media doit ouvrir et démarrer la diffusion en continu du contenu. vous pouvez enregistrer le fichier sur votre serveur web, avec vos pages web, et le lier à un élément **HREF** , ou l’incorporer dans une page web à l’aide de la balise d' **objet** Lecteur Windows Media.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Sélections de métafichiers**](metafile-playlists.md)
</dt> <dt>

[**Utilisation des sélections de métafichiers**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guide du métafichier multimédia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




