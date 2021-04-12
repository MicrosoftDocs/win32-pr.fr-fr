---
description: L’exemple de script de cette rubrique montre comment utiliser l’agent de Windows Update (WUA) pour analyser, télécharger et installer une mise à jour spécifique. La mise à jour peut être spécifiée par son titre.
ms.assetid: 4a5bb920-fc51-48a0-8f66-bb2fcc72589f
title: Recherche, téléchargement et installation de mises à jour spécifiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aadd7903303356c3937f41e44aa7a47e71192409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318498"
---
# <a name="searching-downloading-and-installing-specific-updates"></a>Recherche, téléchargement et installation de mises à jour spécifiques

L’exemple de script de cette rubrique montre comment utiliser l’agent de Windows Update (WUA) pour analyser, télécharger et installer une mise à jour spécifique. La mise à jour peut être spécifiée par son titre.

L’exemple recherche une mise à jour logicielle spécifique, télécharge la mise à jour, puis installe la mise à jour. Par exemple, un utilisateur peut utiliser cette méthode pour déterminer si une mise à jour de sécurité critique est installée sur un ordinateur. Si la mise à jour n’est pas installée, l’utilisateur peut s’assurer que la mise à jour est téléchargée et installée. L’utilisateur peut également s’assurer qu’il est informé de l’état de l’installation.

L’exemple de mise à jour est identifié par le titre de la mise à jour dans la [**propriété Title de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title). Le titre de la mise à jour suggérée dans cet exemple est « mise à jour pour Windows Rights Management client 1,0 ».

> [!Note]  
> Pour plus d’informations sur la recherche, le téléchargement et l’installation de toutes les mises à jour qui s’appliquent à une application spécifique, consultez [recherche, téléchargement et installation des mises à jour](searching--downloading--and-installing-updates.md).

 

Avant de tenter d’exécuter cet exemple, notez les points suivants :

-   WUA doit être installé sur l’ordinateur. Pour plus d’informations sur la façon de déterminer la version de WUA installée, consultez [détermination de la version actuelle de WUA](determining-the-current-version-of-wua.md).
-   L’exemple ne fournit pas sa propre interface utilisateur. WUA invite l’utilisateur à redémarrer l’ordinateur si une mise à jour nécessite un redémarrage.
-   L’exemple peut télécharger des mises à jour à partir de WUA uniquement. Il ne peut pas télécharger les mises à jour à partir d’un serveur SUS (Software Update Services) 1,0.
-   L’exécution de cet exemple nécessite Windows Script Host (WSH). Pour plus d’informations sur WSH, consultez la section WSH du kit de développement logiciel (SDK) de la plateforme. Si l’exemple est copié dans un fichier nommé WUA \_SpecificUpdate.vbs, vous pouvez l’exécuter en ouvrant une fenêtre d’invite de commandes et en tapant la commande suivante : **cscript WUA \_SpecificUpdate.vbs**  
    

## <a name="example"></a>Exemple

> [!IMPORTANT]
> Ce script est destiné à illustrer l’utilisation des API d’agent Windows Update et fournit un exemple de la façon dont les développeurs peuvent utiliser ces API pour résoudre les problèmes. Ce script n’est pas conçu comme un code de production, et le script lui-même n’est pas pris en charge par Microsoft (bien que les API de l’agent de Windows Update sous-jacent soient prises en charge).

 


```VB
Set updateSession = CreateObject("Microsoft.Update.Session")
updateSession.ClientApplicationID = "MSDN Sample Script"

'Get update title to search for
WScript.Echo "Enter the title of the update: " & _
"(for example, Update for Windows Rights Management client 1.0)"
updateTitle = WScript.StdIn.Readline

WScript.Echo vbCRLF & "Searching for: " & updateTitle & "..."

Set updateSearcher = updateSession.CreateupdateSearcher()

'Search for all software updates, already installed and not installed
Set searchResult = _
updateSearcher.Search("Type='Software'")

Set updateToInstall = CreateObject("Microsoft.Update.UpdateColl")

updateIsApplicable = False

'Cycle through search results to look for the update title
For i = 0 To searchResult.Updates.Count-1
   Set update = searchResult.Updates.Item(i)
   If UCase(update.Title) = UCase(updateTitle) Then
   'Update in list of applicable updates 
   'Determine if it is already installed or not
      If update.IsInstalled = False Then
         WScript.Echo vbCRLF & _
         "Result: Update applicable, not installed."
         updateIsApplicable = True
         updateToInstall.Add(update)
      Else 
         'Update is installed so notify user and quit
         WScript.Echo vbCRLF & _
         "Result: Update applicable, already installed."
         updateIsApplicable = True
         WScript.Quit 
      End If
   End If 
Next

If updateIsApplicable = False Then
   WScript.Echo "Result: Update is not applicable to this machine."
   WScript.Quit
End If

WScript.Echo vbCRLF & "Would you like to install now? (Y/N)"
stdInput = WScript.StdIn.Readline
 
If (strInput = "N" or strInput = "n") Then 
   WScript.Quit
ElseIf  (stdInput = "Y" OR stdInput = "y") Then
   'Download update
   Set downloader = updateSession.CreateUpdateDownloader() 
   downloader.Updates = updateToInstall
   WScript.Echo vbCRLF & "Downloading..."
   Set downloadResult = downloader.Download()
   WScript.Echo "Download Result: " & downloadResult.ResultCode
  
   'Install Update
   Set installer = updateSession.CreateUpdateInstaller()
   WScript.Echo vbCRLF & "Installing..."
   installer.Updates = updateToInstall
   Set installationResult = installer.Install()
  
   'Output the result of the installation
   WScript.Echo "Installation Result: " & _
   installationResult.ResultCode
   WScript.Echo "Reboot Required: " & _
   installationResult.RebootRequired 
End If
```



 

 



