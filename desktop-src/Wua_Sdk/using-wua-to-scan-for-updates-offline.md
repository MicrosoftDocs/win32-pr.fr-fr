---
description: Windows Update Agent (WUA) peut être utilisé pour analyser les ordinateurs à la recherche de mises à jour de sécurité sans se connecter à Windows Update ou à un serveur Windows Server Update Services (WSUS), ce qui permet d’analyser les ordinateurs qui ne sont pas connectés à Internet pour rechercher les mises à jour de sécurité. L’analyse hors connexion des mises à jour nécessite le téléchargement d’un fichier signé, Wsusscn2.cab, à partir de Windows Update.
ms.assetid: 452b53af-0f7b-435e-bf12-dd9d84cbd564
title: Utilisation de WUA pour rechercher des mises à jour hors connexion
ms.topic: article
ms.date: 07/23/2020
ms.openlocfilehash: 242ff3655f4ab469d8d768a94f8dc8e529e0da74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318065"
---
# <a name="using-wua-to-scan-for-updates-offline"></a><span data-ttu-id="8b100-104">Utilisation de WUA pour rechercher des mises à jour hors connexion</span><span class="sxs-lookup"><span data-stu-id="8b100-104">Using WUA to Scan for Updates Offline</span></span>

<span data-ttu-id="8b100-105">Windows Update Agent (WUA) peut être utilisé pour analyser les ordinateurs à la recherche de mises à jour de sécurité sans se connecter à Windows Update ou à un serveur Windows Server Update Services (WSUS), ce qui permet d’analyser les ordinateurs qui ne sont pas connectés à Internet pour rechercher les mises à jour de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8b100-105">Windows Update Agent (WUA) can be used to scan computers for security updates without connecting to Windows Update or to a Windows Server Update Services (WSUS) server, which enables computers that are not connected to the Internet to be scanned for security updates.</span></span>

<span data-ttu-id="8b100-106">L’analyse hors connexion des mises à jour nécessite le téléchargement d’un fichier signé, Wsusscn2.cab, à partir de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="8b100-106">Offline scanning for updates requires the download of a signed file, Wsusscn2.cab, from Windows Update.</span></span>

<span data-ttu-id="8b100-107">Le fichier Wsusscn2.cab est un fichier CAB signé par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8b100-107">The Wsusscn2.cab file is a cabinet file that is signed by Microsoft.</span></span> <span data-ttu-id="8b100-108">Ce fichier contient des informations sur les mises à jour liées à la sécurité publiées par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8b100-108">This file contains info about security-related updates that are published by Microsoft.</span></span> <span data-ttu-id="8b100-109">Les ordinateurs qui ne sont pas connectés à Internet peuvent être analysés pour déterminer si ces mises à jour liées à la sécurité sont présentes ou requises.</span><span class="sxs-lookup"><span data-stu-id="8b100-109">Computers that aren't connected to the Internet can be scanned to see whether these security-related updates are present or required.</span></span> <span data-ttu-id="8b100-110">Le fichier Wsusscn2.cab ne contient pas les mises à jour de sécurité elles-mêmes. vous devez donc vous procurer et installer les mises à jour de sécurité nécessaires par d’autres moyens.</span><span class="sxs-lookup"><span data-stu-id="8b100-110">The Wsusscn2.cab file doesn't contain the security updates themselves so you must obtain and install any needed security-related updates through other means.</span></span> <span data-ttu-id="8b100-111">Les nouvelles versions du fichier Wsusscn2.cab sont publiées régulièrement à mesure que des mises à jour liées à la sécurité sont publiées, supprimées ou révisées sur le site Windows Update.</span><span class="sxs-lookup"><span data-stu-id="8b100-111">New versions of the Wsusscn2.cab file are released periodically as security-related updates are released, removed, or revised on the Windows Update site.</span></span> <span data-ttu-id="8b100-112">Le dernier fichier de Wsusscn2.cab est disponible en téléchargement à l’emplacement suivant : [télécharger Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)</span><span class="sxs-lookup"><span data-stu-id="8b100-112">The latest Wsusscn2.cab file is available for download at the following location: [Download Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)</span></span>

<span data-ttu-id="8b100-113">Une fois que vous avez téléchargé la dernière Wsusscn2.cab, le fichier peut être fourni à la méthode [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) , et l’API WUA peut être utilisée pour rechercher les mises à jour de sécurité sur l’ordinateur hors connexion.</span><span class="sxs-lookup"><span data-stu-id="8b100-113">After you download the latest Wsusscn2.cab, the file can be provided to the [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) method, and the WUA API can be used to search the offline computer for security updates.</span></span> <span data-ttu-id="8b100-114">WUA vérifie que le Wsusscn2.cab est signé par un certificat Microsoft valide avant d’exécuter une analyse hors connexion.</span><span class="sxs-lookup"><span data-stu-id="8b100-114">WUA validates that the Wsusscn2.cab is signed by a valid Microsoft certificate before running an offline scan.</span></span>

> [!NOTE]
> <span data-ttu-id="8b100-115">Conformément à notre [initiative SHA-1](https://aka.ms/sha1deprecation), le fichier Wsusscn2.cab n’est plus une double signature à l’aide de SHA-1 et de la suite SHA-2 des algorithmes de hachage (plus particulièrement sha-256).</span><span class="sxs-lookup"><span data-stu-id="8b100-115">In accordance with our [SHA-1 deprecation initiative](https://aka.ms/sha1deprecation), the Wsusscn2.cab file is no longer dual-signed using both SHA-1 and the SHA-2 suite of hash algorithms (specifically SHA-256).</span></span> <span data-ttu-id="8b100-116">Ce fichier est maintenant signé à l’aide de SHA-256 uniquement.</span><span class="sxs-lookup"><span data-stu-id="8b100-116">This file is now signed using only SHA-256.</span></span> <span data-ttu-id="8b100-117">Les administrateurs qui vérifient les signatures numériques de ce fichier doivent à présent attendre uniquement des signatures SHA-256 uniques.</span><span class="sxs-lookup"><span data-stu-id="8b100-117">Administrators who verify digital signatures on this file should now expect only single SHA-256 signatures.</span></span>

## <a name="example"></a><span data-ttu-id="8b100-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="8b100-118">Example</span></span>

<span data-ttu-id="8b100-119">L’exemple suivant utilise le fichier Wsusscn2.cab pour analyser un ordinateur et afficher les mises à jour manquantes.</span><span class="sxs-lookup"><span data-stu-id="8b100-119">The following example uses the Wsusscn2.cab file to scan a computer and displays updates that are missing.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8b100-120">Ce script est destiné à illustrer l’utilisation des API d’agent Windows Update et fournit un exemple de la façon dont les développeurs peuvent utiliser ces API pour résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="8b100-120">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="8b100-121">Ce script n’est pas conçu comme un code de production, et le script lui-même n’est pas pris en charge par Microsoft (bien que les API de l’agent de Windows Update sous-jacent soient prises en charge).</span><span class="sxs-lookup"><span data-stu-id="8b100-121">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


```VB
Set UpdateSession = CreateObject("Microsoft.Update.Session")
Set UpdateServiceManager = CreateObject("Microsoft.Update.ServiceManager")
Set UpdateService = UpdateServiceManager.AddScanPackageService("Offline Sync Service", "c:\wsusscn2.cab", 1)
Set UpdateSearcher = UpdateSession.CreateUpdateSearcher()

WScript.Echo "Searching for updates..." & vbCRLF

UpdateSearcher.ServerSelection = 3 ' ssOthers

UpdateSearcher.ServiceID = UpdateService.ServiceID

Set SearchResult = UpdateSearcher.Search("IsInstalled=0")

Set Updates = SearchResult.Updates

If searchResult.Updates.Count = 0 Then
    WScript.Echo "There are no applicable updates."
    WScript.Quit
End If

WScript.Echo "List of applicable items on the machine when using wssuscan.cab:" & vbCRLF

For I = 0 to searchResult.Updates.Count-1
    Set update = searchResult.Updates.Item(I)
    WScript.Echo I + 1 & "> " & update.Title
Next

WScript.Quit
```



 

 



