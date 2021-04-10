---
title: Une sélection de base
description: Une sélection de base
ms.assetid: fdd87959-861a-456e-b903-f5a27b4f6221
keywords:
- Sélections de métafichiers Windows Media, exemples de sélection
- sélections, exemples de sélection
- sélections de métafichiers, exemples de sélection
- Sélections de métafichiers Windows Media, exemples de sélections
- sélections, exemples de sélections
- sélections de métafichiers, exemples de sélections
- Sélections de métafichiers Windows Media, exemples de sélections
- sélections, exemples de sélections
- sélections de métafichiers, exemples de sélections
- Sélections de métafichiers Windows Media, exemple de code
- sélections, exemple de code
- sélections de métafichiers, exemple de code
- Sélections de métafichiers Windows Media, exemple de sélection de base
- sélections, exemple de sélection de base
- sélections de métafichiers, exemple de sélection de base
- Windows Media Player, exemples de sélection
- Lecteur Windows Media, exemples de sélections
- Lecteur Windows Media, exemples de sélections
- Lecteur Windows Media, exemple de sélection de base
- exemples de sélection
- exemples de sélections
- exemples de sélections
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93bdd9b8ace378c4bcb5b3d6fa98bf3a690e8b60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029711"
---
# <a name="a-basic-playlist"></a>Une sélection de base

L’exemple de sélection suivant montre un ensemble de base d’éléments de sélection. Lorsque vous écrivez votre propre code, vous devez remplacer toutes les URL et tous les noms de fichiers par des noms de fichiers valides accessibles à votre lecteur Windows Media.

**Exemple de code**


```XML
<ASX version = "3.0">
<TITLE>Basic Playlist Demo</TITLE>
    <ENTRY>
        <TITLE>An Entry in a basic playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <REF HREF = "mms://proseware.com/path/Yourfile.wma" />
    </ENTRY>
</ASX>

```



Le tableau suivant fournit des détails sur l’utilisation de chaque élément dans l’exemple de code.



| Lignes                                                                                            | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <ASX version = "3.0">                                                                     | L’élément [ASX](asx-element.md) identifie pour le client (lecteur Windows Media) qu’il s’agit d’une sélection de métafichiers Windows Media. L’attribut **version** spécifie le numéro de version des éléments du métafichier.                                                                                                                                                                                                                                                                                                                                           |
| <TITLE>Démonstration de la playlist de base</TITLE>                                                  | L’élément [title](title-element--metafile.md) identifie le titre de la sélection dans son ensemble. Le lecteur Windows Media affiche ces métadonnées en tant que titre d’affichage.                                                                                                                                                                                                                                                                                                                                                                                               |
| <ENTRY>                                                                                   | Commence l’élément [entry](entry-element.md) . Un élément d' **entrée** permet de définir un clip particulier dans une sélection                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <TITLE>Entrée dans une sélection de base</TITLE>                                         | Identifie le titre du clip de la sélection. Elle est différente de l’élément **title** précédent, car celle-ci est imbriquée dans un élément **entry** . Le lecteur Windows Media affiche ces métadonnées en tant que titre du clip.                                                                                                                                                                                                                                                                                                                                         |
| <AUTHOR>Microsoft Corporation</AUTHOR>                                              | L’élément [Author](author-element.md) identifie l’auteur du clip multimédia. Le lecteur Windows Media affiche ces métadonnées en tant qu' **auteur** de clip.                                                                                                                                                                                                                                                                                                                                                                                                         |

| <!-- This is a comment. Change the following path to point to your Windows media file --> | Commentaire. Les [Commentaires](comments.md) sont visibles uniquement lorsque le code est affiché et sont au même format que les commentaires **XML** .                                                                                                                                                                                                                                                                                                                                                                                                                                  | | <REF HREF = "mms://proseware.com/path/Yourfile.wma" />                                    | Pointeur réel vers le fichier multimédia. L’élément [ref](ref-element.md) identifie la ligne comme un pointeur vers du contenu multimédia, tandis que l’attribut **href** est l’URL du fichier multimédia. Dans ce cas, l’URL utilise le protocole MMS, de sorte qu’elle pointe vers un serveur Windows Media. Les fichiers multimédias sur votre serveur multimédia ne sont généralement pas conservés dans le même emplacement que vos documents HTML.<br/> Notez l’utilisation de la fermeture de l’élément, par exemple « /> », au lieu de « &lt; /Ref &gt; ». Étant donné que cet élément n’a pas d’éléments enfants, il se ferme lui-même.<br/> | | </ENTRY>                                                                                  | Spécifie la fin de l’élément d' **entrée** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | | </ASX>                                                                                    | Spécifie la fin de la sélection.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création de sélections de métafichiers**](creating-metafile-playlists.md)
</dt> <dt>

[**Exemples de sélections**](example-playlists.md)
</dt> <dt>

[**Sélections de métafichiers**](metafile-playlists.md)
</dt> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guide des métafichiers Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 





