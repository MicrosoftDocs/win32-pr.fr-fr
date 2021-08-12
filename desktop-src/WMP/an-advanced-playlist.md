---
title: Une sélection avancée
description: Une sélection avancée
ms.assetid: 3f27562f-bc3b-4b7f-a83b-78317d3ad612
keywords:
- Windows Sélections de métafichiers multimédias, exemples de sélection
- sélections, exemples de sélection
- sélections de métafichiers, exemples de sélection
- Windows Sélections de métafichiers multimédia, exemples de sélections
- sélections, exemples de sélections
- sélections de métafichiers, exemples de sélections
- Windows Sélections de métafichiers multimédias, exemples de sélections
- sélections, exemples de sélections
- sélections de métafichiers, exemples de sélections
- Windows Sélections de métafichiers multimédia, exemple de code
- sélections, exemple de code
- sélections de métafichiers, exemple de code
- Windows Sélections de métafichiers multimédias, exemple de sélection avancée
- sélections, exemple de sélection avancée
- sélections de métafichiers, exemple de sélection avancée
- Lecteur Windows Media, exemples de sélection
- Lecteur Windows Media, exemples de sélections
- Lecteur Windows Media, exemples de sélections
- Lecteur Windows Media, exemple de sélection avancée
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
ms.openlocfilehash: 6573d5bef05c8af943368a12d03677526a9783915d6915b6cc5f1516bc9942f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583256"
---
# <a name="an-advanced-playlist"></a>Une sélection avancée

L’exemple de sélection suivant montre comment utiliser un ensemble plus complet d’éléments de sélection. lorsque vous écrivez votre propre code, vous devez remplacer toutes les url et tous les noms de fichiers par des noms de fichiers valides accessibles à votre Lecteur Windows Media.

Exemple de code


``` XML
<ASX version = "3.0">
    <TITLE>Advanced Playlist Demo</TITLE>
    <ABSTRACT>More Information at this website</ABSTRACT>
    <MOREINFO HREF="https://www.microsoft.com/windows/windowsmedia" />
    <BANNER HREF = "..\samples\home.gif">
        <ABSTRACT>MSN website</ABSTRACT>
        <MOREINFO HREF = "https://www.msn.com" />
    </BANNER>
    <PARAM name="track" value="1"/>
    <ENTRY ClientSkip="no">
        <BANNER HREF = "..\sample\contact.gif">
            <ABSTRACT>Visit Our website</ABSTRACT>
            <MOREINFO HREF = "https://www.msn.com" />
        </BANNER>
        <MOREINFO HREF = "https://www.msn.com" />
        <!-- This is the ToolTip text for Title/Author/Copyright text -->
        <ABSTRACT>Visit the YourImage website</ABSTRACT>
        <TITLE>The first entry in an advanced playlist</TITLE>
        <AUTHOR>YourImage</AUTHOR>
        <COPYRIGHT>(c)2000 YourImage</COPYRIGHT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
         <REF HREF = "..\media\laure.wma" />
    </ENTRY>

    <ENTRY>
        <TITLE>The second entry in the advanced playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <!-- This is the ToolTip text for Title text -->
        <ABSTRACT>This is where you can include your tool tips</ABSTRACT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
        <REF HREF = "..\media\mellow.wma" />
    </ENTRY>
</ASX>

```



Le tableau suivant décrit la sélection avancée précédente.



| Ligne                                                                                            | Description                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<ASX version = "3.0">`                                                                     | l’élément [ASX](asx-element.md) identifie pour le client (Lecteur Windows Media) qu’il s’agit d’une sélection de métafichier Windows Media. L’attribut **version** spécifie le numéro de version des éléments du métafichier.                                                                                                                    |
| `<TITLE>Advanced Playlist Demo</TITLE>`                                               | L’élément [title](title-element--metafile.md) identifie le titre de la sélection dans son ensemble. Lecteur Windows Media affiche ces métadonnées en tant que titre d’affichage.                                                                                                                                                                        |
| `<ABSTRACT>More Information at this Web Site< /ABSTRACT>`                             | L’élément [abstract](abstract-element.md) fournit l’info-bulle pour le titre de l’affichage.                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF ="https://www.microsoft.com/windows/windowsmedia" />`                        | L’élément [moreinfo](moreinfo-element.md) lie le titre d’affichage à une URL. La suspension du pointeur de la souris sur le titre du diaporama accède à l’info-bulle, si elle est définie. Sélectionnez l’option Afficher le titre pour ouvrir l’URL désignée.                                                                                                                |
| `<BANNER HREF = "..\\samples\\home.gif">`                                                   | l’élément [banner](banner-element.md) crée une bannière publicitaire dans Lecteur Windows Media. L’attribut **href** spécifie le graphique de bannière (qui doit être de 194 pixels de largeur par 32 pixels de haut).                                                                                                                                  |
| `<ABSTRACT>MSN website</ABSTRACT>`                                                    | L’élément [abstract](abstract-element.md) fournit l’info-bulle de la **bannière**.                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF = "https://www.msn.com" </ABSTRACT>`                                      | L’élément [moreinfo](moreinfo-element.md) lie le graphique de **bannière** à une URL. Le maintien du pointeur de la souris sur la **bannière** accède à une info-bulle, si elle est définie. La sélection de la **bannière** permet d’ouvrir l’URL désignée.                                                                                                                |
| <PARAM name = "track" value="1"/>                                                         | L’élément [param](param-element.md) définit un paramètre personnalisé. L’attribut **Name** définit le nom du paramètre personnalisé comme « Track ». L’attribut **value** définit la valeur de « Track » sur « 1 ».                                                                                                                          |
| `</BANNER>`                                                                                 | Ferme l’élément de **bannière**                                                                                                                                                                                                                                                                                                           |
| `<ENTRY ClientSkip="no">`                                                                   | Commence le bloc d’élément d' [entrée](entry-element.md) . Cet élément définit un élément dans une playlist en spécifiant un lien dans l’élément **ref** . La définition de **ClientSkip** sur « no » signifie que l’utilisateur ne peut pas avancer rapidement ou passer au clip suivant                                                                                             |
| `<BANNER HREF = "..\\samples\\contact.gif">`                                                | Crée une bannière de publicité. Le **href** est le graphique de bannière (194x32 pixels).                                                                                                                                                                                                                                                      |
| `<ABSTRACT>Visit Our website< /ABSTRACT>`                                             | Fournit l’info-bulle de la bannière.                                                                                                                                                                                                                                                                                                    |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | Fournit un lien vers l’URL de la bannière. La sélection de la bannière permet de se connecter à l’URL.                                                                                                                                                                                                                                                    |
| `</BANNER>`                                                                                 | Ferme l’élément de **bannière**                                                                                                                                                                                                                                                                                                           |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | Fournit un lien vers l’URL du texte du **titre** du clip.                                                                                                                                                                                                                                                                                 |
| `<!--This is the ToolTip text for the Title text -->`                                       | Commentaire. Les [Commentaires](comments.md) ne sont visibles que lorsque le code est affiché.                                                                                                                                                                                                                                                        |
| `<Abstract>Visit the YourImage website</abstract>`                                    | Fournit l’info-bulle pour le texte du **titre** du clip.                                                                                                                                                                                                                                                                                       |
| `<TITLE>The first entry in an advanced playlist</TITLE>`                              | Identifie le titre du clip. Il s’agit du **titre** du clip, car il est imbriqué dans un élément d' **entrée** . Lecteur Windows Media affiche ces métadonnées en tant que titre de clip.                                                                                                                                                             |
| `<AUTHOR>YourImage</AUTHOR>`                                                          | Identifie l’auteur du clip multimédia. ces métadonnées s’affichent en tant qu' **auteur** de clip par Lecteur Windows Media.                                                                                                                                                                                                                     |
| `<COPYRIGHT>(c)2000 YourImage</COPYRIGHT>`                                            | L’élément [Copyright](copyright-element.md) spécifie les droits d’auteur associés au clip multimédia. Lecteur Windows Media affiche ces métadonnées sous forme de COPYRIGHT du clip.                                                                                                                                                              |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | Commentaire, dans le même format que les commentaires **XML** .                                                                                                                                                                                                                                                                                      |
| `<REF HREF = "..\\media\\laure.wma" />`                                                     | URL du contenu multimédia. L’élément [ref](ref-element.md) identifie la ligne comme un pointeur vers du contenu multimédia. L’attribut **href** est l’URL du fichier. Notez l’utilisation de la fermeture de l’élément de type XML, « /> » au lieu de « &lt; /Ref &gt; ». Étant donné que cet élément n’a pas d’éléments enfants, il se ferme lui-même.<br/> |
| `</ENTRY>`                                                                                  | Spécifie la fin du du premier élément d' **entrée** .                                                                                                                                                                                                                                                                                |
| `<ENTRY>`                                                                                   | Commence le deuxième élément d' **entrée** .                                                                                                                                                                                                                                                                                                    |
| `<TITLE>The second Entry in the advanced playlist</TITLE>`                            | Identifie le titre du deuxième clip.                                                                                                                                                                                                                                                                                                |
| `<AUTHOR>Microsoft Corporation</AUTHOR>`                                              | Identifie l’auteur du deuxième clip multimédia.                                                                                                                                                                                                                                                                                         |
| `<!--This is the ToolTip text for the Title/Author/Copyright text -->`                      | Commentaire. Elle est visible uniquement lorsque le code est affiché.                                                                                                                                                                                                                                                                             |
| `<ABSTRACT>This is where you can include your tool tips</ABSTRACT>`                   | Il s’agit du texte d’info-bulle pour le texte du **titre** du clip.                                                                                                                                                                                                                                                                            |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | Commentaire. Elle est visible uniquement lorsque le code est affiché.                                                                                                                                                                                                                                                                             |
| `<REF HREF = ..\\media\\mellow.wma" />`                                                     | Identifie la ligne comme pointeur vers du contenu multimédia. L’attribut **href** est l’URL du fichier.                                                                                                                                                                                                                                       |
| `</ENTRY>`                                                                                  | Spécifie la fin du deuxième élément d' **entrée** .                                                                                                                                                                                                                                                                                      |
| `</ASX>`                                                                                    | Spécifie la fin de la sélection.                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création de sélections de métafichiers**](creating-metafile-playlists.md)
</dt> <dt>

[**Exemples de sélections**](example-playlists.md)
</dt> <dt>

[**Sélections de métafichiers**](metafile-playlists.md)
</dt> <dt>

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guide du métafichier multimédia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 





