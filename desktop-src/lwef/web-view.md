---
title: Personnalisation de l’affichage Web d’un dossier
description: Une vue Web est un moyen puissant et flexible d’utiliser l’Explorateur Windows pour afficher des informations sur le contenu d’un dossier de Shell.
ms.assetid: a894df21-bcc6-4760-b7d7-9bf95a0dba7f
keywords:
- Affichages Web
- Style classique
- Style Web
- bannières
- Zone FileList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e364551d461eff6ae17a780bafc0b69182a1f16f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724693"
---
# <a name="customizing-a-folders-web-view"></a><span data-ttu-id="0edde-108">Personnalisation de l’affichage Web d’un dossier</span><span class="sxs-lookup"><span data-stu-id="0edde-108">Customizing a Folder's Web View</span></span>

<span data-ttu-id="0edde-109">\[Cette fonctionnalité est prise en charge uniquement sous Windows XP ou version antérieure.</span><span class="sxs-lookup"><span data-stu-id="0edde-109">\[This feature is supported only under Windows XP or earlier.</span></span> <span data-ttu-id="0edde-110">\]</span><span class="sxs-lookup"><span data-stu-id="0edde-110">\]</span></span>

<span data-ttu-id="0edde-111">Une vue Web est un moyen puissant et flexible d’utiliser l’Explorateur Windows pour afficher des informations sur le contenu d’un dossier de Shell.</span><span class="sxs-lookup"><span data-stu-id="0edde-111">A Web view is a powerful and flexible way to use the Windows Explorer to display information about the contents of a Shell folder.</span></span>

-   [<span data-ttu-id="0edde-112">Introduction</span><span class="sxs-lookup"><span data-stu-id="0edde-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="0edde-113">Utilisation du modèle d’affichage Web</span><span class="sxs-lookup"><span data-stu-id="0edde-113">Using the Web View Template</span></span>](#using-the-web-view-template)
    -   [<span data-ttu-id="0edde-114">Corps du modèle</span><span class="sxs-lookup"><span data-stu-id="0edde-114">The Template Body</span></span>](#the-template-body)
    -   [<span data-ttu-id="0edde-115">L’en-tête de modèle</span><span class="sxs-lookup"><span data-stu-id="0edde-115">The Template Head</span></span>](#the-template-head)
-   [<span data-ttu-id="0edde-116">Résumé</span><span class="sxs-lookup"><span data-stu-id="0edde-116">Summary</span></span>](#summary)

## <a name="introduction"></a><span data-ttu-id="0edde-117">Introduction</span><span class="sxs-lookup"><span data-stu-id="0edde-117">Introduction</span></span>

<span data-ttu-id="0edde-118">Windows offre aux utilisateurs deux méthodes principales pour afficher et parcourir l’espace de noms Shell.</span><span class="sxs-lookup"><span data-stu-id="0edde-118">Windows offers users two primary ways to view and navigate the Shell namespace.</span></span> <span data-ttu-id="0edde-119">Le style classique, le plus familier, est semblable au gestionnaire de fichiers Windows familier.</span><span class="sxs-lookup"><span data-stu-id="0edde-119">The most familiar of these, the Classic style, is similar to the familiar Windows File Manager.</span></span> <span data-ttu-id="0edde-120">Le volet droit répertorie le contenu du dossier actuellement sélectionné dans l’un des cinq formats suivants : grande icône, petite icône, liste, détails et miniature.</span><span class="sxs-lookup"><span data-stu-id="0edde-120">The right pane lists the contents of the currently selected folder in one of five formats: Large Icon, Small Icon, List, Details, and Thumbnail.</span></span> <span data-ttu-id="0edde-121">La principale différence par rapport au gestionnaire de fichiers Windows est le volet gauche, qui ressemble beaucoup à la barre d’exploration de Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="0edde-121">The major difference from Windows File Manager is the left pane, which looks very similar to the Explorer bar of Windows Internet Explorer.</span></span> <span data-ttu-id="0edde-122">Il peut être redimensionné ou supprimé, et il peut afficher plusieurs volets en plus de l’arborescence de système de fichiers familière, telle qu’un volet de recherche.</span><span class="sxs-lookup"><span data-stu-id="0edde-122">It can be resized or removed, and it can display several panes in addition to the familiar file system tree, such as a search pane.</span></span>

> [!Note]  
> <span data-ttu-id="0edde-123">Les informations contenues dans ce document ne s’appliquent pas à Windows XP, les techniques abordées s’appliquent uniquement aux versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="0edde-123">The information in this document does not apply to Windows XP, the techniques discussed apply only to earlier versions of Windows.</span></span>

 

<span data-ttu-id="0edde-124">L’illustration suivante montre le dossier Imprimantes dans le style classique.</span><span class="sxs-lookup"><span data-stu-id="0edde-124">The following illustration shows the Printers folder in Classic style.</span></span>

![style classique du dossier Imprimantes.](images/webview1.png)

<span data-ttu-id="0edde-126">Le style classique fonctionne raisonnablement bien pour les dossiers et fichiers du système de fichiers normal.</span><span class="sxs-lookup"><span data-stu-id="0edde-126">The Classic style works reasonably well for normal file system folders and files.</span></span> <span data-ttu-id="0edde-127">Toutefois, avec l’introduction de Windows 95, le système de fichiers a évolué vers l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="0edde-127">However, with the introduction of Windows 95, the file system has evolved into the namespace.</span></span> <span data-ttu-id="0edde-128">L’espace de noms permet de créer des *dossiers virtuels*, tels que des imprimantes ou un voisinage réseau, qui peuvent représenter des types d’informations très différents de ceux d’un dossier de système de fichiers normal.</span><span class="sxs-lookup"><span data-stu-id="0edde-128">The namespace allows the creation of *virtual folders*, such as Printers or Network Neighborhood, that can represent very different types of information than a normal file system folder.</span></span>

<span data-ttu-id="0edde-129">Le style Web, également appelé vue Web, offre un moyen plus flexible et plus puissant de présenter des informations que le style classique.</span><span class="sxs-lookup"><span data-stu-id="0edde-129">The Web style, also known as a Web view, offers a more flexible and powerful way of presenting information than Classic style.</span></span> <span data-ttu-id="0edde-130">Dans une vue Web, l’utilisateur affiche et parcourt l’espace de noms à l’aide d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="0edde-130">In a Web view, the user basically views and navigates the namespace using Internet Explorer.</span></span> <span data-ttu-id="0edde-131">La disposition de base d’une vue Web est similaire au style classique.</span><span class="sxs-lookup"><span data-stu-id="0edde-131">The basic layout of a Web view is similar to Classic style.</span></span> <span data-ttu-id="0edde-132">Le volet d’exploration est inchangé.</span><span class="sxs-lookup"><span data-stu-id="0edde-132">The Explorer bar is unchanged.</span></span> <span data-ttu-id="0edde-133">Toutefois, la région occupée par la liste de fichiers devient une zone d’affichage à usage général qui est effectivement une page Web.</span><span class="sxs-lookup"><span data-stu-id="0edde-133">However, the region that was occupied by the file list becomes a general-purpose display area that is effectively a webpage.</span></span> <span data-ttu-id="0edde-134">Un affichage Web est toujours utilisé pour afficher des informations sur le contenu d’un dossier, mais il existe peu de contraintes sur les informations qui sont affichées, ou comment.</span><span class="sxs-lookup"><span data-stu-id="0edde-134">A Web view is still used to display information about the contents of a folder, but there are few constraints on what information is displayed, or how.</span></span> <span data-ttu-id="0edde-135">Chaque dossier peut avoir sa propre vue Web, personnalisée pour l’adapter à ses fonctionnalités particulières.</span><span class="sxs-lookup"><span data-stu-id="0edde-135">Each folder can have its own Web view, customized to suit its particular features.</span></span>

<span data-ttu-id="0edde-136">L’illustration suivante montre une vue Web du dossier Imprimantes (indiqué précédemment dans le style classique).</span><span class="sxs-lookup"><span data-stu-id="0edde-136">The following illustration shows a Web view of the Printers folder (shown previously in Classic style).</span></span>

![vue Web par défaut du dossier Imprimantes.](images/webview2.png)

<span data-ttu-id="0edde-138">À l’instar des pages Web conventionnelles, les vues Web sont contrôlées par un modèle HTML.</span><span class="sxs-lookup"><span data-stu-id="0edde-138">Much like conventional webpages, Web views are controlled by an HTML-based template.</span></span> <span data-ttu-id="0edde-139">La création d’un modèle d’affichage Web est quasiment identique à la création d’une page Web et offre le même degré de flexibilité dans le contenu et la mise en page des informations.</span><span class="sxs-lookup"><span data-stu-id="0edde-139">Authoring a Web view template is nearly identical to authoring a webpage and provides the same degree of flexibility in content and layout of information.</span></span> <span data-ttu-id="0edde-140">Les modèles d’affichage Web peuvent utiliser le DHTML (Dynamic HTML) et les scripts pour répondre aux événements, comme un utilisateur qui clique sur un élément.</span><span class="sxs-lookup"><span data-stu-id="0edde-140">Web view templates can use Dynamic HTML (DHTML) and scripting to respond to events, such as a user clicking an item.</span></span> <span data-ttu-id="0edde-141">Ils peuvent également héberger des objets qui leur permettent d’obtenir et d’afficher des informations à partir du dossier ou de son contenu.</span><span class="sxs-lookup"><span data-stu-id="0edde-141">They can also host objects that allow them to obtain and display information from the folder or its contents.</span></span>

<span data-ttu-id="0edde-142">L’utilisateur peut choisir un affichage Web en démarrant l’Explorateur Windows, en cliquant sur **Options des dossiers** dans le menu **affichage** , puis en sélectionnant cette option : **activer le contenu Web dans les dossiers**.</span><span class="sxs-lookup"><span data-stu-id="0edde-142">The user can choose a Web view by starting Windows Explorer, clicking **Folder Options** on the **View** menu, and selecting this option: **Enable Web content in folders**.</span></span> <span data-ttu-id="0edde-143">Toutefois, l’utilisateur peut également démarrer Internet Explorer et pointer sur le navigateur dans le système de fichiers en cliquant sur le menu **affichage** , en pointant sur **barre d’exploration**, puis en cliquant sur **dossiers**.</span><span class="sxs-lookup"><span data-stu-id="0edde-143">However, the user can also start Internet Explorer and point the browser at the file system by clicking the **View** menu, pointing to **Explorer Bar**, and clicking **Folders**.</span></span> <span data-ttu-id="0edde-144">Dans une vue Web, il n’y a pratiquement aucune différence entre Internet Explorer et l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="0edde-144">In a Web view, there is virtually no difference between Internet Explorer and Windows Explorer.</span></span>

<span data-ttu-id="0edde-145">Sur le côté gauche du volet droit, la vue Web imprimantes affiche une bannière avec le nom et l’icône du dossier, suivis d’un bloc d’informations sur le dossier.</span><span class="sxs-lookup"><span data-stu-id="0edde-145">On the left side of the right pane, the Printers Web view displays a banner with the folder's name and icon, followed by a block of information about the folder.</span></span> <span data-ttu-id="0edde-146">La liste de fichiers habituelle occupe le côté droit de la page.</span><span class="sxs-lookup"><span data-stu-id="0edde-146">The usual file list occupies the right side of the page.</span></span>

<span data-ttu-id="0edde-147">Lorsqu’un utilisateur clique sur un élément, des informations détaillées sur l’élément s’affichent dans le bloc d’informations.</span><span class="sxs-lookup"><span data-stu-id="0edde-147">When a user clicks an item, detailed information about the item appears in the information block.</span></span> <span data-ttu-id="0edde-148">L’affichage Web imprimantes affiche en fait pratiquement les mêmes informations que celles disponibles dans le style classique, mais il le fait dans un format plus utilisable.</span><span class="sxs-lookup"><span data-stu-id="0edde-148">The Printers Web view actually displays much the same information that is available in Classic style, but it does so in a more usable format.</span></span> <span data-ttu-id="0edde-149">Toutefois, une vue Web n’est pas simplement une autre façon d’afficher des informations de style classiques.</span><span class="sxs-lookup"><span data-stu-id="0edde-149">However, a Web view is not simply a different way to display Classic style information.</span></span> <span data-ttu-id="0edde-150">Par exemple, un lien vers un site Web utile peut être affiché sous le bloc d’informations, une fonctionnalité qui n’est pas disponible dans le style classique.</span><span class="sxs-lookup"><span data-stu-id="0edde-150">For example, a link to a useful website can be displayed below the information block, a feature that is not available in Classic style.</span></span> <span data-ttu-id="0edde-151">Si l’utilisateur clique sur le lien, le site s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0edde-151">If the user clicks the link, the site will be displayed.</span></span>

<span data-ttu-id="0edde-152">Le mode Web imprimantes présenté dans l’illustration précédente est semblable au style classique, car le modèle d’affichage Web sous-jacent (fichier. htt) a été écrit de cette façon.</span><span class="sxs-lookup"><span data-stu-id="0edde-152">The Printers Web view shown in the preceding illustration is similar to the Classic style, because the underlying Web view template (an .htt file) was written that way.</span></span> <span data-ttu-id="0edde-153">La liste de fichiers, par exemple, n’est pas générée directement par le modèle d’affichage Web.</span><span class="sxs-lookup"><span data-stu-id="0edde-153">The list of files, for instance, is not generated by the Web view template directly.</span></span> <span data-ttu-id="0edde-154">Elle est créée et affichée par un objet [**WebViewFolderContents**](webviewfoldercontents.md) hébergé par le modèle d’affichage Web.</span><span class="sxs-lookup"><span data-stu-id="0edde-154">It is created and displayed by a [**WebViewFolderContents**](webviewfoldercontents.md) object hosted by the Web view template.</span></span> <span data-ttu-id="0edde-155">Les méthodes et propriétés de l’objet permettent à l’affichage Web de contrôler sa disposition et d’obtenir des informations sur des éléments particuliers.</span><span class="sxs-lookup"><span data-stu-id="0edde-155">The object's methods and properties allow the Web view to control its layout and obtain information about particular items.</span></span> <span data-ttu-id="0edde-156">Le contenu et la mise en page de la bannière et du bloc d’informations sont spécifiés dans le modèle d’affichage Web.</span><span class="sxs-lookup"><span data-stu-id="0edde-156">The content and layout of the banner and information block is specified in the Web view template.</span></span>

<span data-ttu-id="0edde-157">Étant donné qu’une vue Web prend en charge le langage DHTML, le modèle peut également être utilisé pour gérer l’interaction de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0edde-157">Because a Web view supports DHTML, the template can also be used to handle user interaction.</span></span> <span data-ttu-id="0edde-158">Par exemple, lorsqu’un utilisateur clique sur l’une des icônes d’imprimante, l’objet **WebViewFolderIcon** déclenche un événement [**SelectionChanged**](/windows/desktop/shell/application-support-bumper) .</span><span class="sxs-lookup"><span data-stu-id="0edde-158">For instance, when a user clicks one of the printer icons, the **WebViewFolderIcon** object fires a [**SelectionChanged**](/windows/desktop/shell/application-support-bumper) event.</span></span> <span data-ttu-id="0edde-159">Le modèle utilise un gestionnaire d’événements DHTML écrit dans un script pour récupérer les informations demandées et les afficher dans le bloc d’informations.</span><span class="sxs-lookup"><span data-stu-id="0edde-159">The template uses a DHTML event handler written in script to retrieve the requested information and display it in the information block.</span></span>

<span data-ttu-id="0edde-160">Cet exemple simple pour le dossier Printers n’est pas le seul moyen d’utiliser une vue Web.</span><span class="sxs-lookup"><span data-stu-id="0edde-160">This simple example for the Printers folder is by no means the only way to use a Web view.</span></span> <span data-ttu-id="0edde-161">En écrivant votre propre modèle et, si nécessaire, des objets, vous pouvez utiliser une vue Web pour afficher des informations et interagir avec l’utilisateur de la manière la plus efficace.</span><span class="sxs-lookup"><span data-stu-id="0edde-161">By writing your own template and, if necessary, objects, you can use a Web view to display information and interact with the user in whatever way you find most effective.</span></span> <span data-ttu-id="0edde-162">Notez que, à l’heure actuelle, les modèles d’affichage Web affichent uniquement les dossiers virtuels définis par le système.</span><span class="sxs-lookup"><span data-stu-id="0edde-162">Note that, at present, Web view templates only display system-defined virtual folders.</span></span> <span data-ttu-id="0edde-163">Bien que les développeurs puissent créer un dossier virtuel en implémentant une extension d’espace de noms, ils doivent utiliser les techniques décrites dans [extensions d’espace de noms](/windows/desktop/shell/nse-works) pour les afficher.</span><span class="sxs-lookup"><span data-stu-id="0edde-163">Although developers can create a virtual folder by implementing a namespace extension, they must use the techniques described in [Namespace Extensions](/windows/desktop/shell/nse-works) to display it.</span></span>

## <a name="using-the-web-view-template"></a><span data-ttu-id="0edde-164">Utilisation du modèle d’affichage Web</span><span class="sxs-lookup"><span data-stu-id="0edde-164">Using the Web View Template</span></span>

<span data-ttu-id="0edde-165">La façon dont les données sont affichées dans une vue Web peut être personnalisée de façon limitée en modifiant le fichier Desktop.ini d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="0edde-165">The way data is displayed in a Web view can be customized in a limited way by modifying a folder's Desktop.ini file.</span></span> <span data-ttu-id="0edde-166">Pour plus d’informations, consultez [Personnalisation des dossiers avec Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) .</span><span class="sxs-lookup"><span data-stu-id="0edde-166">See [Customizing Folders with Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) for details.</span></span> <span data-ttu-id="0edde-167">Un moyen bien plus flexible et puissant de personnaliser une vue Web consiste à créer un modèle d’affichage Web personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0edde-167">A much more flexible and powerful way to customize a Web view is to create a custom Web view template.</span></span>

<span data-ttu-id="0edde-168">Le modèle d’affichage Web contrôle ce qui est affiché dans une vue Web et comment.</span><span class="sxs-lookup"><span data-stu-id="0edde-168">The Web view template controls what is displayed in a Web view and how.</span></span> <span data-ttu-id="0edde-169">Il utilise des techniques de script, DHTML et HTML standard pour obtenir et afficher des informations et interagir avec l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0edde-169">It uses standard HTML, DHTML, and scripting techniques to obtain and display information and interact with the user.</span></span> <span data-ttu-id="0edde-170">Cette section explique comment créer une vue Web en examinant un modèle simple, générique. htt.</span><span class="sxs-lookup"><span data-stu-id="0edde-170">This section discusses how to create a Web view by examining a simple template—Generic.htt.</span></span>


```
<html>
    <style>
    <!-- This section defines a variety of styles that can be used
     when displaying the document -->
        body        {font: 8pt/10pt verdana; margin: 0}
        #Banner     {position: absolute; width: 100%; height: 88px; background: URL(res://webvw.dll/folder.gif) no-repeat top left}
        #MiniBanner {position: absolute; width: 100%; height: 32px; background: window}
        #Icon       {position: absolute; left: 11px; top: 12px; width: 64px; height: 64px}
        #FileList   {position: absolute; left: 30%; top: 88px; width: 1px; height: 1px}
        #Info       {position: absolute; top: 88px; width: 30%; background: window; overflow: auto}
        p       {margin-left: 20px; margin-right: 8px}
        p.Title     {font: 16pt/16pt verdana; font-weight: bold; color: #0099FF}
        a:link      {color: #FF6633}
        a:visited   {color: #0099FF}
        a:active    {color: black}
    </style>

    <head>
        <!-- allow references to any resources you might add to the
         folder -->
        <base href="%THISDIRPATH%\">

        <script language="JavaScript">
        
        <!-- This section defines a number of JavaScript utilities -->
            var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br><br>To get information about any of them, click the items icon.<br><br>";
            var L_Multiple_Text = " objects selected.";

            function FixSize() {
            // this function handles layout issues not covered by the style sheet

                var hideTop = 200;
                var hideLeft    = 400;
                var miniHeight  = 32;

                if (200 > document.body.clientHeight) {
                //A short window. Use the minibanner
                    document.all.Banner.style.visibility = "hidden";
                    document.all.MiniBanner.style.visibility = "visible";
                    document.all.FileList.style.top = 32;
                    document.all.Info.style.top = 32;
                }

                else {
                //A normal window. Use the normal banner
                    document.all.Banner.style.visibility = "visible";
                    document.all.MiniBanner.style.visibility = "hidden";
                    document.all.FileList.style.top = (document.all.Banner.offsetHeight - 32) + "px";
                    document.all.Info.style.top = (document.all.Banner.offsetHeight) + "px";
                    document.all.Rule.style.width = (document.body.clientWidth > 84 ? document.body.clientWidth - 84 : 0) + "px";     
                }
                if (400 > document.body.clientWidth) {
                //A narrow window. Hide the Info region and expand the file list region
                    document.all.Info.style.visibility = "hidden";
                    document.all.FileList.style.pixelLeft = 0;
                    document.all.FileList.style.pixelTop = document.all.Info.style.pixelTop;
                }

                else {
                //Normal width
                    document.all.Info.style.visibility = "visible";
                    document.all.FileList.style.pixelLeft = document.all.Info.style.pixelWidth;
                }
                document.all.FileList.style.pixelWidth = document.body.clientWidth - document.all.FileList.style.pixelLeft;
                document.all.FileList.style.pixelHeight = document.body.clientHeight - document.all.FileList.style.pixelTop;
                document.all.Info.style.pixelHeight = document.body.clientHeight - document.all.Info.style.pixelTop;
            }

            function Init() {
                /* Set the initial layout and have FixSize() called whenever the window is resized*/
                window.onresize = FixSize;
                FixSize();
                TextBlock.innerHTML = L_Intro_Text;
            }
        </script>

        <script language="JavaScript" for="FileList" event="SelectionChanged">
            // Updates the TextBlock region when an item is selected
            var data;
            var text;

            // name
            text = "<b>" + FileList.FocusedItem.Name + "</b>";

            // comment
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 3);
            if (data)
                text += "<br>" + data;

            // documents
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 1);
            if (data)
                text += "<br><br>" + FileList.Folder.GetDetailsOf(null, 1) + ": " + data;

            // status
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 2);
            if (data)
                text += "<br><br><b><font color=red>" + data + "</font></b>";

            // tip?
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, -1);
            if (data != "" && data != FileList.FocusedItem.Name)
                text += "<br><br>" + data;

            TextBlock.innerHTML = text;
        </script>
    </head>
<!-- The body of the document controls the actual data display.
 It uses several scripting objects to communicate with the
 namespace folder, and calls on the JavaScript objects defined
 in the header to handle much of the processing -->
    <body scroll=no onload="Init()">

        <!-- The normal banner. This banner displays the folder
         name and icon at the top of the WebView pane. This banner
         is used if the WebView pane is sufficiently large to
         display the icon and still have room for some information -->
        <div id="Banner" style="visibility: hidden">
            <!-- Display the folder name using a table with nowrap
             to prevent word wrapping. Explorer will replace
              %THISDIRNAME% with the current folder name -->
            <table class="clsStd"><tr><td nowrap>
                <p class=Title style="margin-left: 104px; margin-top: 16px">
                %THISDIRNAME% 
            </td></tr></table>
            <!-- this is more efficient than a long graphic, but it has to be adjusted in FixSize() -->
            <hr id="Rule" size=1px color=black style="position: absolute; top: 44px; left: 84px">
            <!-- Load the WebViewFolderIcon object, which extracts the folder's icon -->
            <object id=Icon classid="clsid:e5df9d10-3b52-11d1-83e8-00a0c90dc849">
                <param name="scale" value=200>
            </object>
        </div>

        <!-- The mini banner. This banner is used when the
         WebView pane is too short to display the icon. Instead,
          it displays only the folder name -->
        <div id="MiniBanner" style="visibility: hidden">
            <!-- use a table with nowrap to prevent word wrapping -->
            <table class="clsStd"><tr><td nowrap>
                <p class=Title style="margin-left: 16px; margin-top: 4px">
                %THISDIRNAME%
            </td></tr></table>
        </div>

        <!-- The Info region. This displays the information
         associated with a folder or file. Javascript in the header
         is used to generate the regions contents by by assigning
         a text block to TextBlock.innerHTML -->
        <div id="Info">
            <p style="margin-top: 16px");
            <span id="TextBlock">
            </span>
        </div>
        <!-- end left info panel -->

        <!-- Load the WebViewFolderContents object. This object
         returns information on the contents of the folder that
          can be used in the information display.  -->
        <object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>

    </body>
</html>
            
```



<span data-ttu-id="0edde-171">Un moyen simple de créer votre propre modèle d’affichage Web consiste à utiliser Generic. htt et à le modifier.</span><span class="sxs-lookup"><span data-stu-id="0edde-171">A simple way to create your own Web view template is to take Generic.htt and modify it.</span></span> <span data-ttu-id="0edde-172">Étant donné qu’il est plutôt limité, vous devez également consulter d’autres exemples plus complexes pour obtenir des idées supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0edde-172">Because it is rather limited, you should also look at other, more complex examples for additional ideas.</span></span> <span data-ttu-id="0edde-173">Vous pouvez les trouver en recherchant dans votre système l’extension. htt utilisée par tous les modèles d’affichage Web.</span><span class="sxs-lookup"><span data-stu-id="0edde-173">You can find them by searching your system for the .htt extension used by all Web view templates.</span></span> <span data-ttu-id="0edde-174">Si vous souhaitez créer un modèle personnalisé pour un dossier, commencez par le modèle Folder. htt par défaut, qui est généralement stocké dans C : \\ winnt \\ Web ou c : \\ Windows \\ Web.</span><span class="sxs-lookup"><span data-stu-id="0edde-174">If you want to create a custom template for a folder, you should start with the default Folder.htt template, which is usually stored in either C:\\Winnt\\Web or C:\\Windows\\Web.</span></span> <span data-ttu-id="0edde-175">Notez que ces fichiers sont définis comme étant masqués. par conséquent, vous devrez peut-être modifier les paramètres de l’Explorateur Windows pour les afficher.</span><span class="sxs-lookup"><span data-stu-id="0edde-175">Note that these files are defined as hidden, so you may need to modify your Windows Explorer settings to view them.</span></span> <span data-ttu-id="0edde-176">Une fois qu’un fichier. htt est créé, il doit être marqué comme étant en lecture seule et masqué.</span><span class="sxs-lookup"><span data-stu-id="0edde-176">Once an .htt file is created, it should be marked as read-only and hidden.</span></span>

<span data-ttu-id="0edde-177">Les modèles d’affichage Web utilisent l’extension. htt, car ils diffèrent légèrement des documents. htm conventionnels.</span><span class="sxs-lookup"><span data-stu-id="0edde-177">Web view templates use the .htt extension because they differ slightly from conventional .htm documents.</span></span> <span data-ttu-id="0edde-178">La principale différence réside dans le fait que les fichiers. htt remplacent les variables spéciales par les valeurs d’espace de noms actuelles.</span><span class="sxs-lookup"><span data-stu-id="0edde-178">The main difference is several special variables in .htt files that the system replaces with the current namespace values.</span></span> <span data-ttu-id="0edde-179">Les variables% THISDIR% et% THISDIRPATH% représentent le nom et le chemin d’accès du dossier actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="0edde-179">The %THISDIR% and %THISDIRPATH% variables represent the name and path of the currently selected folder.</span></span> <span data-ttu-id="0edde-180">La variable% TEMPLATEDIR% représente le dossier dans lequel sont stockées les feuilles de style d’affichage Web.</span><span class="sxs-lookup"><span data-stu-id="0edde-180">The %TEMPLATEDIR% variable represents the folder where the Web view style sheets are stored.</span></span>

<span data-ttu-id="0edde-181">À l’instar de la plupart des modèles HTML, les fichiers. htt ont deux parties de base : un corps et un début.</span><span class="sxs-lookup"><span data-stu-id="0edde-181">Like most HTML templates, .htt files have two basic parts: a body and a head.</span></span> <span data-ttu-id="0edde-182">Le corps du modèle contrôle la disposition de base de l’affichage Web et charge les objets utilisés pour communiquer avec l’espace de noms et les informations d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0edde-182">The template body controls the basic layout of the Web view and loads the objects used to communicate with the namespace and display information.</span></span> <span data-ttu-id="0edde-183">L’en-tête contient des scripts et des fonctions qui effectuent des tâches telles que la gestion du redimensionnement et l’obtention d’informations à partir du dossier.</span><span class="sxs-lookup"><span data-stu-id="0edde-183">The head contains scripts and functions that do tasks such as handling resizing and obtaining information from the folder.</span></span> <span data-ttu-id="0edde-184">La plupart des modèles, y compris Generic. htt, incluent également une feuille de style.</span><span class="sxs-lookup"><span data-stu-id="0edde-184">Most templates, including Generic.htt, also include a style sheet.</span></span> <span data-ttu-id="0edde-185">En général, il est préférable d’inclure les informations de feuille de style dans votre modèle.</span><span class="sxs-lookup"><span data-stu-id="0edde-185">In general, it is better to include the style sheet information in your template.</span></span> <span data-ttu-id="0edde-186">Les feuilles de style distinctes peuvent ne pas fonctionner correctement lorsqu’une vue Web est utilisée avec des espaces de noms distants.</span><span class="sxs-lookup"><span data-stu-id="0edde-186">Separate style sheets may not work properly when a Web view is used with remote namespaces.</span></span>

### <a name="the-template-body"></a><span data-ttu-id="0edde-187">Corps du modèle</span><span class="sxs-lookup"><span data-stu-id="0edde-187">The Template Body</span></span>

<span data-ttu-id="0edde-188">Le corps du modèle spécifie ce qui sera présenté par une vue Web.</span><span class="sxs-lookup"><span data-stu-id="0edde-188">The body of the template specifies what will be presented by a Web view.</span></span> <span data-ttu-id="0edde-189">C’est également là que les objets utilisés pour afficher des informations et communiquer avec les dossiers d’espaces de noms sont chargés.</span><span class="sxs-lookup"><span data-stu-id="0edde-189">It is also where the objects used to display information and communicate with namespace folders are loaded.</span></span> <span data-ttu-id="0edde-190">La disposition définie par Generic. htt est semblable à celle indiquée dans l’illustration de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="0edde-190">The layout defined by Generic.htt is similar to that shown in the illustration in the previous section.</span></span> <span data-ttu-id="0edde-191">Il existe trois régions d’affichage : la bannière et le bloc d’informations sur le côté gauche de la vue, ainsi que la liste des fichiers à droite.</span><span class="sxs-lookup"><span data-stu-id="0edde-191">There are three display regions: the banner and information block on the left side of the view, and the file list on the right.</span></span>

<span data-ttu-id="0edde-192">Tous les identificateurs attribués aux régions sont utilisés par la feuille de style et DHTML.</span><span class="sxs-lookup"><span data-stu-id="0edde-192">The regions are all assigned identifiers to be used by the style sheet and DHTML.</span></span> <span data-ttu-id="0edde-193">Comme nous l’avons vu dans la section suivante, il existe deux bannières possibles, avec les identificateurs « Banner » et « MiniBanner ».</span><span class="sxs-lookup"><span data-stu-id="0edde-193">As discussed in the next section, there are two possible banners, with identifiers of "Banner" and "MiniBanner".</span></span> <span data-ttu-id="0edde-194">L’identificateur de la région du bloc d’informations est « info ».</span><span class="sxs-lookup"><span data-stu-id="0edde-194">The identifier of the information block's region is "Info".</span></span> <span data-ttu-id="0edde-195">L’identificateur de l’objet de liste de fichiers est « FileList ».</span><span class="sxs-lookup"><span data-stu-id="0edde-195">The file list object's identifier is "FileList".</span></span> <span data-ttu-id="0edde-196">Les détails de la [disposition](#controlling-the-web-view-layout) de la région sont gérés par la feuille de style et une fonction Microsoft JScript, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function), qui est décrite plus loin dans ce chapitre.</span><span class="sxs-lookup"><span data-stu-id="0edde-196">The details of the region's [layout](#controlling-the-web-view-layout) are handled by the style sheet and a Microsoft JScript function, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function), which is discussed later in the chapter.</span></span>

### <a name="the-banner-region"></a><span data-ttu-id="0edde-197">Zone de bannière</span><span class="sxs-lookup"><span data-stu-id="0edde-197">The Banner Region</span></span>

<span data-ttu-id="0edde-198">La bannière est située en haut de l’écran, dans le coin supérieur gauche de la vue Web.</span><span class="sxs-lookup"><span data-stu-id="0edde-198">The banner is located at the top of the display, in the upper-left corner of the Web view.</span></span> <span data-ttu-id="0edde-199">La bannière normale affiche le nom et l’icône du dossier dont le contenu est affiché dans la liste de fichiers à droite.</span><span class="sxs-lookup"><span data-stu-id="0edde-199">The normal banner displays the name and icon of the folder whose contents are displayed in the file list on the right.</span></span> <span data-ttu-id="0edde-200">Toutefois, si la fenêtre devient trop petite, il se peut qu’il n’y ait pas de place sous l’icône pour afficher des informations.</span><span class="sxs-lookup"><span data-stu-id="0edde-200">However, if the window becomes too short, there may be no room below the icon to display information.</span></span> <span data-ttu-id="0edde-201">Pour cette raison, Generic. htt définit également un minibanner qui affiche uniquement le nom du dossier.</span><span class="sxs-lookup"><span data-stu-id="0edde-201">For this reason, Generic.htt also defines a minibanner that only displays the folder name.</span></span> <span data-ttu-id="0edde-202">Les deux bannières sont initialement définies comme masquées.</span><span class="sxs-lookup"><span data-stu-id="0edde-202">Both banners are initially defined as hidden.</span></span> <span data-ttu-id="0edde-203">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) choisit celui à afficher et le définit sur « visible ».</span><span class="sxs-lookup"><span data-stu-id="0edde-203">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) chooses which one to display and sets it to "visible".</span></span>

<span data-ttu-id="0edde-204">La bannière normale pour Generic. htt est définie par :</span><span class="sxs-lookup"><span data-stu-id="0edde-204">The normal banner for Generic.htt is defined by:</span></span>


```
<div id="Banner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
    <p class=Title style="margin-left: 104px; margin-top: 16px">
        %THISDIRNAME% 
    </td></tr></table>
    <hr id="Rule" size=1px color=black style="position: absolute; top: 44px; left: 84px">
    <object id=Icon classid="clsid:e5df9d10-3b52-11d1-83e8-00a0c90dc849">
        <param name="scale" value=200>
    </object>
</div>
                    
```



<span data-ttu-id="0edde-205">La première partie de la section bannière affiche le titre avec une règle horizontale en dessous.</span><span class="sxs-lookup"><span data-stu-id="0edde-205">The first part of the banner section displays the title with a horizontal rule underneath it.</span></span> <span data-ttu-id="0edde-206">Les balises de table sont utilisées pour contrôler sa position.</span><span class="sxs-lookup"><span data-stu-id="0edde-206">Table tags are used to control its position.</span></span> <span data-ttu-id="0edde-207">L’attribut nowrap est défini pour la</span><span class="sxs-lookup"><span data-stu-id="0edde-207">The nowrap attribute is set for the</span></span> <TD> <span data-ttu-id="0edde-208">pour empêcher le retour automatique à la clé.</span><span class="sxs-lookup"><span data-stu-id="0edde-208">tag to prevent word wrapping.</span></span> <span data-ttu-id="0edde-209">Le système remplacera% THISDIRNAME% par le nom du dossier actif.</span><span class="sxs-lookup"><span data-stu-id="0edde-209">The system will replace %THISDIRNAME% with the name of the current folder.</span></span> <span data-ttu-id="0edde-210">Un objet **WebViewFolderIcon** , avec un identificateur « Icon » pour plus de simplicité, est ensuite chargé pour extraire et afficher l’icône du dossier.</span><span class="sxs-lookup"><span data-stu-id="0edde-210">A **WebViewFolderIcon** object, with an identifier of "Icon" for simplicity, is then loaded to extract and display the folder's icon.</span></span>

<span data-ttu-id="0edde-211">La section minibanner est similaire à la bannière normale.</span><span class="sxs-lookup"><span data-stu-id="0edde-211">The minibanner section is similar to the normal banner.</span></span> <span data-ttu-id="0edde-212">Le format du titre est placé légèrement plus haut et n’a pas de règle.</span><span class="sxs-lookup"><span data-stu-id="0edde-212">The format of the title is placed slightly higher and does not have a rule.</span></span> <span data-ttu-id="0edde-213">Étant donné qu’il n’y a pas d’icône, l’objet **WebViewFolderIcon** n’est pas chargé.</span><span class="sxs-lookup"><span data-stu-id="0edde-213">Because there is no icon, the **WebViewFolderIcon** object is not loaded.</span></span>


```
<div id="MiniBanner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
        <p class=Title style="margin-left: 16px; margin-top: 4px">
        %THISDIRNAME%
    </td></tr></table>
</div>
                    
```



### <a name="the-info-region"></a><span data-ttu-id="0edde-214">La région d’informations</span><span class="sxs-lookup"><span data-stu-id="0edde-214">The Info Region</span></span>

<span data-ttu-id="0edde-215">La partie de l’affichage Web sous la bannière est utilisée pour présenter des informations détaillées sur l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="0edde-215">The portion of the Web view below the banner is used to present detailed information about the selected item.</span></span> <span data-ttu-id="0edde-216">Si aucun élément n’est sélectionné, un message par défaut est affiché.</span><span class="sxs-lookup"><span data-stu-id="0edde-216">If no item is selected, a default message is shown.</span></span> <span data-ttu-id="0edde-217">Étant donné que Generic. htt affiche uniquement un bloc de texte unique, cette section est assez simple.</span><span class="sxs-lookup"><span data-stu-id="0edde-217">Because Generic.htt only displays a single block of text, this section is quite simple.</span></span>


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
</div>
                    
```



<span data-ttu-id="0edde-218">La majeure partie du travail de collecte des informations est traitée par un [script d’informations sur les dossiers](#retrieving-and-displaying-folder-information) qui est abordé plus loin dans ce chapitre.</span><span class="sxs-lookup"><span data-stu-id="0edde-218">Most of the work of collecting the information is handled by a [folder information script](#retrieving-and-displaying-folder-information) that is discussed later in the chapter.</span></span> <span data-ttu-id="0edde-219">Elle affiche les informations en affectant le texte à [TextBlock. innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="0edde-219">It displays the information by assigning the text to [TextBlock.innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span></span>

<span data-ttu-id="0edde-220">Vous pouvez facilement personnaliser l’affichage des informations en modifiant ces éléments ou en y incluant des éléments supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0edde-220">You can easily customize the information display by modifying these elements or including additional ones.</span></span> <span data-ttu-id="0edde-221">Tout ce que vous pouvez placer sur une page Web peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="0edde-221">Anything that you can put on a webpage can be used.</span></span> <span data-ttu-id="0edde-222">Par exemple, pour afficher un lien vers votre site Web, vous pouvez ajouter un élément d’ancrage après le bloc de texte dans Generic. htt.</span><span class="sxs-lookup"><span data-stu-id="0edde-222">For example, to display a link to your website, you can add an anchor element after the text block in Generic.htt.</span></span>


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
        <span>
        <p> Click on <a href="https://your.address"></a>
        </span>
</div>
                    
```



### <a name="the-filelist-region"></a><span data-ttu-id="0edde-223">Région FileList</span><span class="sxs-lookup"><span data-stu-id="0edde-223">The FileList Region</span></span>

<span data-ttu-id="0edde-224">Enfin, Generic. htt charge un objet [**WebViewFolderContents**](webviewfoldercontents.md) pour la région filelist.</span><span class="sxs-lookup"><span data-stu-id="0edde-224">Finally, Generic.htt loads a [**WebViewFolderContents**](webviewfoldercontents.md) object for the FileList region.</span></span> <span data-ttu-id="0edde-225">Étant donné que son identificateur est défini sur « FileList », il est appelé à l’objet FileList à partir de maintenant.</span><span class="sxs-lookup"><span data-stu-id="0edde-225">Because its identifier is set to "FileList", it will be referred to as the FileList object from now on.</span></span>


```
<object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>
                    
```



<span data-ttu-id="0edde-226">L’objet FileList se trouve dans la plupart des affichages Web et remplit plusieurs fonctions.</span><span class="sxs-lookup"><span data-stu-id="0edde-226">The FileList object is found in most Web views and serves several purposes.</span></span> <span data-ttu-id="0edde-227">FileList affiche la liste des éléments contenus dans le dossier sélectionné avec les mêmes options et apparence que la liste des fichiers dans le style classique.</span><span class="sxs-lookup"><span data-stu-id="0edde-227">FileList displays the list of items contained by the selected folder with the same options and appearance as the file list in Classic style.</span></span> <span data-ttu-id="0edde-228">Lorsqu’un élément est sélectionné, FileList notifie l’affichage Web en déclenchant un événement [SelectionChanged](#retrieving-and-displaying-folder-information) .</span><span class="sxs-lookup"><span data-stu-id="0edde-228">When an item is selected, FileList notifies the Web view by firing a [SelectionChanged](#retrieving-and-displaying-folder-information) event.</span></span> <span data-ttu-id="0edde-229">FileList expose également des méthodes et des propriétés qui peuvent être utilisées pour récupérer des informations sur des éléments individuels et contrôler la position et la taille de la zone d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0edde-229">FileList also exposes methods and properties that can be used to retrieve information about individual items and control the position and size of its display area.</span></span>

<span data-ttu-id="0edde-230">Bien que l’objet FileList soit très utile, il retourne uniquement des informations de système de fichiers standard, telles que la taille ou les attributs de fichier.</span><span class="sxs-lookup"><span data-stu-id="0edde-230">Although the FileList object is very useful, it only returns standard file system information, such as file size or attributes.</span></span> <span data-ttu-id="0edde-231">Pour récupérer d’autres types d’informations à partir d’un dossier shell, vous devez charger et gérer des objets supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0edde-231">To retrieve other kinds of information from a Shell folder, you will have to load and handle additional objects.</span></span> <span data-ttu-id="0edde-232">Tout objet pouvant être hébergé par une page Web peut être utilisé avec une vue Web.</span><span class="sxs-lookup"><span data-stu-id="0edde-232">Any object that can be hosted by a webpage can be used with a Web view.</span></span>

### <a name="the-template-head"></a><span data-ttu-id="0edde-233">L’en-tête de modèle</span><span class="sxs-lookup"><span data-stu-id="0edde-233">The Template Head</span></span>

<span data-ttu-id="0edde-234">Le début du modèle d’affichage Web contient les scripts et les fonctions qui effectuent la plupart du travail réel.</span><span class="sxs-lookup"><span data-stu-id="0edde-234">The head of the Web view template contains the scripts and functions that do most of the actual work.</span></span> <span data-ttu-id="0edde-235">Deux tâches essentielles doivent être gérées.</span><span class="sxs-lookup"><span data-stu-id="0edde-235">There are two essential tasks that need to be handled.</span></span> <span data-ttu-id="0edde-236">L’une est la mise en page de l’affichage Web qui doit être ajustée pour prendre en charge différentes zones d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0edde-236">One is the layout of the Web view display, which needs to be adjusted to accommodate different display regions.</span></span> <span data-ttu-id="0edde-237">L’autre récupère et affiche des informations à partir du dossier lorsqu’un élément est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="0edde-237">The other is retrieving and displaying information from the folder when an item is selected.</span></span> <span data-ttu-id="0edde-238">Comme pour les feuilles de style, il est préférable d’inclure tous les scripts et les fonctions dans le modèle au lieu de les référencer en tant que fichiers distincts.</span><span class="sxs-lookup"><span data-stu-id="0edde-238">As with style sheets, it is better to include all scripts and functions in the template instead of referencing them as separate files.</span></span>

### <a name="controlling-the-web-view-layout"></a><span data-ttu-id="0edde-239">Contrôle de la disposition de l’affichage Web</span><span class="sxs-lookup"><span data-stu-id="0edde-239">Controlling the Web View Layout</span></span>

<span data-ttu-id="0edde-240">La zone disponible pour une vue Web dépend de la taille de la fenêtre d’affichage Web et de la quantité d’informations qu’elle a prises en considération par la barre de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="0edde-240">The area available for a Web view depends on the size of the Web view window and how much of it is taken up by the Windows Explorer bar.</span></span> <span data-ttu-id="0edde-241">Cette zone est modifiée chaque fois que la fenêtre ou la barre de l’Explorateur Windows est redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="0edde-241">This area will change anytime the window or Windows Explorer bar is resized.</span></span> <span data-ttu-id="0edde-242">La disposition doit donc être mise en correspondance avec la zone disponible lorsqu’une vue Web est chargée et modifiée de manière appropriée lorsqu’elle est redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="0edde-242">So the layout needs to be matched to the available area when a Web view is loaded and change appropriately when it is resized.</span></span> <span data-ttu-id="0edde-243">Une grande partie de la mise en page est spécifiée dans la feuille de style.</span><span class="sxs-lookup"><span data-stu-id="0edde-243">Much of the layout is specified in the style sheet.</span></span> <span data-ttu-id="0edde-244">La région d’informations, par exemple, est définie pour occuper le plus à gauche de 30% de l’affichage Web.</span><span class="sxs-lookup"><span data-stu-id="0edde-244">The Info region, for example, is defined to occupy the leftmost 30 percent of the Web view.</span></span>


```
#Info       {position: absolute; top: 88px; width: 30%; background: window;
    overflow: auto}
                    
```



<span data-ttu-id="0edde-245">Lorsqu’une vue Web est redimensionnée, la largeur de la région d’informations est modifiée pour conserver ce pourcentage.</span><span class="sxs-lookup"><span data-stu-id="0edde-245">As a Web view is resized, the width of the Info region will change to maintain that percentage.</span></span> <span data-ttu-id="0edde-246">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) gère les problèmes de disposition qui ne peuvent pas être gérés par une feuille de style.</span><span class="sxs-lookup"><span data-stu-id="0edde-246">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) manages the layout issues that can't be handled by a style sheet.</span></span>

### <a name="loading-and-initializing-the-web-view"></a><span data-ttu-id="0edde-247">Chargement et initialisation de l’affichage Web</span><span class="sxs-lookup"><span data-stu-id="0edde-247">Loading and Initializing the Web View</span></span>

<span data-ttu-id="0edde-248">Lorsqu’un affichage Web est chargé, la disposition doit être ajustée pour correspondre à la zone d’affichage disponible.</span><span class="sxs-lookup"><span data-stu-id="0edde-248">When a Web view is loaded, the layout needs to be adjusted to fit the available display area.</span></span> <span data-ttu-id="0edde-249">Comme aucun élément n’a encore été sélectionné, les affichages Web affichent normalement des informations par défaut qui s’appliquent à l’ensemble du dossier.</span><span class="sxs-lookup"><span data-stu-id="0edde-249">Because no item has been selected yet, Web views normally display some default information that applies to the whole folder.</span></span> <span data-ttu-id="0edde-250">Pour gérer l’initialisation, le</span><span class="sxs-lookup"><span data-stu-id="0edde-250">To handle initialization, the</span></span> <BODY> <span data-ttu-id="0edde-251">tag pour Generic. htt détecte l’événement [OnLoad](/previous-versions//ms531409(v=vs.85)) et appelle la fonction **init** .</span><span class="sxs-lookup"><span data-stu-id="0edde-251">tag for Generic.htt detects the [onload](/previous-versions//ms531409(v=vs.85)) event and calls the **Init** function.</span></span>


```
<body scroll=no onload="Init">
                    
```



<span data-ttu-id="0edde-252">**Init** est une fonction JScript simple.</span><span class="sxs-lookup"><span data-stu-id="0edde-252">**Init** is a simple JScript function.</span></span>


```
function Init() {
    window.onresize = FixSize;
    FixSize();
    TextBlock.innerHTML = L_Intro_Text;
}
                    
```



<span data-ttu-id="0edde-253">**Init** lie [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) à l’événement [Window. OnResize](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) afin qu’il soit appelé chaque fois que la zone d’affichage Web est modifiée.</span><span class="sxs-lookup"><span data-stu-id="0edde-253">**Init** binds [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) to the [window.onresize](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) event so that it will be called whenever the Web view display area changes.</span></span> <span data-ttu-id="0edde-254">Il exécute ensuite FixSize pour définir la disposition initiale et assigne le \_ \_ texte d’introduction L à la région d’informations.</span><span class="sxs-lookup"><span data-stu-id="0edde-254">It then runs FixSize to set the initial layout and assigns L\_Intro\_Text to the Info region.</span></span> <span data-ttu-id="0edde-255">L \_ Intro \_ Text est un bloc de texte d’introduction qui est défini dans la section de la feuille de style.</span><span class="sxs-lookup"><span data-stu-id="0edde-255">L\_Intro\_Text is a block of introductory text that is defined in the style sheet section.</span></span>


```
var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br>
<br>To get information about any of them, click the items icon.<br><br>";
                    
```



### <a name="adjusting-the-layout-by-using-the-fixsize-function"></a><span data-ttu-id="0edde-256">Ajustement de la disposition à l’aide de la fonction FixSize</span><span class="sxs-lookup"><span data-stu-id="0edde-256">Adjusting the Layout by using the FixSize function</span></span>

<span data-ttu-id="0edde-257">La fonction [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) est utilisée pour spécifier plusieurs aspects de la disposition qui ne peuvent pas être gérés par la feuille de style.</span><span class="sxs-lookup"><span data-stu-id="0edde-257">The [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) function is used to specify several aspects of the layout that can't be handled by the style sheet.</span></span>

<span data-ttu-id="0edde-258">Il existe deux bannières possibles qui peuvent être utilisées, en fonction de la hauteur de l’affichage Web.</span><span class="sxs-lookup"><span data-stu-id="0edde-258">There are two possible banners that can be used, depending on the height of the Web view.</span></span>


```
if (200 > document.body.clientHeight) {
    //A short window. Use the minibanner.
    document.all.Banner.style.visibility = "hidden";
    document.all.MiniBanner.style.visibility = "visible";
    document.all.FileList.style.top = 32;
    document.all.Info.style.top = 32;
}
else {
    //A normal window. Use the normal banner.
    document.all.Banner.style.visibility = "visible";
    document.all.MiniBanner.style.visibility = "hidden";
    document.all.FileList.style.top = (document.all.Banner.offsetHeight - 32) + "px";
    document.all.Info.style.top = (document.all.Banner.offsetHeight) + "px";
    document.all.Rule.style.width = (document.body.clientWidth > 84 ?                                    document.body.clientWidth - 84 : 0) + "px";      
}
                    
```



<span data-ttu-id="0edde-259">Generic. htt utilise une hauteur de 200 pixels comme ligne de séparation entre normal et minibanners.</span><span class="sxs-lookup"><span data-stu-id="0edde-259">Generic.htt uses a height of 200 pixels as the dividing line between normal and minibanners.</span></span> <span data-ttu-id="0edde-260">Il définit le style de la bannière sélectionnée sur visible et l’autre sur masqué.</span><span class="sxs-lookup"><span data-stu-id="0edde-260">It sets the style of the selected banner to visible and the other to hidden.</span></span> <span data-ttu-id="0edde-261">Il définit également plusieurs propriétés de disposition pour les régions info et FileList afin qu’elles s’adaptent correctement à la bannière sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="0edde-261">It also sets several layout properties for the Info and FileList regions so that they fit properly with the selected banner.</span></span>

<span data-ttu-id="0edde-262">Si un affichage Web devient trop étroit, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) utilise la largeur complète de la zone d’affichage pour l’affichage filelist.</span><span class="sxs-lookup"><span data-stu-id="0edde-262">If a Web view becomes too narrow, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) uses the full width of the display area for the FileList display.</span></span>


```
if (400 > document.body.clientWidth) {
    //A narrow window. Hide the Info region, and expand the file list region.
    document.all.Info.style.visibility = "hidden";
    document.all.FileList.style.pixelLeft = 0;
    document.all.FileList.style.pixelTop = document.all.Info.style.pixelTop;
}

else {
    //Normal width.
    document.all.Info.style.visibility = "visible";
    document.all.FileList.style.pixelLeft = document.all.Info.style.pixelWidth;
}
                    
```



<span data-ttu-id="0edde-263">Generic. htt utilise 400 pixels comme ligne de séparation entre les affichages étroits et larges.</span><span class="sxs-lookup"><span data-stu-id="0edde-263">Generic.htt uses 400 pixels as the dividing line between narrow and wide displays.</span></span> <span data-ttu-id="0edde-264">Si l’affichage Web est trop étroit, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) masque la région d’informations et modifie la propriété filelist [pixelLeft](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) pour qu’elle remplisse toute la région sous la bannière.</span><span class="sxs-lookup"><span data-stu-id="0edde-264">If the Web view is too narrow, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) hides the Info region and modifies the FileList [pixelLeft](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) property so that it fills the entire region below the banner.</span></span>

<span data-ttu-id="0edde-265">Les dernières lignes de [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) ajustent plusieurs propriétés de disposition en fonction des résultats du code précédent.</span><span class="sxs-lookup"><span data-stu-id="0edde-265">The final few lines of [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) adjust several layout properties based on the results of the preceding code.</span></span> <span data-ttu-id="0edde-266">La largeur de la région FileList est ajustée afin de remplir exactement la partie de l’affichage Web qui n’est pas occupée par la région d’informations.</span><span class="sxs-lookup"><span data-stu-id="0edde-266">The width of the FileList region is adjusted so that it exactly fills the portion of the Web view not occupied by the Info region.</span></span> <span data-ttu-id="0edde-267">La hauteur de la région d’informations est dimensionnée pour s’ajuster à la bannière et au bas de la vue Web.</span><span class="sxs-lookup"><span data-stu-id="0edde-267">The height of the Info region is sized to fit between the banner and the bottom of the Web view.</span></span>


```
document.all.FileList.style.pixelWidth = document.body.clientWidth
    document.all.FileList.style.pixelLeft;
document.all.FileList.style.pixelHeight = document.body.clientHeight
    document.all.FileList.style.pixelTop;
document.all.Info.style.pixelHeight = document.body.clientHeight
    document.all.Info.style.pixelTop;
                    
```



### <a name="retrieving-and-displaying-folder-information"></a><span data-ttu-id="0edde-268">Récupération et affichage des informations sur les dossiers</span><span class="sxs-lookup"><span data-stu-id="0edde-268">Retrieving and Displaying Folder Information</span></span>

<span data-ttu-id="0edde-269">Lorsqu’un utilisateur sélectionne un élément, l’objet FileList déclenche un événement [SelectionChanged](#retrieving-and-displaying-folder-information) .</span><span class="sxs-lookup"><span data-stu-id="0edde-269">When a user selects an item, the FileList object fires a [SelectionChanged](#retrieving-and-displaying-folder-information) event.</span></span> <span data-ttu-id="0edde-270">Cet événement est géré par un script JScript.</span><span class="sxs-lookup"><span data-stu-id="0edde-270">This event is handled by a JScript script.</span></span> <span data-ttu-id="0edde-271">Par souci de simplicité, le script trouvé dans Generic. htt suppose qu’un seul élément peut être sélectionné à la fois.</span><span class="sxs-lookup"><span data-stu-id="0edde-271">For simplicity, the script found in Generic.htt assumes that only one item can be selected at a time.</span></span>


```
<script language="JavaScript" for="FileList" event="SelectionChanged">
    // Updates the TextBlock region when an item is selected.
    var data;
    var text;

    // Name
    text = "<b>" + FileList.FocusedItem.Name + "</b>";

    // Comment
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 3);
    if (data)
        text += "<br>" + data;

    // Documents
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 1);
    if (data)
        text += "<br><br>" + FileList.Folder.GetDetailsOf(null, 1) + ": " + data;

    // Status
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 2);
    if (data)
        text += "<br><br><b><font color=red>" + data + "</font></b>";

    // Tip 
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, -1);
    if (data != "" && data != FileList.FocusedItem.Name)
        text += "<br><br>" + data;

    TextBlock.innerHTML = text;
</script>
                    
```



<span data-ttu-id="0edde-272">Le script utilise deux propriétés FileList, [**filelist. FocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)et [**filelist. Folder**](/windows/desktop/shell/shellfolderview-folder) pour obtenir des informations sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="0edde-272">The script uses two FileList properties, [**FileList.FocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)and [**FileList.Folder**](/windows/desktop/shell/shellfolderview-folder) to obtain information about the item.</span></span> <span data-ttu-id="0edde-273">**Filelist. FocusedItem** identifie l’élément sélectionné, avec le nom de l’élément donné par **filelist.FocusedItem.Name**.</span><span class="sxs-lookup"><span data-stu-id="0edde-273">**FileList.FocusedItem** identifies the selected item, with the item's name given by **FileList.FocusedItem.Name**.</span></span> <span data-ttu-id="0edde-274">**Filelist. Folder** est en fait un pointeur vers un objet [**Folder**](../shell/folder.md) .</span><span class="sxs-lookup"><span data-stu-id="0edde-274">**FileList.Folder** is actually a pointer to a [**Folder**](../shell/folder.md) object.</span></span> <span data-ttu-id="0edde-275">La méthode [**GetDetailsOf**](/windows/desktop/shell/folder-getdetailsof) de l’objet Folder est utilisée pour récupérer les informations restantes sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="0edde-275">The Folder object's [**GetDetailsOf**](/windows/desktop/shell/folder-getdetailsof) method is used to retrieve the remaining information about the item.</span></span>

<span data-ttu-id="0edde-276">Toutes les informations sont concaténées dans une chaîne de texte unique, séparées par</span><span class="sxs-lookup"><span data-stu-id="0edde-276">All the information is concatenated into a single text string, separated by</span></span> <BR> <span data-ttu-id="0edde-277">balises pour la lisibilité.</span><span class="sxs-lookup"><span data-stu-id="0edde-277">tags for readability.</span></span> <span data-ttu-id="0edde-278">Le texte est ensuite affiché en l’affectant à [TextBlock. innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="0edde-278">The text is then displayed by assigning it to [TextBlock.innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span></span>

## <a name="summary"></a><span data-ttu-id="0edde-279">Résumé</span><span class="sxs-lookup"><span data-stu-id="0edde-279">Summary</span></span>

<span data-ttu-id="0edde-280">Ce chapitre décrit certaines des techniques que vous pouvez utiliser pour personnaliser la façon dont l’Explorateur Windows affiche des informations sur les dossiers Shell.</span><span class="sxs-lookup"><span data-stu-id="0edde-280">This chapter outlines some of the techniques you can use to customize the way the Windows Explorer displays information about Shell folders.</span></span> <span data-ttu-id="0edde-281">La création d’un fichier Desktop.ini vous permet d’effectuer une simple personnalisation, comme l’affichage d’une icône personnalisée à la place de l’icône de dossier standard.</span><span class="sxs-lookup"><span data-stu-id="0edde-281">Creating a Desktop.ini file allows you to do some simple customization, such as displaying a custom icon in place of the standard folder icon.</span></span> <span data-ttu-id="0edde-282">Lorsqu’un dossier s’affiche dans une vue Web, sa disposition et son affichage sont contrôlés par un modèle HTML qui détermine quelles informations sont affichées et comment.</span><span class="sxs-lookup"><span data-stu-id="0edde-282">When a folder appears in a Web view, its layout and display are controlled by an HTML-based template that determines what information is displayed and how.</span></span> <span data-ttu-id="0edde-283">Vous pouvez exercer un haut degré de contrôle sur l’affichage Web d’un dossier à l’aide de techniques de script, HTML et DHTML standard pour créer un modèle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0edde-283">You can exercise a high degree of control over a folder's Web view by using standard HTML, DHTML, and scripting techniques to create a custom template.</span></span>

 

 