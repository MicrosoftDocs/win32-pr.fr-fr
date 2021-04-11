---
title: Création de sélections de métafichiers
description: Création de sélections de métafichiers
ms.assetid: 0afe3aaa-bcd1-4060-8772-add50f3b6bac
keywords:
- Sélections de métafichiers Windows Media, création
- sélections, création
- sélections de métafichiers, création
- création de sélections de métafichiers Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d4acff6452640c3f0b66219b765a931033b9f3a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197126"
---
# <a name="creating-metafile-playlists"></a>Création de sélections de métafichiers

Vous pouvez créer une sélection à l’aide de n’importe quel éditeur de texte, tel que le bloc-notes Microsoft. Ouvrez votre éditeur de texte. Tapez les entrées de script que vous souhaitez implémenter. Une fois que vous avez fini de taper dans le bloc-notes, enregistrez le fichier avec un nom de fichier et une extension de nom de fichier appropriés. Pour plus d’informations sur les extensions, consultez [instructions relatives](metafile-extension-guidelines.md)aux extensions de métafichiers. En général, le nom de fichier est le nom du fichier ou du flux Windows Media suivi d’une extension. Wax,. wvx ou. asx. Par exemple, si votre contenu multimédia est un fichier audio Windows Media qui a une extension. WMA, utilisez l’extension. Wax lors de l’attribution d’un nom à la sélection. Les sélections ne doivent inclure aucun code de mise en forme d’un traitement de texte, tel que Microsoft Word. Pour vous assurer qu’aucun code de mise en forme n’est inclus dans la sélection, enregistrez le fichier sous forme de fichier ASCII ou texte brut.

> [!Note]  
> Les éléments et les attributs ne respectent pas la casse. Le texte utilisé dans la sélection pour définir un élément ou un attribut peut être en majuscules ou en minuscules, ou un mélange des deux.

 

Si un élément n’a pas d’éléments enfants (ceux qui modifient ou sont contenus dans un autre élément), une barre oblique (/) peut être utilisée à la fin de la balise d’ouverture, juste avant le' > ', à la place d’une balise de fermeture. Les éléments enfants d’un élément doivent apparaître entre les balises d’ouverture et de fermeture de cet élément ; dans le cas contraire, ils ne sont pas des éléments enfants pour cet élément et sont ignorés ou provoquent une erreur dans la syntaxe de la playlist.

Les quatre premiers caractères d’une sélection doivent être « &lt; ASX ». L’élément **ASX** est utilisé dans toutes les sélections, que son extension soit. Wax,. wvx ou. asx. Il ne doit y avoir qu’un seul élément **ASX** par playlist. Cet élément identifie le fichier comme une sélection de métafichiers Windows Media. Elle ne spécifie pas le type de sélection.

L’élément **ASX** a trois attributs possibles :

**VERSION**

L’attribut **version** est obligatoire et doit suivre immédiatement après l’élément **ASX** , par exemple « <ASX version = "3,0" &gt; ». Le numéro de version actuel est 3,0. Le lecteur Windows Media prend en charge toutes les versions précédentes. Les valeurs acceptables pour l’attribut **version** incluent à la fois 3,0 et 3 (sans virgule décimale).

**PREVIEWMODE**

L’attribut **PREVIEWMODE** est facultatif. Il fournit un autre mécanisme pour spécifier la durée de rendu d’un clip. Si la valeur de l’attribut **PREVIEWMODE** est Yes, le lecteur Windows Media affiche chaque clip pendant la durée spécifiée par l’élément **PREVIEWDURATION**. Un **PREVIEWDURATION** peut être spécifié pour chaque clip.

**BANNERBAR**

L’attribut facultatif **BANNERBAR** définit si le contrôle du lecteur Windows Media réserve de l’espace pour un graphique de bannière. (Utilisez l’élément **bannière** pour spécifier le graphique à afficher.) Si la valeur de **BANNERBAR** est fixe, le lecteur Windows Media réserve de l’espace de bannière pour l’affichage et pour chaque clip, que la sélection de métafichier spécifie une bannière pour le diaporama ou le clip. Cela permet de conserver la taille de la fenêtre du lecteur Windows Media le même (sauf si la taille de la vidéo change) indépendamment de l’absence ou de la présence d’un graphique de bannière. Si aucune bannière n’est associée à l’affichage ou au clip, l’espace réservé pour celui-ci est noir. Si la valeur de l’attribut **BANNERBAR** est auto, le lecteur Windows Media réserve de l’espace pour la bannière uniquement lorsque le diaporama ou le clip en contient un.


```XML
<ASX version="3.0" BANNERBAR="AUTO" >

```



Pour plus d’informations sur les trois attributs de l’élément **ASX** , consultez l’entrée de référence de l' [élément ASX](asx-element.md).

Un élément **ASX** contient des éléments enfants d' **entrée** qui définissent des informations sur les fichiers multimédias à accéder. Chaque élément d' **entrée** doit contenir un élément **ref** qui spécifie le chemin d’accès au fichier multimédia à diffuser en continu. Il doit y avoir au moins une **entrée** ou un élément **ENTRYREF** dans un élément **ASX** .

Les autres éléments définis dans l’étendue de l’élément **ASX** , tels que **title** et **Author**, sont associés aux métadonnées affichées par le lecteur Windows Media.

Les sélections les plus simples sont créées en ajoutant plusieurs éléments d' **entrée** avec un seul élément **ref** à un métafichier. Chaque élément d' **entrée** d’une sélection de métafichier est restitué dans l’ordre dans lequel il apparaît dans le fichier comme si l’utilisateur avait ouvert manuellement chaque clip.

Exemple de code


```XML
<ASX version = "3.0">
<!--A simple playlist with entries to be played in sequence.-->
    <Title>The Show Title</Title>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title1.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title2.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title3.wma" />
    </Entry>
</ASX>

```



Assurez-vous que la sélection fonctionne en double-cliquant dessus dans l’Explorateur Windows. Le lecteur Windows Media doit ouvrir et démarrer la diffusion en continu du contenu multimédia. Une fois que vous avez confirmé que la sélection fonctionne, enregistrez-la sur votre serveur Web avec vos pages Web, et liez-la au moyen d’un élément **href** , ou incorporez-la dans une page Web à l’aide de l’élément **objet** du lecteur Windows Media.

Les sections suivantes contiennent des informations supplémentaires :

-   [Imbrication de refichiers](nesting-metafiles.md)
-   [Utilisation de pages ASP pour créer dynamiquement des sélections de métafichiers Windows Media](using-asp-pages-to-dynamically-create-windows-media-metafile-playlists.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Élément BANNER**](banner-element.md)
</dt> <dt>

[**Exemples de sélections**](example-playlists.md)
</dt> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guide des métafichiers Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




