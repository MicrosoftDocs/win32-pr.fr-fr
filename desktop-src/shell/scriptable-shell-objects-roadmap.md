---
description: l’interpréteur de commandes Windows fournit un ensemble puissant d’objets automation qui vous permettent de programmer l’interpréteur de commandes avec microsoft Visual Basic et des langages de script tels que microsoft JScript (compatible avec la spécification du langage ECMA 262) et microsoft Visual Basic scripting Edition (VBScript). Vous pouvez utiliser ces objets pour accéder à la plupart des fonctionnalités et boîtes de dialogue de l’interpréteur de commandes. Par exemple, vous pouvez accéder au système de fichiers, lancer des programmes et modifier les paramètres système.
title: Objets Shell scriptable
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09455fad-a769-42ef-83ba-b745ac819bf3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e8685b44d00d3f48e8de2a567218ef08c1cb5070
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196447"
---
# <a name="scriptable-shell-objects"></a>Objets Shell scriptable

l’interpréteur de commandes Windows fournit un ensemble puissant d’objets automation qui vous permettent de programmer l’interpréteur de commandes avec microsoft Visual Basic et des langages de script tels que microsoft JScript (compatible avec la spécification du langage ECMA 262) et microsoft Visual Basic scripting Edition (VBScript). Vous pouvez utiliser ces objets pour accéder à la plupart des fonctionnalités et boîtes de dialogue de l’interpréteur de commandes. Par exemple, vous pouvez accéder au système de fichiers, lancer des programmes et modifier les paramètres système.

Cette section présente les objets Shell scriptables.

-   [Versions de Shell](#shell-versions)
-   [Instanciation d’objets Shell](#instantiating-shell-objects)
    -   [Liaison tardive](#late-binding)
    -   [Élément objet HTML](#html-object-element)
-   [Objet Shell](#shell-object)
    -   [Sécurité](#security)
-   [Objets de dossier](#folder-objects)

## <a name="shell-versions"></a>Versions de Shell

La plupart des objets Shell sont disponibles dans la [version 4,71](versions.md) de l’interpréteur de commandes. D’autres sont disponibles dans la version 5,00 et les versions ultérieures. la Version 5,00 est devenue disponible avec Windows 2000. Le tableau suivant répertorie chaque objet Shell sous la version du Shell dans lequel l’objet est devenu disponible.



| Version 4,71                                            | Version 5,00                                          |
|---------------------------------------------------------|-------------------------------------------------------|
| [**Dossier**](folder.md)                                | [**DIDiskQuotaUser**](didiskquotauser-object.md)     |
| [**FolderItemVerb**](folderitemverb.md)                | [**DiskQuotaControl**](diskquotacontrol-object.md)   |
| [**FolderItemVerbs**](folderitemverbs.md)              | [**Dossier2**](folder2-object.md)                     |
| [**Shell**](shell.md)                                  | [**FolderItem**](folderitem.md)                      |
| [**ShellFolderView**](shellfolderview.md)              | [**FolderItems**](folderitems.md)                    |
| [**ShellUIHelper**](shelluihelper.md)                  | [**FolderItems2**](folderitems2-object.md)           |
| [**ShellWindows**](shellwindows.md)                    | [**IShellDispatch2**](ishelldispatch2-object.md)     |
| [**WebViewFolderContents**](../lwef/webviewfoldercontents.md) | [**IShellLinkDual2**](ishelllinkdual2-object.md)     |
|                                                         | [**ShellFolderItem**](shellfolderitem-object.md)     |
|                                                         | [**ShellFolderViewOC**](shellfolderviewoc-object.md) |
|                                                         | [**ShellLinkObject**](shelllinkobject-object.md)     |



 

## <a name="instantiating-shell-objects"></a>Instanciation d’objets Shell

pour instancier les objets Shell dans Visual Basic applications avec une liaison précoce, ajoutez des références aux bibliothèques suivantes dans votre projet :

-   Contrôles Microsoft Internet (SHDocVw)
-   Microsoft Shell Controls and Automation (shell32)

### <a name="late-binding"></a>Liaison tardive

Vous pouvez également instancier un grand nombre d’objets Shell avec une liaison tardive. cette approche fonctionne dans les applications Visual Basic et dans le script. L’exemple suivant montre comment instancier l’objet [**Shell**](shell.md) dans JScript.


```
<SCRIPT LANGUAGE="JScript">
<!--
    function fnCreateShell()    
    {
        // Instantiate the Shell object and invoke its FileRun method.
        var oShell = new ActiveXObject("shell.application");
        oshell.FileRun;
    }
-->
</SCRIPT>
```



L’exemple suivant montre comment instancier l’objet [**Folder**](folder.md) dans VBScript.


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnCreateFolder()
        dim oShell    
        dim oFolder
        dim sDir

        sDir = "C:\SomePath" 
        set oShell = CreateObject("shell.application")
        set oFolder = oShell.NameSpace(sDir)  
    end function
-->  
</SCRIPT>
```



Dans l’exemple précédent, *sDir* est le chemin d’accès à l’objet [**Folder**](folder.md) . Notez que les valeurs d’énumération [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) ne sont pas disponibles dans le script.

Le ProgID de chacun des objets Shell est indiqué dans le tableau suivant.



| Object                                                  | ProgID                                                                                  |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**DIDiskQuotaUser**](didiskquotauser-object.md)       | Microsoft. DiskQuota. 1                                                                   |
| [**DiskQuotaControl**](diskquotacontrol-object.md)     | Liaison tardive impossible                                                                        |
| [**Dossier**](folder.md)                                | Shell. Shell \_ application. Namespace ("...")                                               |
| [**Dossier2**](folder2-object.md)                       | Shell. Shell \_ application. Namespace ("...")                                               |
| [**FolderItem**](folderitem.md)                        | Shell. Shell \_ application. Namespace ("..."). Self ou dossier. Items. Item ou Folder. ParseName |
| [**FolderItems**](folderitems.md)                      | Dossier. Items                                                                            |
| [**FolderItems2**](folderitems2-object.md)             | Dossier. Items                                                                            |
| [**FolderItemVerb**](folderitemverb.md)                | Shell. NameSpace ("..."). Self. verbes. Item ()                                                |
| [**FolderItemVerbs**](folderitemverbs.md)              | FolderItem. Verbs ou Shell. NameSpace ("..."). Self. verbes                                   |
| [**IShellDispatch2**](ishelldispatch2-object.md)       | Shell. \_Application Shell                                                                |
| [**IShellLinkDual2**](ishelllinkdual2-object.md)       | Shell. NameSpace ("..."). Self. GetLink ou Shell. NameSpace ("..."). Items (). GetLink           |
| [**Shell**](shell.md)                                  | Shell. \_Application Shell                                                                |
| [**ShellFolderItem**](shellfolderitem-object.md)       | Shell. NameSpace ("..."). Self ou Shell. NameSpace ("..."). Items ()                           |
| [**ShellFolderView**](shellfolderview.md)              | Liaison tardive impossible                                                                        |
| [**ShellFolderViewOC**](shellfolderviewoc-object.md)   | Liaison tardive impossible                                                                        |
| [**ShellLinkObject**](shelllinkobject-object.md)       | Shell. NameSpace ("..."). Self. GetLink ou Shell. NameSpace ("..."). Items (). GetLink           |
| [**ShellUIHelper**](shelluihelper.md)                  | Liaison tardive impossible                                                                        |
| [**ShellWindows**](shellwindows.md)                    | Shell. Shell \_ Windows ou ShellWindows. \_ NewEnum                                          |
| [**WebViewFolderContents**](../lwef/webviewfoldercontents.md) | Liaison tardive impossible                                                                        |



 

### <a name="html-object-element"></a>Élément objet HTML

Vous pouvez également utiliser l’élément [**Object**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) pour instancier des objets Shell sur une page html. Pour ce faire, définissez l’attribut **ID** de l’élément **Object** sur le nom de la variable que vous allez utiliser dans vos scripts, puis identifiez l’objet à l’aide de son numéro d’inscription (ClassID). Le code HTML suivant crée une instance de l’objet [**ShellFolderItem**](shellfolderitem-object.md) à l’aide de l’élément **objet** .


```
<OBJECT ID="oShFolderItem" 
    NAME="Shell Folder Item Object"
    CLASSID="clsid:2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e">
</OBJECT>
```



Le tableau suivant répertorie chaque objet Shell et son CLASSID respectif.



| Objet Shell                                           | CLASSID                              |
|--------------------------------------------------------|--------------------------------------|
| [**DIDiskQuotaUser**](didiskquotauser-object.md)       | 7988B571-EC89-11cf-9C00-00AA00A14F56 |
| [**DiskQuotaControl**](diskquotacontrol-object.md)     | 7988B571-EC89-11cf-9C00-00AA00A14F56 |
| [**Dossier**](folder.md)                                | BBCBDE60-C3FF-11CE-8350-444553540000 |
| [**Dossier2**](folder2-object.md)                       | f0d2d8ef-3890-11d2-bf8b-00c04fb93661 |
| [**FolderItem**](folderitem.md)                        | 744129E0-CBE5-11CE-8350-444553540000 |
| [**FolderItems**](folderitems.md)                      | 744129E0-CBE5-11CE-8350-444553540000 |
| [**FolderItems2**](folderitems2-object.md)             | C94F0AD0-F363-11d2-A327-00C04F8EEC7F |
| [**FolderItemVerb**](folderitemverb.md)                | 08EC3E00-50B0-11CF-960C-0080C7F4EE85 |
| [**FolderItemVerbs**](folderitemverbs.md)              | 1F8352C0-50B0-11CF-960C-0080C7F4EE85 |
| [**IShellDispatch2**](ishelldispatch2-object.md)       | A4C6892C-3BA9-11d2-9DEA-00C04FB16162 |
| [**IShellLinkDual2**](ishelllinkdual2-object.md)       | 317EE249-F12E-11d2-B1E4-00C04F8EEB3E |
| [**Shell**](shell.md)                                  | 13709620-C279-11CE-A49E-444553540000 |
| [**ShellFolderItem**](shellfolderitem-object.md)       | 2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e |
| [**ShellFolderView**](shellfolderview.md)              | 62112AA1-EBE4-11cf-A5FB-0020AFE7292D |
| [**ShellFolderViewOC**](shellfolderviewoc-object.md)   | 4a3df050-23bd-11d2-939f-00a0c91eedba |
| [**ShellLinkObject**](shelllinkobject-object.md)       | 11219420-1768-11d1-95BE-00609797EA4F |
| [**ShellUIHelper**](shelluihelper.md)                  | 64AB4BB7-111E-11D1-8F79-00C04FC2FBE1 |
| [**ShellWindows**](shellwindows.md)                    | 9BA05972-F6A8-11CF-A442-00A0C90A8F39 |
| [**WebViewFolderContents**](../lwef/webviewfoldercontents.md) | 1820FED0-473E-11D0-A96C-00C04FD705A2 |



 

## <a name="shell-object"></a>Objet Shell

L’objet [**Shell**](shell.md) représente les objets dans l’interpréteur de commandes. Vous pouvez utiliser les méthodes exposées par l’objet Shell pour effectuer les opérations suivantes :

-   Ouvrir, Explorer et parcourir les dossiers.
-   Réduction, restauration, mise en cascade ou vignette des fenêtres ouvertes.
-   Lancez les applications du panneau de configuration.
-   Affiche les boîtes de dialogue système.

Les utilisateurs sont peut-être plus familiarisés avec les commandes auxquelles ils accèdent à partir du menu **Démarrer** et du menu contextuel de la barre des tâches. Le menu contextuel de la barre des tâches s’affiche lorsque les utilisateurs cliquent avec le bouton droit sur la barre des tâches. L’application HTML (HTA) suivante génère une page de démarrage avec des boutons qui implémentent un grand nombre des méthodes de l’objet [**Shell**](shell.md) . Certaines de ces méthodes implémentent des fonctionnalités dans le menu **Démarrer** et le menu contextuel de la barre des tâches.


```
<HTML>
<HEAD>
    <TITLE>Start Page</TITLE>
    
    <OBJECT ID="oShell"
        CLASSID="clsid:13709620-C279-11CE-A49E-444553540000">
    </OBJECT>
    
    <STYLE>
        INPUT {width: 200} 
    </STYLE>  
    
    <SCRIPT LANGUAGE="VBScript">
    <!--
        function fnStart(sMethod)
            select case sMethod
              case 0    
                  'Minimizes all windows on the desktop
                oshell.Shell_MinimizeAll
              case 1  
                  'Displays the Run dialog box
                oshell.FileRun
              case 2  
                  'Displays the Shut Down Windows dialog box
                oshell.Shell_ShutdownWindows
              case 3  
                  'Displays the Find dialog box
                oshell.Shell_FindFilesr
              case 4  
                  'Displays the Date/Time dialog box
                oshell.Shell_SetTime 
              case 5  
                  'Displays the Internet Properties dialog box
                oshell.Shell_ControlPanelItem "INETCPL.cpl"
              case 6  
                  'Explores the My Documents folder
                oshell.Shell_Explore "C:\My Documents"
              case 7  
                  'Enables user to select folder from Program Files
                oshell.Shell_BrowseForFolder 0, "My Programs", 0, "C:\Program Files" 
              case 8  
                  'Opens the Favorites folder
                oshell.Shell_Open "C:\WINDOWS\Favorites"
              case 9  
                  'Displays the Taskbar Properties dialog box
                oshell.Shell_TrayProperties
            end select  
        end function      
    -->
    </SCRIPT>
</HEAD>

<BODY>
    <H1>Start...</H1>
    <INPUT type="button" value="Edit Taskbar Properties" onclick="fnStart(9)"><br>
    <INPUT type="button" value="Open Favorites Folder" onclick="fnStart(8)"><br>
    <INPUT type="button" value="Browse Program Files" onclick="fnStart(7)"><br>
    <INPUT type="button" value="Explore My Documents" onclick="fnStart(6)"><br>
    <INPUT type="button" value="Modify Internet Properties" onclick="fnStart(5)"><br>
    <INPUT type="button" value="Set System Time" onclick="fnStart(4)"><br>
    <INPUT type="button" value="Find a File or Folder" onclick="fnStart(3)"><br>
    <INPUT type="button" value="Shut Down Windows" onclick="fnStart(2)"><br>
    <INPUT type="button" value="Run" onclick="fnStart(1)">     
    <INPUT type="button" value="Minimize All Windows" onclick="fnStart(0)">     
</BODY>
</HTML>
```



### <a name="security"></a>Sécurité

En tant qu’application, une HTA s’exécute sous un modèle de sécurité différent de celui d’une page Web. pour interagir avec une page web qui implémente la fonctionnalité des objets Shell, les utilisateurs doivent activer les **contrôles initialize et script ActiveX qui ne sont pas marqués comme sécurisés** pour la zone de sécurité dans laquelle ils visualisent la page.

## <a name="folder-objects"></a>Objets de dossier

L’objet [**Folder**](folder.md) représente un dossier shell. Vous pouvez utiliser les méthodes exposées par l’objet Folder pour effectuer les opérations suivantes :

-   Obtenir des informations sur un dossier.
-   Créer des sous-dossiers.
-   Copier et déplacer des objets de fichier dans le dossier.

L’objet [**FolderItem**](folderitem.md) représente un élément dans un dossier shell. Ses propriétés vous permettent de récupérer des informations sur l’élément. Vous pouvez utiliser les méthodes exposées par cet objet pour exécuter les verbes d’un élément, ou pour récupérer des informations sur l’objet [**FolderItemVerbs**](folderitemverbs.md) d’un élément.

L’objet [**FolderItems**](folderitems.md) représente une collection d’éléments dans un dossier shell. Ses méthodes et propriétés vous permettent de récupérer des informations sur la collection.

l’exemple de Visual Basic suivant montre la relation entre plusieurs objets de dossier et comment ils peuvent être utilisés ensemble. Quand l’utilisateur clique sur le bouton de commande appelé **cmdGetPath**, le programme affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner un dossier dans **poste de travail**, où ssfDRIVES est la valeur d’énumération [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) pour **poste de travail**. Quand l’utilisateur choisit un dossier, son chemin d’accès est affiché dans la zone de texte appelée **txtPath**.


```
Private Sub cmdGetPath_Click()
    Dim oShell As New Shell
    Dim oFolder As Folder
    Dim oFolderItem As FolderItem
 
    Set oFolder = oshell.Shell_BrowseForFolder(Me.hWnd, "Select a Folder", 0, ssfDrives)
   
    Set oFolderItem = oFolderItems.Item

    txtPath.Text = oFolderItem.Path
End Sub
```



Dans VBScript, cette fonction est légèrement différente, car les valeurs d’énumération [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) ne sont pas disponibles dans le script. L’exemple suivant illustre l’équivalent en VBScript de l’exemple précédent.


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnGetMyPathVB() 
        dim oShell
        dim oFolder
        dim oFolderItem
        
        set oShell = CreateObject("shell.application")      
        set oFolder = oshell.Shell_BrowseForFolder(0, "Choose a Folder", 0)             
        set oFolderItem = oFolder.Items.Item         
        
        document.all.item("myPath").innerText = oFolderItem.Path                                
    end function
-->
</SCRIPT>
```



dans l’exemple de JScript suivant, qui est une traduction directe de l’exemple VBScript précédent, notez la manière dont les parenthèses vides « () » sont utilisées pour appeler les [**méthodes items et**](folder-items.md) [**item**](folderitems-item.md) .


```
<SCRIPT LANGUAGE="JavaScript">
<!--
    function fnGetMyPathJ() 
    {       
        var oShell = new ActiveXObject("shell.application");
                    
        var oFolder = new Object;                   
        oFolder = oshell.Shell_BrowseForFolder(0, "Choose a folder", 0);
                                
        var oFolderItem = new Object;       
        oFolderItem = oFolder.Items().Item();                               
        
        document.all.item("myPath").innerText = oFolderItem.Path;
    }    
-->
</SCRIPT>
```



 

 
