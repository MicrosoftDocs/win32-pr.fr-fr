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
# <a name="searching-downloading-and-installing-specific-updates"></a><span data-ttu-id="98963-104">Recherche, téléchargement et installation de mises à jour spécifiques</span><span class="sxs-lookup"><span data-stu-id="98963-104">Searching, Downloading, and Installing Specific Updates</span></span>

<span data-ttu-id="98963-105">L’exemple de script de cette rubrique montre comment utiliser l’agent de Windows Update (WUA) pour analyser, télécharger et installer une mise à jour spécifique.</span><span class="sxs-lookup"><span data-stu-id="98963-105">The scripting sample in this topic shows you how to use the Windows Update Agent (WUA) to scan, download, and install a specific update.</span></span> <span data-ttu-id="98963-106">La mise à jour peut être spécifiée par son titre.</span><span class="sxs-lookup"><span data-stu-id="98963-106">The update can be specified by its title.</span></span>

<span data-ttu-id="98963-107">L’exemple recherche une mise à jour logicielle spécifique, télécharge la mise à jour, puis installe la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="98963-107">The sample searches for a specific software update, downloads the update, and then installs the update.</span></span> <span data-ttu-id="98963-108">Par exemple, un utilisateur peut utiliser cette méthode pour déterminer si une mise à jour de sécurité critique est installée sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="98963-108">For example, a user can use this method to determine if a critical security update is installed on a computer.</span></span> <span data-ttu-id="98963-109">Si la mise à jour n’est pas installée, l’utilisateur peut s’assurer que la mise à jour est téléchargée et installée.</span><span class="sxs-lookup"><span data-stu-id="98963-109">If the update isn't installed, the user can ensure that the update is downloaded and installed.</span></span> <span data-ttu-id="98963-110">L’utilisateur peut également s’assurer qu’il est informé de l’état de l’installation.</span><span class="sxs-lookup"><span data-stu-id="98963-110">The user can also ensure that they are notified about the status of the installation.</span></span>

<span data-ttu-id="98963-111">L’exemple de mise à jour est identifié par le titre de la mise à jour dans la [**propriété Title de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title).</span><span class="sxs-lookup"><span data-stu-id="98963-111">The sample update is identified by the update title in [**Title Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title).</span></span> <span data-ttu-id="98963-112">Le titre de la mise à jour suggérée dans cet exemple est « mise à jour pour Windows Rights Management client 1,0 ».</span><span class="sxs-lookup"><span data-stu-id="98963-112">The title of the update that is suggested in this sample is "Update for Windows Rights Management client 1.0."</span></span>

> [!Note]  
> <span data-ttu-id="98963-113">Pour plus d’informations sur la recherche, le téléchargement et l’installation de toutes les mises à jour qui s’appliquent à une application spécifique, consultez [recherche, téléchargement et installation des mises à jour](searching--downloading--and-installing-updates.md).</span><span class="sxs-lookup"><span data-stu-id="98963-113">For info about how to search, download, and install all the updates that apply to a specific application, see [Searching, Downloading, and Installing Updates](searching--downloading--and-installing-updates.md).</span></span>

 

<span data-ttu-id="98963-114">Avant de tenter d’exécuter cet exemple, notez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="98963-114">Before you attempt to run this sample, note the following:</span></span>

-   <span data-ttu-id="98963-115">WUA doit être installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="98963-115">WUA must be installed on the computer.</span></span> <span data-ttu-id="98963-116">Pour plus d’informations sur la façon de déterminer la version de WUA installée, consultez [détermination de la version actuelle de WUA](determining-the-current-version-of-wua.md).</span><span class="sxs-lookup"><span data-stu-id="98963-116">For more info about how to determine the version of WUA that is installed, see [Determining the Current Version of WUA](determining-the-current-version-of-wua.md).</span></span>
-   <span data-ttu-id="98963-117">L’exemple ne fournit pas sa propre interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="98963-117">The sample doesn't provide its own user interface.</span></span> <span data-ttu-id="98963-118">WUA invite l’utilisateur à redémarrer l’ordinateur si une mise à jour nécessite un redémarrage.</span><span class="sxs-lookup"><span data-stu-id="98963-118">WUA prompts the user to restart the computer if an update requires a restart.</span></span>
-   <span data-ttu-id="98963-119">L’exemple peut télécharger des mises à jour à partir de WUA uniquement.</span><span class="sxs-lookup"><span data-stu-id="98963-119">The sample can download updates only from WUA.</span></span> <span data-ttu-id="98963-120">Il ne peut pas télécharger les mises à jour à partir d’un serveur SUS (Software Update Services) 1,0.</span><span class="sxs-lookup"><span data-stu-id="98963-120">It can't download updates from a Software Update Services (SUS) 1.0 server.</span></span>
-   <span data-ttu-id="98963-121">L’exécution de cet exemple nécessite Windows Script Host (WSH).</span><span class="sxs-lookup"><span data-stu-id="98963-121">Running this sample requires Windows Script Host (WSH).</span></span> <span data-ttu-id="98963-122">Pour plus d’informations sur WSH, consultez la section WSH du kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="98963-122">For more info about WSH, see the WSH section of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="98963-123">Si l’exemple est copié dans un fichier nommé WUA \_SpecificUpdate.vbs, vous pouvez l’exécuter en ouvrant une fenêtre d’invite de commandes et en tapant la commande suivante : **cscript WUA \_SpecificUpdate.vbs**</span><span class="sxs-lookup"><span data-stu-id="98963-123">If the sample is copied to a file named WUA\_SpecificUpdate.vbs, you can run it by opening a Command Prompt window and by typing this command: **cscript WUA\_SpecificUpdate.vbs**</span></span>  
    

## <a name="example"></a><span data-ttu-id="98963-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="98963-124">Example</span></span>

> [!IMPORTANT]
> <span data-ttu-id="98963-125">Ce script est destiné à illustrer l’utilisation des API d’agent Windows Update et fournit un exemple de la façon dont les développeurs peuvent utiliser ces API pour résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="98963-125">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="98963-126">Ce script n’est pas conçu comme un code de production, et le script lui-même n’est pas pris en charge par Microsoft (bien que les API de l’agent de Windows Update sous-jacent soient prises en charge).</span><span class="sxs-lookup"><span data-stu-id="98963-126">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


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



 

 



