---
description: à partir de Windows Vista, l’affichage des catégories du panneau de configuration fournit des liens vers les tâches sous chaque icône de l’élément du panneau de configuration, comme illustré ici.
ms.assetid: 54a03536-6fe6-4304-a555-58e5bca128b9
title: Création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7be43d98ea6c0f1cdf2d9c399aa1377d6b7b46a36fed10b3d6a4796ce49f92d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943399"
---
# <a name="creating-searchable-task-links-for-a-control-panel-item"></a>Création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration

à partir de Windows Vista, l’affichage des catégories du panneau de configuration fournit des liens vers les tâches sous chaque icône de l’élément du panneau de configuration, comme illustré ici.

![Liens de tâches sur la page système et catégorie de maintenance](images/controlpaneltasklinks.png)

Quand un utilisateur entre du texte dans la zone de **recherche** située dans le coin supérieur droit de la fenêtre, les résultats de la recherche incluent ces liens de tâches, comme illustré ici pour une recherche sur le mot « afficher ».

![Liens de tâches dans les résultats de la recherche du panneau de configuration](images/controlpanelsearchresults.png)

Cette rubrique traite des sujets suivants :

-   [Meilleures pratiques relatives aux liaisons de tâches](#task-link-best-practices)
-   [Création d’un fichier de tâche XML](#creating-a-task-xml-file)
-   [Localiser des liens de tâches](#localizing-task-links)
-   [Mots clés et recherche](#keywords-and-searching)
-   [Rubriques connexes](#related-topics)

## <a name="task-link-best-practices"></a>Meilleures pratiques relatives aux liaisons de tâches

Il est recommandé de fournir des liens de tâches pour les éléments du panneau de configuration en tant qu’aide aux utilisateurs qui recherchent des fonctionnalités. Il est également possible d’ajouter des mots clés aux liens de tâche afin qu’un utilisateur puisse les trouver même sans connaître le titre ou la terminologie d’une tâche.

Les meilleurs liens de tâches répondent à trois objectifs :

1.  Fournissez un raccourci vers les fonctionnalités de l’élément du panneau de configuration.
2.  Fournissez des mots clés afin que les utilisateurs puissent effectuer des recherches dans leur propre langue. Un utilisateur peut vouloir taper « compactage », car il connaît le terme technique. Un utilisateur peut taper « DB trop grand » ou « taille de base de données ». L’ajout de mots clés appropriés à la tâche signifie que les utilisateurs peuvent trouver votre élément du panneau de configuration.
3.  Fournir des indications sur ce que fait l’élément du panneau de configuration. Quand un utilisateur voit les liens sous l’icône d’un élément du panneau de configuration, il peut obtenir plus d’informations sur l’utilisation de l’élément du panneau de configuration par rapport au nom et à l’icône que seul peut fournir.

Les liaisons de tâches doivent être axées sur les utilisateurs finaux, et non sur la technologie ou sur les fonctionnalités. Par exemple, le terme « activer la compression de la base de données » serait incorrect, car il s’agit d’un jargon technique qui n’est pas familier à la majorité des utilisateurs. « Rendre mon fichier de base de données plus petit » est préférable, car il mentionne l’objectif final réel de l’utilisateur plutôt que le mécanisme pour y accéder. L’objectif n’est pas de se simplifier, mais plutôt d’expression de la tâche en termes de ce que l’utilisateur souhaite accomplir.

## <a name="creating-a-task-xml-file"></a>Création d’un fichier de tâche XML

Les liens de tâche sont définis dans un fichier XML. cette section fournit les détails d’un exemple .xml fichier qui définit trois liens de tâches pour un élément du panneau de configuration appelé **Bloc-notes**. Il définit les titres, les mots clés et les lignes de commande pour les liaisons de tâches. Il montre également comment spécifier les liens de tâches qui s’affichent sous quelle catégorie. Un élément du panneau de configuration qui est inscrit pour apparaître dans plusieurs catégories peut afficher différents liens en fonction de la catégorie. Les explications des différents éléments et informations fournis sont fournies sous forme de commentaires dans le document XML lui-même.


```
<?xml version="1.0" ?>
<applications xmlns="http://schemas.microsoft.com/windows/cpltasks/v1" 
              xmlns:sh="http://schemas.microsoft.com/windows/tasks/v1">
    
    <!-- Notepad -->
    <application id="{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}"> 
    <!-- This GUID must match the GUID you created for your Control Panel item,
         and registered in namespace -->
    
        <!-- Solitaire -->
        <sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
            <!-- This is a generated GUID, specific to this task link -->
            <sh:name>Play solitaire</sh:name>
            <sh:keywords>solitare;game;cards;ace;diamond;heart;club;single</sh:keywords>
            <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
        </sh:task>

        <!-- Task Manager -->
        <sh:task id="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}" needsElevation="true"> 
            <!-- This is a generated GUID, specific to this task link -->
            <!-- The needsElevation="true" attribute means that the task 
                 appears with a shield icon next to it. Adding this attribute 
                 does not cause the .exe to require elevation - it just adds an 
                 icon to tell users that the command already requires it -->
            <sh:name>See running processes</sh:name>
            <sh:keywords>taskmgr;taskman;running processes;threads;cpu;</sh:keywords>
            <sh:command>taskmgr.exe</sh:command>
        </sh:task>

        <!-- IE -->
        <sh:task id="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}">
            <sh:name>Open Internet Explorer</sh:name>
            <sh:keywords>IE;web;browser;net;Internet;ActiveX;plug-in;plugin</sh:keywords>
            <sh:command>iexplore.exe</sh:command>
        </sh:task>
        
        <!-- Category assignments -->

        <!-- Appearance and Personalization -->
        <category id="1"> 
        <!-- These idref attributes refer to the GUIDs of the tasks defined above. A maximum of five tasks are shown per category. -->
            <sh:task idref="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"/>   
            <sh:task idref="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}"/>
            <sh:task idref="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}"/>
        </category>
        
        <!-- Programs -->
        <category id="8"> 
            <sh:task idref="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}">
                <sh:name>Click here to play</sh:name>
                <!-- This overrides the defined text. When the Notepad Control 
                     Panel item appears in the Programs category, it uses the 
                     "Click here to play" text for this Solitaire link, instead 
                     of "Play solitaire". -->
            </sh:task>
            <sh:task idref="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}"/>
            <sh:task idref="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}"/>
       </category>
   </application>
</applications>
```



> [!Note]  
> à partir de Windows 7, un élément du panneau de configuration peut être identifié par son nom canonique plutôt que par son nom d’exécutable : l’élément **<sh : controlpanel>** peut être utilisé à la place de **<sh : command>**. L’élément **<SH : controlpanel>** fournit également un attribut pour spécifier la page de l’élément auquel il doit s’ouvrir. L’exemple suivant illustre l’élément **<SH : controlpanel>** :

 


```
<sh:controlpanel name="Microsoft.Presentation" page="pageWallpaper"/>
```



## <a name="localizing-task-links"></a>Localiser des liens de tâches

Le texte des titres et des mots clés des liens de tâche peut être stocké dans une table de chaînes dans le module de l’élément du panneau de configuration. Dans ce cas, le format utilisé dans le fichier XML est le suivant :


```
<sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
    <!-- This is a generated GUID, specific to this task link -->
    <sh:name>@myTextResources.dll,-100</sh:name>
    <sh:keywords>@myTextResources.dll,-101</sh:keywords>
    <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
</sh:task>
```



Dans cet exemple, le texte du nom de la tâche s’affiche dans l’ID de ressource de chaîne 100 dans myTextResources.dll, et le texte des mots clés apparaît dans l’ID de ressource de chaîne 101.

## <a name="keywords-and-searching"></a>Mots clés et recherche

La recherche du panneau de configuration recherche des liens de tâches en fonction de leur nom et également de leurs mots clés. Elle met en correspondance chaque mot de la recherche par le préfixe des mots du nom et des mots clés. Par exemple, la chaîne de requête « CPU » correspond à la tâche « voir les processus en cours d’exécution » dans l’exemple précédent, car « UC » se trouve dans la liste de mots clés. La chaîne de requête « Pro » trouve également ce résultat, car le mot de titre « Processes » commence par cette chaîne. Notez que la requête ne correspond qu’à des préfixes. La chaîne de requête « tionnaire » ne correspondrait pas à un résultat, car cette chaîne, alors qu’elle fait partie du mot de titre « process », ne commence pas par ce mot.

Quand une requête de recherche contient plusieurs jetons, tous les jetons doivent correspondre au préfixe d’un mot clé ou d’une partie du titre de la tâche pour obtenir un résultat. La requête « Level CPU » ne correspond pas, car « Level » n’est pas dans le mot clé Set. La requête « CPU Run » donne un résultat, car « CPU » correspond à un mot clé, et « Run » est le préfixe du mot « Running » dans le titre de la tâche.

Le panneau de configuration ne fournit pas automatiquement de correction orthographique ni de variations telles que le pluriel ou la césure. Les correspondances sont également non sensibles à la casse. Pour garantir la réussite de la liste de mots clés, il est recommandé de fournir des variantes vous-même, par exemple pour ce lien de tâche qui implique des économiseurs d’écran : « économiseurs d’écran, économiseurs d’écran ; économiseurs d’écran ».

Il n’est pas nécessaire d’ajouter l’écran de veille « singulier », car une requête qui recherche des « économiseurs d’écran » trouvera également « économiseur d’écran » en raison de la correspondance du préfixe. Un utilisateur qui tape une partie du mot, par exemple « screens », verra toujours une correspondance sur un lien de tâche qui contient « économiseurs d’écran » comme mot clé. Pour les langues où les formes plurielles changent le mot, il est nécessaire de placer toutes les formes qu’un utilisateur peut raisonnablement être amené à taper dans les mots clés.

En guise de Convention, Microsoft a omis de petits mots tels que « comment faire » ou « je souhaite » dans l’ensemble de mots-clés. L’objectif est que la plupart des utilisateurs tapent simplement les mots les plus importants tels que « Mouse », « contraste élevé » ou « pilote vidéo » pour obtenir les résultats.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Éléments du panneau de configuration](control-panel-applications.md)
</dt> <dt>

[Conseils sur l’expérience utilisateur](user-experience-guidelines.md)
</dt> <dt>

[Inscription des éléments du panneau de configuration](registering-control-panel-items.md)
</dt> <dt>

[Utilisation de CPLApplet](using-cplapplet.md)
</dt> <dt>

[Traitement des messages du panneau de configuration](message-processing.md)
</dt> <dt>

[Exécution des éléments du panneau de configuration](executing-control-panel-items.md)
</dt> <dt>

[Extension des éléments du panneau de configuration système](extending-system-control-panel-items.md)
</dt> <dt>

[Affectation des catégories du panneau de configuration](assigning-control-panel-categories.md)
</dt> <dt>

[accès au panneau de configuration en Mode Coffre sous Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



