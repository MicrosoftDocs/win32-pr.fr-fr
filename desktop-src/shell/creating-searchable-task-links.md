---
description: À compter de Windows Vista, l’affichage des catégories du panneau de configuration fournit des liens vers les tâches sous chaque icône de l’élément du panneau de configuration, comme illustré ici.
ms.assetid: 54a03536-6fe6-4304-a555-58e5bca128b9
title: Création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b4e98e8a6e07f84e8012b58cefe8e0d249fc069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862126"
---
# <a name="creating-searchable-task-links-for-a-control-panel-item"></a><span data-ttu-id="95c80-103">Création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="95c80-103">Creating Searchable Task Links for a Control Panel Item</span></span>

<span data-ttu-id="95c80-104">À compter de Windows Vista, l’affichage des catégories du panneau de configuration fournit des liens vers les tâches sous chaque icône de l’élément du panneau de configuration, comme illustré ici.</span><span class="sxs-lookup"><span data-stu-id="95c80-104">As of Windows Vista, the Control Panel category view provides task links beneath each Control Panel item's icon as shown here.</span></span>

![Liens de tâches sur la page système et catégorie de maintenance](images/controlpaneltasklinks.png)

<span data-ttu-id="95c80-106">Quand un utilisateur entre du texte dans la zone de **recherche** située dans le coin supérieur droit de la fenêtre, les résultats de la recherche incluent ces liens de tâches, comme illustré ici pour une recherche sur le mot « afficher ».</span><span class="sxs-lookup"><span data-stu-id="95c80-106">When a user enters text in the **Search** box in the upper right of the window, the search results include these task links as shown here for a search on the word "display".</span></span>

![Liens de tâches dans les résultats de la recherche du panneau de configuration](images/controlpanelsearchresults.png)

<span data-ttu-id="95c80-108">Cette rubrique traite des sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="95c80-108">This topic discusses the following:</span></span>

-   [<span data-ttu-id="95c80-109">Meilleures pratiques relatives aux liaisons de tâches</span><span class="sxs-lookup"><span data-stu-id="95c80-109">Task Link Best Practices</span></span>](#task-link-best-practices)
-   [<span data-ttu-id="95c80-110">Création d’un fichier de tâche XML</span><span class="sxs-lookup"><span data-stu-id="95c80-110">Creating a Task XML File</span></span>](#creating-a-task-xml-file)
-   [<span data-ttu-id="95c80-111">Localiser des liens de tâches</span><span class="sxs-lookup"><span data-stu-id="95c80-111">Localizing Task Links</span></span>](#localizing-task-links)
-   [<span data-ttu-id="95c80-112">Mots clés et recherche</span><span class="sxs-lookup"><span data-stu-id="95c80-112">Keywords and Searching</span></span>](#keywords-and-searching)
-   [<span data-ttu-id="95c80-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95c80-113">Related topics</span></span>](#related-topics)

## <a name="task-link-best-practices"></a><span data-ttu-id="95c80-114">Meilleures pratiques relatives aux liaisons de tâches</span><span class="sxs-lookup"><span data-stu-id="95c80-114">Task Link Best Practices</span></span>

<span data-ttu-id="95c80-115">Il est recommandé de fournir des liens de tâches pour les éléments du panneau de configuration en tant qu’aide aux utilisateurs qui recherchent des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="95c80-115">It is recommended that you provide task links for your Control Panel items as an aid to users searching for functionality.</span></span> <span data-ttu-id="95c80-116">Il est également possible d’ajouter des mots clés aux liens de tâche afin qu’un utilisateur puisse les trouver même sans connaître le titre ou la terminologie d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="95c80-116">It is also possible to add keywords to the task links so that a user can find them even without knowing a task's title or terminology.</span></span>

<span data-ttu-id="95c80-117">Les meilleurs liens de tâches répondent à trois objectifs :</span><span class="sxs-lookup"><span data-stu-id="95c80-117">The best task links serve three purposes:</span></span>

1.  <span data-ttu-id="95c80-118">Fournissez un raccourci vers les fonctionnalités de l’élément du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="95c80-118">Provide a shortcut to the functionality of the Control Panel item.</span></span>
2.  <span data-ttu-id="95c80-119">Fournissez des mots clés afin que les utilisateurs puissent effectuer des recherches dans leur propre langue.</span><span class="sxs-lookup"><span data-stu-id="95c80-119">Provide keywords so that users can search using their own language.</span></span> <span data-ttu-id="95c80-120">Un utilisateur peut vouloir taper « compactage », car il connaît le terme technique.</span><span class="sxs-lookup"><span data-stu-id="95c80-120">A user may want to type "compaction" because he or she knows the technical term.</span></span> <span data-ttu-id="95c80-121">Un utilisateur peut taper « DB trop grand » ou « taille de base de données ».</span><span class="sxs-lookup"><span data-stu-id="95c80-121">A user may type "DB too big", or "database filesize".</span></span> <span data-ttu-id="95c80-122">L’ajout de mots clés appropriés à la tâche signifie que les utilisateurs peuvent trouver votre élément du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="95c80-122">Adding suitable keywords to the task means that users can find your Control Panel item.</span></span>
3.  <span data-ttu-id="95c80-123">Fournir des indications sur ce que fait l’élément du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="95c80-123">Provide hints about what the Control Panel item does.</span></span> <span data-ttu-id="95c80-124">Quand un utilisateur voit les liens sous l’icône d’un élément du panneau de configuration, il peut obtenir plus d’informations sur l’utilisation de l’élément du panneau de configuration par rapport au nom et à l’icône que seul peut fournir.</span><span class="sxs-lookup"><span data-stu-id="95c80-124">When a user sees the links beneath a Control Panel item's icon, they can get more information about what the Control Panel item is used for than the name and icon alone can provide.</span></span>

<span data-ttu-id="95c80-125">Les liaisons de tâches doivent être axées sur les utilisateurs finaux, et non sur la technologie ou sur les fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="95c80-125">Task links should be end-user focused, not technology- or feature-focused.</span></span> <span data-ttu-id="95c80-126">Par exemple, le terme « activer la compression de la base de données » serait incorrect, car il s’agit d’un jargon technique qui n’est pas familier à la majorité des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="95c80-126">For example, "Enable database compaction" would be bad wording because it is technical jargon unfamiliar to the majority of users.</span></span> <span data-ttu-id="95c80-127">« Rendre mon fichier de base de données plus petit » est préférable, car il mentionne l’objectif final réel de l’utilisateur plutôt que le mécanisme pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="95c80-127">"Make my database file smaller" is better because it mentions the user's actual end goal rather than the mechanism to get there.</span></span> <span data-ttu-id="95c80-128">L’objectif n’est pas de se simplifier, mais plutôt d’expression de la tâche en termes de ce que l’utilisateur souhaite accomplir.</span><span class="sxs-lookup"><span data-stu-id="95c80-128">The goal is not to oversimplify, but rather to phrase the task in terms of what the user wants to accomplish.</span></span>

## <a name="creating-a-task-xml-file"></a><span data-ttu-id="95c80-129">Création d’un fichier de tâche XML</span><span class="sxs-lookup"><span data-stu-id="95c80-129">Creating a Task XML File</span></span>

<span data-ttu-id="95c80-130">Les liens de tâche sont définis dans un fichier XML.</span><span class="sxs-lookup"><span data-stu-id="95c80-130">Task links are defined in an XML file.</span></span> <span data-ttu-id="95c80-131">Cette section fournit les détails d’un exemple de fichier. XML qui définit trois liens de tâches pour un élément du panneau de configuration appelé **bloc-notes**.</span><span class="sxs-lookup"><span data-stu-id="95c80-131">This section provides the details of an example .xml file that defines three task links for a Control Panel item called **Notepad**.</span></span> <span data-ttu-id="95c80-132">Il définit les titres, les mots clés et les lignes de commande pour les liaisons de tâches.</span><span class="sxs-lookup"><span data-stu-id="95c80-132">It defines titles, keywords, and the command lines for the task links.</span></span> <span data-ttu-id="95c80-133">Il montre également comment spécifier les liens de tâches qui s’affichent sous quelle catégorie.</span><span class="sxs-lookup"><span data-stu-id="95c80-133">It also illustrates how to specify which task links appear under which category.</span></span> <span data-ttu-id="95c80-134">Un élément du panneau de configuration qui est inscrit pour apparaître dans plusieurs catégories peut afficher différents liens en fonction de la catégorie.</span><span class="sxs-lookup"><span data-stu-id="95c80-134">A Control Panel item that is registered to appear in more than one category has the option of showing different links depending on the category.</span></span> <span data-ttu-id="95c80-135">Les explications des différents éléments et informations fournis sont fournies sous forme de commentaires dans le document XML lui-même.</span><span class="sxs-lookup"><span data-stu-id="95c80-135">Explanations of the various elements and information provided are given as comments in the XML itself.</span></span>


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
> <span data-ttu-id="95c80-136">À compter de Windows 7, un élément du panneau de configuration peut être identifié par son nom canonique plutôt que par son nom d’exécutable : l’élément **<SH : controlpanel>** peut être utilisé à la place de **<sh : Command>**.</span><span class="sxs-lookup"><span data-stu-id="95c80-136">As of Windows 7, a Control Panel item can be identified by its canonical name rather than its executable name: the **<sh:controlpanel>** element can be used in place of **<sh:command>**.</span></span> <span data-ttu-id="95c80-137">L’élément **<SH : controlpanel>** fournit également un attribut pour spécifier la page de l’élément auquel il doit s’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="95c80-137">The **<sh:controlpanel>** element also provides an attribute to specify the page of the item to which it should open.</span></span> <span data-ttu-id="95c80-138">L’exemple suivant illustre l’élément **<SH : controlpanel>** :</span><span class="sxs-lookup"><span data-stu-id="95c80-138">The following shows an example of the **<sh:controlpanel>** element:</span></span>

 


```
<sh:controlpanel name="Microsoft.Presentation" page="pageWallpaper"/>
```



## <a name="localizing-task-links"></a><span data-ttu-id="95c80-139">Localiser des liens de tâches</span><span class="sxs-lookup"><span data-stu-id="95c80-139">Localizing Task Links</span></span>

<span data-ttu-id="95c80-140">Le texte des titres et des mots clés des liens de tâche peut être stocké dans une table de chaînes dans le module de l’élément du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="95c80-140">The text for the task links' titles and keywords can be stored in a string table in the Control Panel item's module.</span></span> <span data-ttu-id="95c80-141">Dans ce cas, le format utilisé dans le fichier XML est le suivant :</span><span class="sxs-lookup"><span data-stu-id="95c80-141">In that case, the format used in the XML file becomes:</span></span>


```
<sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
    <!-- This is a generated GUID, specific to this task link -->
    <sh:name>@myTextResources.dll,-100</sh:name>
    <sh:keywords>@myTextResources.dll,-101</sh:keywords>
    <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
</sh:task>
```



<span data-ttu-id="95c80-142">Dans cet exemple, le texte du nom de la tâche s’affiche dans l’ID de ressource de chaîne 100 dans myTextResources.dll, et le texte des mots clés apparaît dans l’ID de ressource de chaîne 101.</span><span class="sxs-lookup"><span data-stu-id="95c80-142">In this example, the text for the task's name appears in string resource ID 100 in myTextResources.dll, and the text for the keywords appears in string resource ID 101.</span></span>

## <a name="keywords-and-searching"></a><span data-ttu-id="95c80-143">Mots clés et recherche</span><span class="sxs-lookup"><span data-stu-id="95c80-143">Keywords and Searching</span></span>

<span data-ttu-id="95c80-144">La recherche du panneau de configuration recherche des liens de tâches en fonction de leur nom et également de leurs mots clés.</span><span class="sxs-lookup"><span data-stu-id="95c80-144">The Control Panel search finds task links based on their name and also on their keywords.</span></span> <span data-ttu-id="95c80-145">Elle met en correspondance chaque mot de la recherche par le préfixe des mots du nom et des mots clés.</span><span class="sxs-lookup"><span data-stu-id="95c80-145">It matches each word in the search with the prefix of words in the name and keywords.</span></span> <span data-ttu-id="95c80-146">Par exemple, la chaîne de requête « CPU » correspond à la tâche « voir les processus en cours d’exécution » dans l’exemple précédent, car « UC » se trouve dans la liste de mots clés.</span><span class="sxs-lookup"><span data-stu-id="95c80-146">For example, the query string "cpu" would match the task "See running processes" in the earlier example because "cpu" is in the keyword list.</span></span> <span data-ttu-id="95c80-147">La chaîne de requête « Pro » trouve également ce résultat, car le mot de titre « Processes » commence par cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="95c80-147">The query string "pro" would also find that result because the title word "processes" begins with that string.</span></span> <span data-ttu-id="95c80-148">Notez que la requête ne correspond qu’à des préfixes.</span><span class="sxs-lookup"><span data-stu-id="95c80-148">Note that the query only matches prefixes.</span></span> <span data-ttu-id="95c80-149">La chaîne de requête « tionnaire » ne correspondrait pas à un résultat, car cette chaîne, alors qu’elle fait partie du mot de titre « process », ne commence pas par ce mot.</span><span class="sxs-lookup"><span data-stu-id="95c80-149">The query string "rocess" would not match a result because that string, while part of the title word "process", does not begin that word.</span></span>

<span data-ttu-id="95c80-150">Quand une requête de recherche contient plusieurs jetons, tous les jetons doivent correspondre au préfixe d’un mot clé ou d’une partie du titre de la tâche pour obtenir un résultat.</span><span class="sxs-lookup"><span data-stu-id="95c80-150">When a search query contains multiple tokens, all the tokens must match the prefix of some keyword or part of the task title for a result.</span></span> <span data-ttu-id="95c80-151">La requête « Level CPU » ne correspond pas, car « Level » n’est pas dans le mot clé Set.</span><span class="sxs-lookup"><span data-stu-id="95c80-151">The query "cpu level" would not match, because "level" is not in the keyword set.</span></span> <span data-ttu-id="95c80-152">La requête « CPU Run » donne un résultat, car « CPU » correspond à un mot clé, et « Run » est le préfixe du mot « Running » dans le titre de la tâche.</span><span class="sxs-lookup"><span data-stu-id="95c80-152">The query "cpu run" would give a result, because "cpu" matches a keyword, and "run" is the prefix of the word "running" in the task's title.</span></span>

<span data-ttu-id="95c80-153">Le panneau de configuration ne fournit pas automatiquement de correction orthographique ni de variations telles que le pluriel ou la césure.</span><span class="sxs-lookup"><span data-stu-id="95c80-153">Control Panel does not automatically provide spelling correction or variations such as plurals or hyphenation.</span></span> <span data-ttu-id="95c80-154">Les correspondances sont également non sensibles à la casse.</span><span class="sxs-lookup"><span data-stu-id="95c80-154">Matches are also case-insensitive.</span></span> <span data-ttu-id="95c80-155">Pour garantir la réussite de la liste de mots clés, il est recommandé de fournir des variantes vous-même, par exemple pour ce lien de tâche qui implique des économiseurs d’écran : « économiseurs d’écran, économiseurs d’écran ; économiseurs d’écran ».</span><span class="sxs-lookup"><span data-stu-id="95c80-155">To ensure a successful keyword list, it is recommended to provide variations yourself, such as for this task link that involves screen savers: "screensavers;screen-savers;screen savers;"</span></span>

<span data-ttu-id="95c80-156">Il n’est pas nécessaire d’ajouter l’écran de veille « singulier », car une requête qui recherche des « économiseurs d’écran » trouvera également « économiseur d’écran » en raison de la correspondance du préfixe.</span><span class="sxs-lookup"><span data-stu-id="95c80-156">There is no need to add the singular "screensaver", because a query that finds "screensavers" will also find "screensaver" due to the prefix match.</span></span> <span data-ttu-id="95c80-157">Un utilisateur qui tape une partie du mot, par exemple « screens », verra toujours une correspondance sur un lien de tâche qui contient « économiseurs d’écran » comme mot clé.</span><span class="sxs-lookup"><span data-stu-id="95c80-157">A user typing even part of the word, like "screensa" will still see a match on a task link that has "screensavers" as a keyword.</span></span> <span data-ttu-id="95c80-158">Pour les langues où les formes plurielles changent le mot, il est nécessaire de placer toutes les formes qu’un utilisateur peut raisonnablement être amené à taper dans les mots clés.</span><span class="sxs-lookup"><span data-stu-id="95c80-158">For languages where plural forms change the word, it is necessary to put all the forms a user could reasonably be expected to type into the keywords.</span></span>

<span data-ttu-id="95c80-159">En guise de Convention, Microsoft a omis de petits mots tels que « comment faire » ou « je souhaite » dans l’ensemble de mots-clés.</span><span class="sxs-lookup"><span data-stu-id="95c80-159">As a convention, Microsoft has omitted small words like "how do I" or "I want to" from the set of keywords.</span></span> <span data-ttu-id="95c80-160">L’objectif est que la plupart des utilisateurs tapent simplement les mots les plus importants tels que « Mouse », « contraste élevé » ou « pilote vidéo » pour obtenir les résultats.</span><span class="sxs-lookup"><span data-stu-id="95c80-160">The expectation is that most users will simply type the most important words such as "mouse", "high contrast", or "video driver" to get results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95c80-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95c80-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95c80-162">Éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="95c80-162">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="95c80-163">Conseils sur l’expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="95c80-163">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="95c80-164">Inscription des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="95c80-164">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="95c80-165">Utilisation de CPLApplet</span><span class="sxs-lookup"><span data-stu-id="95c80-165">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="95c80-166">Traitement des messages du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="95c80-166">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="95c80-167">Exécution des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="95c80-167">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="95c80-168">Extension des éléments du panneau de configuration système</span><span class="sxs-lookup"><span data-stu-id="95c80-168">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="95c80-169">Affectation des catégories du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="95c80-169">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="95c80-170">Accès au panneau de configuration en mode sans échec sous Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95c80-170">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



