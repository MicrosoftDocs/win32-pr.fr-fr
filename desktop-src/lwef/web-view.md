---
title: Personnalisation de l’affichage Web d’un dossier
description: une vue Web est un moyen puissant et flexible d’utiliser l’explorateur de Windows pour afficher des informations sur le contenu d’un dossier de Shell.
ms.assetid: a894df21-bcc6-4760-b7d7-9bf95a0dba7f
keywords:
- Affichages Web
- Style classique
- Style Web
- bannières
- Zone FileList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ebe106bdada4da55eef8891a3c93ee82aba3cc4da9194e1fcd4c7e71bcd4e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745682"
---
# <a name="customizing-a-folders-web-view"></a>Personnalisation de l’affichage Web d’un dossier

\[cette fonctionnalité est prise en charge uniquement sous Windows XP ou version antérieure. \]

une vue Web est un moyen puissant et flexible d’utiliser l’explorateur de Windows pour afficher des informations sur le contenu d’un dossier de Shell.

-   [Introduction](#introduction)
-   [Utilisation du modèle d’affichage Web](#using-the-web-view-template)
    -   [Corps du modèle](#the-template-body)
    -   [L’en-tête de modèle](#the-template-head)
-   [Résumé](#summary)

## <a name="introduction"></a>Introduction

Windows offre aux utilisateurs deux méthodes principales pour afficher et parcourir l’espace de noms Shell. les plus familières de ceux-ci, le style classique, sont similaires au gestionnaire de fichiers Windows familier. Le volet droit répertorie le contenu du dossier actuellement sélectionné dans l’un des cinq formats suivants : grande icône, petite icône, liste, détails et miniature. la principale différence par rapport au gestionnaire de fichiers Windows est le volet gauche, qui ressemble beaucoup à la barre d’exploration d’Windows Internet Explorer. Il peut être redimensionné ou supprimé, et il peut afficher plusieurs volets en plus de l’arborescence de système de fichiers familière, telle qu’un volet de recherche.

> [!Note]  
> les informations contenues dans ce document ne s’appliquent pas à Windows XP, les techniques abordées s’appliquent uniquement aux versions antérieures de Windows.

 

L’illustration suivante montre le dossier Imprimantes dans le style classique.

![style classique du dossier Imprimantes.](images/webview1.png)

Le style classique fonctionne raisonnablement bien pour les dossiers et fichiers du système de fichiers normal. toutefois, avec l’introduction de Windows 95, le système de fichiers a évolué vers l’espace de noms. L’espace de noms permet de créer des *dossiers virtuels*, tels que des imprimantes ou un voisinage réseau, qui peuvent représenter des types d’informations très différents de ceux d’un dossier de système de fichiers normal.

Le style Web, également appelé vue Web, offre un moyen plus flexible et plus puissant de présenter des informations que le style classique. Dans une vue Web, l’utilisateur affiche et parcourt l’espace de noms à l’aide d’Internet Explorer. La disposition de base d’une vue Web est similaire au style classique. Le volet d’exploration est inchangé. Toutefois, la région occupée par la liste de fichiers devient une zone d’affichage à usage général qui est effectivement une page Web. Un affichage Web est toujours utilisé pour afficher des informations sur le contenu d’un dossier, mais il existe peu de contraintes sur les informations qui sont affichées, ou comment. Chaque dossier peut avoir sa propre vue Web, personnalisée pour l’adapter à ses fonctionnalités particulières.

L’illustration suivante montre une vue Web du dossier Imprimantes (indiqué précédemment dans le style classique).

![vue Web par défaut du dossier Imprimantes.](images/webview2.png)

À l’instar des pages Web conventionnelles, les vues Web sont contrôlées par un modèle HTML. La création d’un modèle d’affichage Web est quasiment identique à la création d’une page Web et offre le même degré de flexibilité dans le contenu et la mise en page des informations. Les modèles d’affichage Web peuvent utiliser le DHTML (Dynamic HTML) et les scripts pour répondre aux événements, comme un utilisateur qui clique sur un élément. Ils peuvent également héberger des objets qui leur permettent d’obtenir et d’afficher des informations à partir du dossier ou de son contenu.

l’utilisateur peut choisir un affichage Web en démarrant Windows Explorer, en cliquant sur **Options des dossiers** dans le menu **affichage** , puis en sélectionnant cette option : **activer le contenu Web dans les dossiers**. Toutefois, l’utilisateur peut également démarrer Internet Explorer et pointer sur le navigateur dans le système de fichiers en cliquant sur le menu **affichage** , en pointant sur **barre d’exploration**, puis en cliquant sur **dossiers**. dans une vue Web, il n’y a pratiquement aucune différence entre Internet explorer et l’explorateur de Windows.

Sur le côté gauche du volet droit, la vue Web imprimantes affiche une bannière avec le nom et l’icône du dossier, suivis d’un bloc d’informations sur le dossier. La liste de fichiers habituelle occupe le côté droit de la page.

Lorsqu’un utilisateur clique sur un élément, des informations détaillées sur l’élément s’affichent dans le bloc d’informations. L’affichage Web imprimantes affiche en fait pratiquement les mêmes informations que celles disponibles dans le style classique, mais il le fait dans un format plus utilisable. Toutefois, une vue Web n’est pas simplement une autre façon d’afficher des informations de style classiques. Par exemple, un lien vers un site Web utile peut être affiché sous le bloc d’informations, une fonctionnalité qui n’est pas disponible dans le style classique. Si l’utilisateur clique sur le lien, le site s’affiche.

Le mode Web imprimantes présenté dans l’illustration précédente est semblable au style classique, car le modèle d’affichage Web sous-jacent (fichier. htt) a été écrit de cette façon. La liste de fichiers, par exemple, n’est pas générée directement par le modèle d’affichage Web. Elle est créée et affichée par un objet [**WebViewFolderContents**](webviewfoldercontents.md) hébergé par le modèle d’affichage Web. Les méthodes et propriétés de l’objet permettent à l’affichage Web de contrôler sa disposition et d’obtenir des informations sur des éléments particuliers. Le contenu et la mise en page de la bannière et du bloc d’informations sont spécifiés dans le modèle d’affichage Web.

Étant donné qu’une vue Web prend en charge le langage DHTML, le modèle peut également être utilisé pour gérer l’interaction de l’utilisateur. Par exemple, lorsqu’un utilisateur clique sur l’une des icônes d’imprimante, l’objet **WebViewFolderIcon** déclenche un événement [**SelectionChanged**](/windows/desktop/shell/application-support-bumper) . Le modèle utilise un gestionnaire d’événements DHTML écrit dans un script pour récupérer les informations demandées et les afficher dans le bloc d’informations.

Cet exemple simple pour le dossier Printers n’est pas le seul moyen d’utiliser une vue Web. En écrivant votre propre modèle et, si nécessaire, des objets, vous pouvez utiliser une vue Web pour afficher des informations et interagir avec l’utilisateur de la manière la plus efficace. Notez que, à l’heure actuelle, les modèles d’affichage Web affichent uniquement les dossiers virtuels définis par le système. Bien que les développeurs puissent créer un dossier virtuel en implémentant une extension d’espace de noms, ils doivent utiliser les techniques décrites dans [extensions d’espace de noms](/windows/desktop/shell/nse-works) pour les afficher.

## <a name="using-the-web-view-template"></a>Utilisation du modèle d’affichage Web

La façon dont les données sont affichées dans une vue Web peut être personnalisée de façon limitée en modifiant le fichier Desktop.ini d’un dossier. Pour plus d’informations, consultez [Personnalisation des dossiers avec Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) . Un moyen bien plus flexible et puissant de personnaliser une vue Web consiste à créer un modèle d’affichage Web personnalisé.

Le modèle d’affichage Web contrôle ce qui est affiché dans une vue Web et comment. Il utilise des techniques de script, DHTML et HTML standard pour obtenir et afficher des informations et interagir avec l’utilisateur. Cette section explique comment créer une vue Web en examinant un modèle simple, générique. htt.


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



Un moyen simple de créer votre propre modèle d’affichage Web consiste à utiliser Generic. htt et à le modifier. Étant donné qu’il est plutôt limité, vous devez également consulter d’autres exemples plus complexes pour obtenir des idées supplémentaires. Vous pouvez les trouver en recherchant dans votre système l’extension. htt utilisée par tous les modèles d’affichage Web. si vous souhaitez créer un modèle personnalisé pour un dossier, commencez par le modèle folder. htt par défaut, qui est généralement stocké dans c : \\ winnt \\ web ou c : \\ Windows \\ web. notez que ces fichiers sont définis comme étant masqués. par conséquent, vous devrez peut-être modifier vos paramètres de l’explorateur d’Windows pour les afficher. Une fois qu’un fichier. htt est créé, il doit être marqué comme étant en lecture seule et masqué.

Les modèles d’affichage Web utilisent l’extension. htt, car ils diffèrent légèrement des documents .htm conventionnels. La principale différence réside dans le fait que les fichiers. htt remplacent les variables spéciales par les valeurs d’espace de noms actuelles. Les variables% THISDIR% et% THISDIRPATH% représentent le nom et le chemin d’accès du dossier actuellement sélectionné. La variable% TEMPLATEDIR% représente le dossier dans lequel sont stockées les feuilles de style d’affichage Web.

À l’instar de la plupart des modèles HTML, les fichiers. htt ont deux parties de base : un corps et un début. Le corps du modèle contrôle la disposition de base de l’affichage Web et charge les objets utilisés pour communiquer avec l’espace de noms et les informations d’affichage. L’en-tête contient des scripts et des fonctions qui effectuent des tâches telles que la gestion du redimensionnement et l’obtention d’informations à partir du dossier. La plupart des modèles, y compris Generic. htt, incluent également une feuille de style. En général, il est préférable d’inclure les informations de feuille de style dans votre modèle. Les feuilles de style distinctes peuvent ne pas fonctionner correctement lorsqu’une vue Web est utilisée avec des espaces de noms distants.

### <a name="the-template-body"></a>Corps du modèle

Le corps du modèle spécifie ce qui sera présenté par une vue Web. C’est également là que les objets utilisés pour afficher des informations et communiquer avec les dossiers d’espaces de noms sont chargés. La disposition définie par Generic. htt est semblable à celle indiquée dans l’illustration de la section précédente. Il existe trois régions d’affichage : la bannière et le bloc d’informations sur le côté gauche de la vue, ainsi que la liste des fichiers à droite.

Tous les identificateurs attribués aux régions sont utilisés par la feuille de style et DHTML. Comme nous l’avons vu dans la section suivante, il existe deux bannières possibles, avec les identificateurs « Banner » et « MiniBanner ». L’identificateur de la région du bloc d’informations est « info ». L’identificateur de l’objet de liste de fichiers est « FileList ». les détails de la [disposition](#controlling-the-web-view-layout) de la région sont gérés par la feuille de style et une fonction de JScript Microsoft, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function), qui est décrite plus loin dans ce chapitre.

### <a name="the-banner-region"></a>Zone de bannière

La bannière est située en haut de l’écran, dans le coin supérieur gauche de la vue Web. La bannière normale affiche le nom et l’icône du dossier dont le contenu est affiché dans la liste de fichiers à droite. Toutefois, si la fenêtre devient trop petite, il se peut qu’il n’y ait pas de place sous l’icône pour afficher des informations. Pour cette raison, Generic. htt définit également un minibanner qui affiche uniquement le nom du dossier. Les deux bannières sont initialement définies comme masquées. [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) choisit celui à afficher et le définit sur « visible ».

La bannière normale pour Generic. htt est définie par :


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



La première partie de la section bannière affiche le titre avec une règle horizontale en dessous. Les balises de table sont utilisées pour contrôler sa position. L’attribut nowrap est défini pour la <TD> pour empêcher le retour automatique à la clé. Le système remplacera% THISDIRNAME% par le nom du dossier actif. Un objet **WebViewFolderIcon** , avec un identificateur « Icon » pour plus de simplicité, est ensuite chargé pour extraire et afficher l’icône du dossier.

La section minibanner est similaire à la bannière normale. Le format du titre est placé légèrement plus haut et n’a pas de règle. Étant donné qu’il n’y a pas d’icône, l’objet **WebViewFolderIcon** n’est pas chargé.


```
<div id="MiniBanner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
        <p class=Title style="margin-left: 16px; margin-top: 4px">
        %THISDIRNAME%
    </td></tr></table>
</div>
                    
```



### <a name="the-info-region"></a>La région d’informations

La partie de l’affichage Web sous la bannière est utilisée pour présenter des informations détaillées sur l’élément sélectionné. Si aucun élément n’est sélectionné, un message par défaut est affiché. Étant donné que Generic. htt affiche uniquement un bloc de texte unique, cette section est assez simple.


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
</div>
                    
```



La majeure partie du travail de collecte des informations est traitée par un [script d’informations sur les dossiers](#retrieving-and-displaying-folder-information) qui est abordé plus loin dans ce chapitre. Elle affiche les informations en affectant le texte à [TextBlock. innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).

Vous pouvez facilement personnaliser l’affichage des informations en modifiant ces éléments ou en y incluant des éléments supplémentaires. Tout ce que vous pouvez placer sur une page Web peut être utilisé. Par exemple, pour afficher un lien vers votre site Web, vous pouvez ajouter un élément d’ancrage après le bloc de texte dans Generic. htt.


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



### <a name="the-filelist-region"></a>Région FileList

Enfin, Generic. htt charge un objet [**WebViewFolderContents**](webviewfoldercontents.md) pour la région filelist. Étant donné que son identificateur est défini sur « FileList », il est appelé à l’objet FileList à partir de maintenant.


```
<object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>
                    
```



L’objet FileList se trouve dans la plupart des affichages Web et remplit plusieurs fonctions. FileList affiche la liste des éléments contenus dans le dossier sélectionné avec les mêmes options et apparence que la liste des fichiers dans le style classique. Lorsqu’un élément est sélectionné, FileList notifie l’affichage Web en déclenchant un événement [SelectionChanged](#retrieving-and-displaying-folder-information) . FileList expose également des méthodes et des propriétés qui peuvent être utilisées pour récupérer des informations sur des éléments individuels et contrôler la position et la taille de la zone d’affichage.

Bien que l’objet FileList soit très utile, il retourne uniquement des informations de système de fichiers standard, telles que la taille ou les attributs de fichier. Pour récupérer d’autres types d’informations à partir d’un dossier shell, vous devez charger et gérer des objets supplémentaires. Tout objet pouvant être hébergé par une page Web peut être utilisé avec une vue Web.

### <a name="the-template-head"></a>L’en-tête de modèle

Le début du modèle d’affichage Web contient les scripts et les fonctions qui effectuent la plupart du travail réel. Deux tâches essentielles doivent être gérées. L’une est la mise en page de l’affichage Web qui doit être ajustée pour prendre en charge différentes zones d’affichage. L’autre récupère et affiche des informations à partir du dossier lorsqu’un élément est sélectionné. Comme pour les feuilles de style, il est préférable d’inclure tous les scripts et les fonctions dans le modèle au lieu de les référencer en tant que fichiers distincts.

### <a name="controlling-the-web-view-layout"></a>Contrôle de la disposition de l’affichage Web

la zone disponible pour une vue web dépend de la taille de la fenêtre d’affichage web et de la quantité d’informations qu’elle a prises en considération par le Windows volet d’exploration. cette zone est modifiée chaque fois que la fenêtre ou la barre d’exploration Windows est redimensionnée. La disposition doit donc être mise en correspondance avec la zone disponible lorsqu’une vue Web est chargée et modifiée de manière appropriée lorsqu’elle est redimensionnée. Une grande partie de la mise en page est spécifiée dans la feuille de style. La région d’informations, par exemple, est définie pour occuper le plus à gauche de 30% de l’affichage Web.


```
#Info       {position: absolute; top: 88px; width: 30%; background: window;
    overflow: auto}
                    
```



Lorsqu’une vue Web est redimensionnée, la largeur de la région d’informations est modifiée pour conserver ce pourcentage. [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) gère les problèmes de disposition qui ne peuvent pas être gérés par une feuille de style.

### <a name="loading-and-initializing-the-web-view"></a>Chargement et initialisation de l’affichage Web

Lorsqu’un affichage Web est chargé, la disposition doit être ajustée pour correspondre à la zone d’affichage disponible. Comme aucun élément n’a encore été sélectionné, les affichages Web affichent normalement des informations par défaut qui s’appliquent à l’ensemble du dossier. Pour gérer l’initialisation, le <BODY> tag pour Generic. htt détecte l’événement [OnLoad](/previous-versions//ms531409(v=vs.85)) et appelle la fonction **init** .


```
<body scroll=no onload="Init">
                    
```



**Init** est une fonction de JScript simple.


```
function Init() {
    window.onresize = FixSize;
    FixSize();
    TextBlock.innerHTML = L_Intro_Text;
}
                    
```



**Init** lie [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) à l’événement [Window. OnResize](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) afin qu’il soit appelé chaque fois que la zone d’affichage Web est modifiée. Il exécute ensuite FixSize pour définir la disposition initiale et assigne le \_ \_ texte d’introduction L à la région d’informations. L \_ Intro \_ Text est un bloc de texte d’introduction qui est défini dans la section de la feuille de style.


```
var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br>
<br>To get information about any of them, click the items icon.<br><br>";
                    
```



### <a name="adjusting-the-layout-by-using-the-fixsize-function"></a>Ajustement de la disposition à l’aide de la fonction FixSize

La fonction [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) est utilisée pour spécifier plusieurs aspects de la disposition qui ne peuvent pas être gérés par la feuille de style.

Il existe deux bannières possibles qui peuvent être utilisées, en fonction de la hauteur de l’affichage Web.


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



Generic. htt utilise une hauteur de 200 pixels comme ligne de séparation entre normal et minibanners. Il définit le style de la bannière sélectionnée sur visible et l’autre sur masqué. Il définit également plusieurs propriétés de disposition pour les régions info et FileList afin qu’elles s’adaptent correctement à la bannière sélectionnée.

Si un affichage Web devient trop étroit, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) utilise la largeur complète de la zone d’affichage pour l’affichage filelist.


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



Generic. htt utilise 400 pixels comme ligne de séparation entre les affichages étroits et larges. Si l’affichage Web est trop étroit, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) masque la région d’informations et modifie la propriété filelist [pixelLeft](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) pour qu’elle remplisse toute la région sous la bannière.

Les dernières lignes de [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) ajustent plusieurs propriétés de disposition en fonction des résultats du code précédent. La largeur de la région FileList est ajustée afin de remplir exactement la partie de l’affichage Web qui n’est pas occupée par la région d’informations. La hauteur de la région d’informations est dimensionnée pour s’ajuster à la bannière et au bas de la vue Web.


```
document.all.FileList.style.pixelWidth = document.body.clientWidth
    document.all.FileList.style.pixelLeft;
document.all.FileList.style.pixelHeight = document.body.clientHeight
    document.all.FileList.style.pixelTop;
document.all.Info.style.pixelHeight = document.body.clientHeight
    document.all.Info.style.pixelTop;
                    
```



### <a name="retrieving-and-displaying-folder-information"></a>Récupération et affichage des informations sur les dossiers

Lorsqu’un utilisateur sélectionne un élément, l’objet FileList déclenche un événement [SelectionChanged](#retrieving-and-displaying-folder-information) . Cet événement est géré par un script de JScript. Par souci de simplicité, le script trouvé dans Generic. htt suppose qu’un seul élément peut être sélectionné à la fois.


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



Le script utilise deux propriétés FileList, [**filelist. FocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)et [**filelist. Folder**](/windows/desktop/shell/shellfolderview-folder) pour obtenir des informations sur l’élément. **Filelist. FocusedItem** identifie l’élément sélectionné, avec le nom de l’élément donné par **filelist.FocusedItem.Name**. **Filelist. Folder** est en fait un pointeur vers un objet [**Folder**](../shell/folder.md) . La méthode [**GetDetailsOf**](/windows/desktop/shell/folder-getdetailsof) de l’objet Folder est utilisée pour récupérer les informations restantes sur l’élément.

Toutes les informations sont concaténées dans une chaîne de texte unique, séparées par <BR> balises pour la lisibilité. Le texte est ensuite affiché en l’affectant à [TextBlock. innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).

## <a name="summary"></a>Résumé

ce chapitre décrit certaines des techniques que vous pouvez utiliser pour personnaliser la façon dont l’explorateur de Windows affiche des informations sur les dossiers Shell. La création d’un fichier Desktop.ini vous permet d’effectuer une simple personnalisation, comme l’affichage d’une icône personnalisée à la place de l’icône de dossier standard. Lorsqu’un dossier s’affiche dans une vue Web, sa disposition et son affichage sont contrôlés par un modèle HTML qui détermine quelles informations sont affichées et comment. Vous pouvez exercer un haut degré de contrôle sur l’affichage Web d’un dossier à l’aide de techniques de script, HTML et DHTML standard pour créer un modèle personnalisé.

 

 